---
title: Finite types
---

```agda
{-# OPTIONS --without-K --exact-split #-}

module univalent-combinatorics.finite-types where

open import elementary-number-theory.equality-natural-numbers using
  ( is-set-ℕ; ℕ-Set; has-decidable-equality-ℕ)
open import elementary-number-theory.modular-arithmetic using (ℤ-Mod)
open import elementary-number-theory.natural-numbers using
  ( ℕ; zero-ℕ; is-nonzero-ℕ; succ-ℕ; is-zero-ℕ; is-one-ℕ)

open import foundation.booleans using (bool)
open import foundation.connected-components-universes using
  ( equiv-component-UU-Level; equiv-component-UU; id-equiv-component-UU-Level;
    id-equiv-component-UU; equiv-eq-component-UU-Level; equiv-eq-component-UU;
    is-contr-total-equiv-component-UU-Level; is-contr-total-equiv-component-UU;
    is-equiv-equiv-eq-component-UU-Level; is-equiv-equiv-eq-component-UU;
    eq-equiv-component-UU-Level; eq-equiv-component-UU)
open import foundation.connected-types using
  ( is-path-connected; is-path-connected-mere-eq)
open import foundation.contractible-types using
  ( is-contr; equiv-is-contr; is-contr-Prop; is-contr-equiv')
open import foundation.coproduct-types using (coprod; inl; inr)
open import foundation.decidable-equality using
  ( has-decidable-equality; has-decidable-equality-Prop;
    has-decidable-equality-equiv')
open import foundation.decidable-propositions using
  ( decidable-Prop; equiv-bool-decidable-Prop)
open import foundation.decidable-types using
  ( is-decidable; is-inhabited-or-empty; is-inhabited-or-empty-Prop;
    is-decidable-iff)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.empty-types using
  ( empty; is-empty; ex-falso; is-empty-Prop; empty-Prop)
open import foundation.equivalences using
  ( id-equiv; _≃_; is-equiv; inv-equiv; _∘e_; map-equiv; equiv-precomp-equiv)
open import foundation.functions using (id; _∘_)
open import foundation.functoriality-coproduct-types using (map-coprod)
open import foundation.functoriality-dependent-pair-types using
  ( equiv-tot)
open import foundation.functoriality-propositional-truncation using
  ( functor-trunc-Prop)
open import foundation.identity-types using
  ( refl; Id; _∙_; ap; tr; equiv-tr; inv)
open import foundation.mere-equivalences using
  ( mere-equiv-Prop; mere-equiv)
open import foundation.propositional-truncations using
  ( trunc-Prop; unit-trunc-Prop; map-universal-property-trunc-Prop;
    apply-universal-property-trunc-Prop; type-trunc-Prop; ind-trunc-Prop;
    is-prop-type-trunc-Prop)
open import foundation.propositions using
  ( UU-Prop; type-Prop; is-prop; is-prop-type-Prop; is-proof-irrelevant-is-prop;
    all-elements-equal; is-prop-all-elements-equal; eq-is-prop; eq-is-prop';
    equiv-prop; is-equiv-is-prop)
open import foundation.raising-universe-levels using (equiv-raise)
open import foundation.sets using (is-set; is-set-Prop; Id-Prop)
open import foundation.subtypes using (eq-subtype)
open import foundation.type-arithmetic-dependent-pair-types using
  ( equiv-left-swap-Σ)
open import foundation.type-arithmetic-empty-type using
  ( left-unit-law-coprod)
open import foundation.unit-type using (unit; star; is-contr-unit)
open import foundation.universe-levels using (Level; UU; _⊔_; lsuc; lzero)

open import univalent-combinatorics.counting using
  ( count; count-empty; count-is-empty; count-unit; count-is-contr; count-Fin;
    count-equiv; is-set-count; equiv-count; number-of-elements-count;
    is-empty-is-zero-number-of-elements-count; is-inhabited-or-empty-count;
    count-type-trunc-Prop; inv-equiv-count)
open import univalent-combinatorics.equality-standard-finite-types using
  ( has-decidable-equality-Fin)
open import univalent-combinatorics.standard-finite-types using
  ( Fin; raise-Fin; equiv-raise-Fin; is-injective-Fin; equiv-bool-Fin-two-ℕ;
    is-contr-Fin-one-ℕ)
```

## Idea

A type is finite if it is merely equivalent to a standard finite type.

## Definition

### Finite types

```agda
is-finite-Prop :
  {l : Level} → UU l → UU-Prop l
is-finite-Prop X = trunc-Prop (count X)

is-finite :
  {l : Level} → UU l → UU l
is-finite X = type-Prop (is-finite-Prop X)

abstract
  is-prop-is-finite :
    {l : Level} (X : UU l) → is-prop (is-finite X)
  is-prop-is-finite X = is-prop-type-Prop (is-finite-Prop X)

abstract
  is-finite-count :
    {l : Level} {X : UU l} → count X → is-finite X
  is-finite-count = unit-trunc-Prop
```

### The type of all finite types

```agda
𝔽 : UU (lsuc lzero)
𝔽 = Σ (UU lzero) is-finite

type-𝔽 : 𝔽 → UU lzero
type-𝔽 X = pr1 X

abstract
  is-finite-type-𝔽 : (X : 𝔽) → is-finite (type-𝔽 X)
  is-finite-type-𝔽 X = pr2 X
```

### Types with cardinality `k`

```agda
has-cardinality-Prop :
  {l : Level} → ℕ → UU l → UU-Prop l
has-cardinality-Prop k X = mere-equiv-Prop (Fin k) X

has-cardinality :
  {l : Level} → ℕ → UU l → UU l
has-cardinality k X = mere-equiv (Fin k) X
```

### The type of all types of cardinality k of a given universe leve l

```agda
UU-Fin-Level : (l : Level) → ℕ → UU (lsuc l)
UU-Fin-Level l k = Σ (UU l) (mere-equiv (Fin k))

type-UU-Fin-Level : {l : Level} {k : ℕ} → UU-Fin-Level l k → UU l
type-UU-Fin-Level X = pr1 X

abstract
  has-cardinality-type-UU-Fin-Level :
    {l : Level} {k : ℕ} (X : UU-Fin-Level l k) →
    mere-equiv (Fin k) (type-UU-Fin-Level X)
  has-cardinality-type-UU-Fin-Level X = pr2 X
```

### The type of all types of cardinality k of univerese level `lzero`

```agda
UU-Fin : ℕ → UU (lsuc lzero)
UU-Fin k = UU-Fin-Level lzero k

type-UU-Fin : {k : ℕ} → UU-Fin k → UU lzero
type-UU-Fin X = pr1 X

abstract
  has-cardinality-type-UU-Fin :
    {k : ℕ} (X : UU-Fin k) → has-cardinality k (type-UU-Fin X)
  has-cardinality-type-UU-Fin X = pr2 X
```

### Types of finite cardinality

```agda
has-finite-cardinality :
  {l : Level} → UU l → UU l
has-finite-cardinality X = Σ ℕ (λ k → has-cardinality k X)

number-of-elements-has-finite-cardinality :
  {l : Level} {X : UU l} → has-finite-cardinality X → ℕ
number-of-elements-has-finite-cardinality = pr1

abstract
  mere-equiv-has-finite-cardinality :
    {l : Level} {X : UU l} (c : has-finite-cardinality X) →
    type-trunc-Prop (Fin (number-of-elements-has-finite-cardinality c) ≃ X)
  mere-equiv-has-finite-cardinality = pr2
```

## Properties

### Finite types are closed under equivalences

```agda
abstract
  is-finite-equiv :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} (e : A ≃ B) →
    is-finite A → is-finite B
  is-finite-equiv e =
    map-universal-property-trunc-Prop
      ( is-finite-Prop _)
      ( is-finite-count ∘ (count-equiv e))

abstract
  is-finite-is-equiv :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} {f : A → B} →
    is-equiv f → is-finite A → is-finite B
  is-finite-is-equiv is-equiv-f =
    map-universal-property-trunc-Prop
      ( is-finite-Prop _)
      ( is-finite-count ∘ (count-equiv (pair _ is-equiv-f)))

abstract
  is-finite-equiv' :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} (e : A ≃ B) →
    is-finite B → is-finite A
  is-finite-equiv' e = is-finite-equiv (inv-equiv e)
```

### Finite types are closed under mere equivalences

```agda
abstract
  is-finite-mere-equiv :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} → mere-equiv A B →
    is-finite A → is-finite B
  is-finite-mere-equiv e H =
    apply-universal-property-trunc-Prop e
      ( is-finite-Prop _)
      ( λ e' → is-finite-equiv e' H)
```

### The empty type is finite

```agda
abstract
  is-finite-empty : is-finite empty
  is-finite-empty = is-finite-count count-empty

empty-𝔽 : 𝔽
pr1 empty-𝔽 = empty
pr2 empty-𝔽 = is-finite-empty

empty-UU-Fin : UU-Fin zero-ℕ
pr1 empty-UU-Fin = empty
pr2 empty-UU-Fin = unit-trunc-Prop id-equiv
```

### The empty type has finite cardinality

```agda
has-finite-cardinality-empty : has-finite-cardinality empty
pr1 has-finite-cardinality-empty = zero-ℕ
pr2 has-finite-cardinality-empty = unit-trunc-Prop id-equiv
```

### Empty types are finite

```agda
abstract
  is-finite-is-empty :
    {l1 : Level} {X : UU l1} → is-empty X → is-finite X
  is-finite-is-empty H = is-finite-count (count-is-empty H)
```

### Empty types have finite cardinality

```agda
has-finite-cardinality-is-empty :
  {l1 : Level} {X : UU l1} → is-empty X → has-finite-cardinality X
pr1 (has-finite-cardinality-is-empty f) = zero-ℕ
pr2 (has-finite-cardinality-is-empty f) =
  unit-trunc-Prop (equiv-count (count-is-empty f))
```

### The unit type is finite

```agda
abstract
  is-finite-unit : is-finite unit
  is-finite-unit = is-finite-count count-unit

unit-𝔽 : 𝔽
pr1 unit-𝔽 = unit
pr2 unit-𝔽 = is-finite-unit

unit-UU-Fin : UU-Fin 1
pr1 unit-UU-Fin = unit
pr2 unit-UU-Fin = unit-trunc-Prop (left-unit-law-coprod unit)
```

### Contractible types are finite

```agda
abstract
  is-finite-is-contr :
    {l1 : Level} {X : UU l1} → is-contr X → is-finite X
  is-finite-is-contr H = is-finite-count (count-is-contr H)

abstract
  has-cardinality-is-contr :
    {l1 : Level} {X : UU l1} → is-contr X → has-cardinality 1 X
  has-cardinality-is-contr H =
    unit-trunc-Prop (equiv-is-contr is-contr-Fin-one-ℕ H)
```

### Decidable propositions are finite

```agda
abstract
  is-finite-is-decidable-Prop :
    {l : Level} (P : UU-Prop l) →
    is-decidable (type-Prop P) → is-finite (type-Prop P)
  is-finite-is-decidable-Prop P (inl x) =
    is-finite-is-contr (is-proof-irrelevant-is-prop (is-prop-type-Prop P) x)
  is-finite-is-decidable-Prop P (inr x) =
    is-finite-is-empty x
```

### The standard finite types are finite

```agda
abstract
  is-finite-Fin : {k : ℕ} → is-finite (Fin k)
  is-finite-Fin {k} = is-finite-count (count-Fin k)

Fin-𝔽 : ℕ → 𝔽
pr1 (Fin-𝔽 k) = Fin k
pr2 (Fin-𝔽 k) = is-finite-Fin

Fin-UU-Fin : (k : ℕ) → UU-Fin k
pr1 (Fin-UU-Fin k) = Fin k
pr2 (Fin-UU-Fin k) = unit-trunc-Prop id-equiv

has-cardinality-raise-Fin :
  {l : Level} {k : ℕ} → has-cardinality k (raise-Fin l k)
has-cardinality-raise-Fin {l} {k} = unit-trunc-Prop (equiv-raise-Fin l k)

Fin-UU-Fin-Level : (l : Level) (k : ℕ) → UU-Fin-Level l k
pr1 (Fin-UU-Fin-Level l k) = raise-Fin l k
pr2 (Fin-UU-Fin-Level l k) = has-cardinality-raise-Fin
```

### The type of booleans is finite

```agda
is-finite-bool : is-finite bool
is-finite-bool = is-finite-equiv equiv-bool-Fin-two-ℕ is-finite-Fin
```

### The type of decidable propositions of any universe level is finite

```agda
is-finite-decidable-Prop : {l : Level} → is-finite (decidable-Prop l)
is-finite-decidable-Prop {l} =
  is-finite-equiv' equiv-bool-decidable-Prop is-finite-bool
```

### The types `ℤ-Mod k` are finite for nonzero natural numbers `k`

```agda
abstract
  is-finite-ℤ-Mod : {k : ℕ} → is-nonzero-ℕ k → is-finite (ℤ-Mod k)
  is-finite-ℤ-Mod {zero-ℕ} H = ex-falso (H refl)
  is-finite-ℤ-Mod {succ-ℕ k} H = is-finite-Fin

ℤ-Mod-𝔽 : (k : ℕ) → is-nonzero-ℕ k → 𝔽
pr1 (ℤ-Mod-𝔽 k H) = ℤ-Mod k
pr2 (ℤ-Mod-𝔽 k H) = is-finite-ℤ-Mod H
```

### Every type of cardinality `k` is finite

```agda
abstract
  is-finite-type-UU-Fin-Level :
    {l : Level} {k : ℕ} (X : UU-Fin-Level l k) → is-finite (type-UU-Fin-Level X)
  is-finite-type-UU-Fin-Level X =
    is-finite-mere-equiv
      ( has-cardinality-type-UU-Fin-Level X)
      ( is-finite-Fin)

abstract
  is-finite-type-UU-Fin :
    {k : ℕ} (X : UU-Fin k) → is-finite (type-UU-Fin X)
  is-finite-type-UU-Fin X = is-finite-type-UU-Fin-Level X
```

### Having a finite cardinality is a proposition

```agda
abstract
  all-elements-equal-has-finite-cardinality :
    {l1 : Level} {X : UU l1} → all-elements-equal (has-finite-cardinality X)
  all-elements-equal-has-finite-cardinality {l1} {X} (pair k K) (pair l L) =
    eq-subtype
      ( λ k → mere-equiv-Prop (Fin k) X)
      ( apply-universal-property-trunc-Prop K
        ( pair (Id k l) (is-set-ℕ k l))
        ( λ (e : Fin k ≃ X) →
          apply-universal-property-trunc-Prop L
            ( pair (Id k l) (is-set-ℕ k l))
            ( λ (f : Fin l ≃ X) → is-injective-Fin ((inv-equiv f) ∘e e))))

abstract
  is-prop-has-finite-cardinality :
    {l1 : Level} {X : UU l1} → is-prop (has-finite-cardinality X)
  is-prop-has-finite-cardinality =
    is-prop-all-elements-equal all-elements-equal-has-finite-cardinality

has-finite-cardinality-Prop :
  {l1 : Level} (X : UU l1) → UU-Prop l1
pr1 (has-finite-cardinality-Prop X) = has-finite-cardinality X
pr2 (has-finite-cardinality-Prop X) = is-prop-has-finite-cardinality
```

### A type has a finite cardinality if and only if it is finite

```agda
module _
  {l : Level} {X : UU l}
  where

  abstract
    is-finite-has-finite-cardinality : has-finite-cardinality X → is-finite X
    is-finite-has-finite-cardinality (pair k K) =
      apply-universal-property-trunc-Prop K
        ( is-finite-Prop X)
        ( is-finite-count ∘ (pair k))

  abstract
    is-finite-has-cardinality : {k : ℕ} → has-cardinality k X → is-finite X
    is-finite-has-cardinality {k} H =
      is-finite-has-finite-cardinality (pair k H)

  has-finite-cardinality-count : count X → has-finite-cardinality X
  pr1 (has-finite-cardinality-count e) = number-of-elements-count e
  pr2 (has-finite-cardinality-count e) = unit-trunc-Prop (equiv-count e)

  abstract
    has-finite-cardinality-is-finite : is-finite X → has-finite-cardinality X
    has-finite-cardinality-is-finite =
      map-universal-property-trunc-Prop
        ( has-finite-cardinality-Prop X)
        ( has-finite-cardinality-count)

  number-of-elements-is-finite : is-finite X → ℕ
  number-of-elements-is-finite =
    number-of-elements-has-finite-cardinality ∘ has-finite-cardinality-is-finite

  abstract
    mere-equiv-is-finite :
      (f : is-finite X) → mere-equiv (Fin (number-of-elements-is-finite f)) X
    mere-equiv-is-finite f =
      mere-equiv-has-finite-cardinality (has-finite-cardinality-is-finite f)

  abstract
    compute-number-of-elements-is-finite :
      (e : count X) (f : is-finite X) →
      Id (number-of-elements-count e) (number-of-elements-is-finite f)
    compute-number-of-elements-is-finite e f =
      ind-trunc-Prop
        ( λ g →
          Id-Prop ℕ-Set
            ( number-of-elements-count e)
            ( number-of-elements-is-finite g))
        ( λ g →
          ( is-injective-Fin ((inv-equiv (equiv-count g)) ∘e (equiv-count e))) ∙
          ( ap pr1
            ( eq-is-prop' is-prop-has-finite-cardinality
              ( has-finite-cardinality-count g)
              ( has-finite-cardinality-is-finite (unit-trunc-Prop g)))))
        ( f)

  has-cardinality-is-finite :
    (H : is-finite X) → has-cardinality (number-of-elements-is-finite H) X
  has-cardinality-is-finite H =
    pr2 (has-finite-cardinality-is-finite H)
```

### If a type has cardinality `k` and cardinality `l`, then `k = l`.

```agda
eq-cardinality :
  {l1 : Level} {k l : ℕ} {A : UU l1} →
  has-cardinality k A → has-cardinality l A → Id k l
eq-cardinality H K =
  apply-universal-property-trunc-Prop H
    ( Id-Prop ℕ-Set _ _)
    ( λ e →
      apply-universal-property-trunc-Prop K
        ( Id-Prop ℕ-Set _ _)
        ( λ f → is-injective-Fin (inv-equiv f ∘e e)))
```

### A finite type is empty if and only if it has 0 elements

```agda
abstract
  is-empty-is-zero-number-of-elements-is-finite :
    {l1 : Level} {X : UU l1} (f : is-finite X) →
    is-zero-ℕ (number-of-elements-is-finite f) → is-empty X
  is-empty-is-zero-number-of-elements-is-finite {l1} {X} f p =
    apply-universal-property-trunc-Prop f
      ( is-empty-Prop X)
      ( λ e →
        is-empty-is-zero-number-of-elements-count e
          ( compute-number-of-elements-is-finite e f ∙ p))
```

### A finite type is contractible if and only if it has one element

```agda
is-one-number-of-elements-is-finite-is-contr :
  {l : Level} {X : UU l} (H : is-finite X) →
  is-contr X → is-one-ℕ (number-of-elements-is-finite H)
is-one-number-of-elements-is-finite-is-contr H K =
  eq-cardinality
    ( has-cardinality-is-finite H)
    ( has-cardinality-is-contr K)

is-contr-is-one-number-of-elements-is-finite :
  {l : Level} {X : UU l} (H : is-finite X) →
  is-one-ℕ (number-of-elements-is-finite H) → is-contr X
is-contr-is-one-number-of-elements-is-finite H p =
  apply-universal-property-trunc-Prop H
    ( is-contr-Prop _)
    ( λ e →
      is-contr-equiv'
        ( Fin 1)
        ( ( equiv-count e) ∘e
          ( equiv-tr Fin
            ( inv p ∙ inv (compute-number-of-elements-is-finite e H))))
        ( is-contr-Fin-one-ℕ))

is-decidable-is-contr-is-finite :
  {l : Level} {X : UU l} (H : is-finite X) → is-decidable (is-contr X)
is-decidable-is-contr-is-finite H =
  is-decidable-iff
    ( is-contr-is-one-number-of-elements-is-finite H)
    ( is-one-number-of-elements-is-finite-is-contr H)
    ( has-decidable-equality-ℕ (number-of-elements-is-finite H) 1)
```

### The type of all pairs consisting of a natural number `k` and a type of cardinality `k` is equivalent to the type of all finite types

```agda
map-compute-total-UU-Fin : Σ ℕ UU-Fin → 𝔽
pr1 (map-compute-total-UU-Fin (pair k (pair X e))) = X
pr2 (map-compute-total-UU-Fin (pair k (pair X e))) =
  is-finite-has-finite-cardinality (pair k e)

compute-total-UU-Fin : Σ ℕ UU-Fin ≃ 𝔽
compute-total-UU-Fin =
  ( equiv-tot
    ( λ X →
      equiv-prop
        ( is-prop-has-finite-cardinality)
        ( is-prop-is-finite X)
        ( is-finite-has-finite-cardinality)
        ( has-finite-cardinality-is-finite))) ∘e
  ( equiv-left-swap-Σ)
```

### Finite types are either inhabited or empty

```agda
is-inhabited-or-empty-is-finite :
  {l1 : Level} {A : UU l1} → is-finite A → is-inhabited-or-empty A
is-inhabited-or-empty-is-finite {l1} {A} f =
  apply-universal-property-trunc-Prop f
    ( is-inhabited-or-empty-Prop A)
    ( is-inhabited-or-empty-count)
```

### If `X` is finite, then its propositional truncation is decidable

```agda
is-decidable-type-trunc-Prop-is-finite :
  {l1 : Level} {A : UU l1} → is-finite A → is-decidable (type-trunc-Prop A)
is-decidable-type-trunc-Prop-is-finite H =
  map-coprod
    ( id)
    ( map-universal-property-trunc-Prop empty-Prop)
      ( is-inhabited-or-empty-is-finite H)
```

### If a type is finite, then its propositional truncation is finite

```agda
abstract
  is-finite-type-trunc-Prop :
    {l1 : Level} {A : UU l1} → is-finite A → is-finite (type-trunc-Prop A)
  is-finite-type-trunc-Prop = functor-trunc-Prop count-type-trunc-Prop

trunc-Prop-𝔽 : 𝔽 → 𝔽
pr1 (trunc-Prop-𝔽 A) = type-trunc-Prop (type-𝔽 A)
pr2 (trunc-Prop-𝔽 A) = is-finite-type-trunc-Prop (is-finite-type-𝔽 A)
```

### We characterize the identity type of `UU-Fin-Level`

```agda
equiv-UU-Fin-Level :
  {l1 l2 : Level} {k : ℕ} → UU-Fin-Level l1 k → UU-Fin-Level l2 k → UU (l1 ⊔ l2)
equiv-UU-Fin-Level X Y = type-UU-Fin-Level X ≃ type-UU-Fin-Level Y

id-equiv-UU-Fin-Level :
  {l : Level} {k : ℕ} (X : UU-Fin-Level l k) → equiv-UU-Fin-Level X X
id-equiv-UU-Fin-Level X = id-equiv-component-UU-Level X

equiv-eq-UU-Fin-Level :
  {l : Level} {k : ℕ} {X Y : UU-Fin-Level l k} → Id X Y → equiv-UU-Fin-Level X Y
equiv-eq-UU-Fin-Level p = equiv-eq-component-UU-Level p

abstract
  is-contr-total-equiv-UU-Fin-Level :
    {l : Level} {k : ℕ} (X : UU-Fin-Level l k) →
    is-contr (Σ (UU-Fin-Level l k) (equiv-UU-Fin-Level X))
  is-contr-total-equiv-UU-Fin-Level {l} {k} X =
    is-contr-total-equiv-component-UU-Level X

abstract
  is-equiv-equiv-eq-UU-Fin-Level :
    {l : Level} {k : ℕ} (X Y : UU-Fin-Level l k) →
    is-equiv (equiv-eq-UU-Fin-Level {X = X} {Y})
  is-equiv-equiv-eq-UU-Fin-Level X =
    is-equiv-equiv-eq-component-UU-Level X

eq-equiv-UU-Fin-Level :
  {l : Level} {k : ℕ} (X Y : UU-Fin-Level l k) →
  equiv-UU-Fin-Level X Y → Id X Y
eq-equiv-UU-Fin-Level X Y =
  eq-equiv-component-UU-Level X Y

equiv-equiv-eq-UU-Fin-Level :
  {l : Level} {k : ℕ} (X Y : UU-Fin-Level l k) →
  Id X Y ≃ equiv-UU-Fin-Level X Y
pr1 (equiv-equiv-eq-UU-Fin-Level X Y) = equiv-eq-UU-Fin-Level
pr2 (equiv-equiv-eq-UU-Fin-Level X Y) = is-equiv-equiv-eq-UU-Fin-Level X Y
```

### We characterize the identity type of `UU-Fin`

```agda
equiv-UU-Fin : {k : ℕ} (X Y : UU-Fin k) → UU lzero
equiv-UU-Fin X Y = equiv-component-UU X Y

id-equiv-UU-Fin :
  {k : ℕ} (X : UU-Fin k) → equiv-UU-Fin X X
id-equiv-UU-Fin X = id-equiv-component-UU X

equiv-eq-UU-Fin :
  {k : ℕ} {X Y : UU-Fin k} → Id X Y → equiv-UU-Fin X Y
equiv-eq-UU-Fin p = equiv-eq-component-UU p

abstract
  is-contr-total-equiv-UU-Fin :
    {k : ℕ} (X : UU-Fin k) → is-contr (Σ (UU-Fin k) (equiv-UU-Fin X))
  is-contr-total-equiv-UU-Fin X =
    is-contr-total-equiv-component-UU X

abstract
  is-equiv-equiv-eq-UU-Fin :
    {k : ℕ} (X Y : UU-Fin k) → is-equiv (equiv-eq-UU-Fin {X = X} {Y})
  is-equiv-equiv-eq-UU-Fin X =
    is-equiv-equiv-eq-component-UU X

eq-equiv-UU-Fin :
  {k : ℕ} (X Y : UU-Fin k) → equiv-UU-Fin X Y → Id X Y
eq-equiv-UU-Fin X Y = eq-equiv-component-UU X Y

equiv-equiv-eq-UU-Fin :
  {k : ℕ} (X Y : UU-Fin k) → Id X Y ≃ equiv-UU-Fin X Y
pr1 (equiv-equiv-eq-UU-Fin X Y) = equiv-eq-UU-Fin
pr2 (equiv-equiv-eq-UU-Fin X Y) = is-equiv-equiv-eq-UU-Fin X Y
```

### The types `UU-Fin-Level` and `UU-Fin` are connected

```agda
abstract
  is-path-connected-UU-Fin-Level :
    {l : Level} (n : ℕ) → is-path-connected (UU-Fin-Level l n)
  is-path-connected-UU-Fin-Level {l} n =
    is-path-connected-mere-eq
      ( Fin-UU-Fin-Level l n)
      ( λ A →
        functor-trunc-Prop
          ( ( eq-equiv-UU-Fin-Level (Fin-UU-Fin-Level l n) A) ∘
            ( map-equiv
              ( equiv-precomp-equiv
                ( inv-equiv (equiv-raise l (Fin n)))
                ( type-UU-Fin-Level A))))
          ( pr2 A))

abstract
  is-path-connected-UU-Fin :
    (n : ℕ) → is-path-connected (UU-Fin n)
  is-path-connected-UU-Fin n =
    is-path-connected-mere-eq
      ( Fin-UU-Fin n)
      ( λ A → functor-trunc-Prop (eq-equiv-UU-Fin (Fin-UU-Fin n) A) (pr2 A))
```

```agda
  equiv-has-cardinality-id-number-of-elements-is-finite :
    {l : Level} (X : UU l) ( H : is-finite X) (n : ℕ) →
    ( has-cardinality n X ≃ Id (number-of-elements-is-finite H) n)
  pr1 (equiv-has-cardinality-id-number-of-elements-is-finite X H n) Q =
    ap
      ( number-of-elements-has-finite-cardinality)
      ( all-elements-equal-has-finite-cardinality
        ( has-finite-cardinality-is-finite H)
        ( pair n Q))
  pr2 (equiv-has-cardinality-id-number-of-elements-is-finite X H n) =
    is-equiv-is-prop
      ( is-prop-type-trunc-Prop)
      ( is-set-ℕ (number-of-elements-is-finite H) n)
      ( λ p →
        tr ( λ m → has-cardinality m X)
           ( p)
           ( pr2 (has-finite-cardinality-is-finite H)))
```
