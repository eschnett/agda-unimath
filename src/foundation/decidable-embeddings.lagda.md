# Decidable embeddings

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.decidable-embeddings where

open import foundation.cartesian-product-types using (_×_)
open import foundation.coproduct-types using (coprod; inl; inr; ind-coprod)
open import foundation.contractible-maps using (is-contr-map-is-equiv)
open import foundation.contractible-types using (center; is-contr)
open import foundation.decidable-maps using (is-decidable-map)
open import foundation.decidable-propositions using
  ( is-decidable-prop; is-prop-is-decidable-prop; decidable-Prop)
open import foundation.decidable-subtypes using (decidable-subtype)
open import foundation.decidable-types using
  ( is-prop-is-decidable; is-decidable; is-decidable-equiv)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import
  foundation.distributivity-of-dependent-functions-over-dependent-pairs
  using
  ( inv-distributive-Π-Σ)
open import foundation.embeddings using
  ( is-emb; _↪_; is-emb-id; is-prop-is-emb; is-emb-comp'; is-emb-htpy)
open import foundation.empty-types using (ex-falso; is-emb-ex-falso)
open import foundation.equivalences using
  ( _≃_; _∘e_; id-equiv; is-equiv; is-emb-is-equiv; map-inv-is-equiv;
    equiv-precomp; map-equiv; issec-map-inv-equiv; is-equiv-map-inv-equiv)
open import foundation.fibers-of-maps using (fib; fib-comp)
open import foundation.functions using (id; _∘_)
open import foundation.functoriality-cartesian-product-types using
  ( equiv-prod)
open import foundation.functoriality-dependent-pair-types using
  ( equiv-tot; equiv-Σ)
open import foundation.fundamental-theorem-of-identity-types using
  ( fundamental-theorem-id)
open import foundation.homotopies using (_~_; refl-htpy; is-contr-total-htpy)
open import foundation.identity-types using (Id; refl; equiv-concat; inv; ap)
open import foundation.propositional-maps using
  ( is-prop-map; is-emb-is-prop-map; equiv-is-prop-map-is-emb;
    is-prop-map-is-emb)
open import foundation.propositions using
  ( is-prop; is-prop-Π; is-prop-is-inhabited; is-prop-prod;
    is-proof-irrelevant-is-prop; equiv-prop)
open import foundation.slice using (equiv-Fib-structure)
open import foundation.subtype-identity-principle using
  ( is-contr-total-Eq-subtype)
open import foundation.type-arithmetic-dependent-pair-types using
  ( left-unit-law-Σ-is-contr)
open import foundation.universe-levels using (Level; UU; _⊔_)
```

## Idea

A map is said to be a decidable embedding if it is an embedding and its fibers are decidable types.

## Definitions

### The condition on a map of being a decidable embedding

```agda
is-decidable-emb :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} → (X → Y) → UU (l1 ⊔ l2)
is-decidable-emb {Y = Y} f = is-emb f × is-decidable-map f

abstract
  is-emb-is-decidable-emb :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} {f : X → Y} →
    is-decidable-emb f → is-emb f
  is-emb-is-decidable-emb H = pr1 H

is-decidable-map-is-decidable-emb :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} {f : X → Y} →
  is-decidable-emb f → is-decidable-map f
is-decidable-map-is-decidable-emb H = pr2 H
```

### Decidably propositional maps

```
is-decidable-prop-map :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} → (X → Y) → UU (l1 ⊔ l2)
is-decidable-prop-map {Y = Y} f = (y : Y) → is-decidable-prop (fib f y)

abstract
  is-prop-map-is-decidable-prop-map :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} {f : X → Y} →
    is-decidable-prop-map f → is-prop-map f
  is-prop-map-is-decidable-prop-map H y = pr1 (H y)

is-decidable-map-is-decidable-prop-map :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} {f : X → Y} →
  is-decidable-prop-map f → is-decidable-map f
is-decidable-map-is-decidable-prop-map H y = pr2 (H y)
```

### The type of decidable embeddings

```agda
_↪d_ :
  {l1 l2 : Level} (X : UU l1) (Y : UU l2) → UU (l1 ⊔ l2)
X ↪d Y = Σ (X → Y) is-decidable-emb

map-decidable-emb :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} → X ↪d Y → X → Y
map-decidable-emb e = pr1 e

abstract
  is-decidable-emb-map-decidable-emb :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} (e : X ↪d Y) →
    is-decidable-emb (map-decidable-emb e)
  is-decidable-emb-map-decidable-emb e = pr2 e

abstract
  is-emb-map-decidable-emb :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} (e : X ↪d Y) →
    is-emb (map-decidable-emb e)
  is-emb-map-decidable-emb e =
    is-emb-is-decidable-emb (is-decidable-emb-map-decidable-emb e)

abstract
  is-decidable-map-map-decidable-emb :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} (e : X ↪d Y) →
    is-decidable-map (map-decidable-emb e)
  is-decidable-map-map-decidable-emb e =
    is-decidable-map-is-decidable-emb (is-decidable-emb-map-decidable-emb e)

emb-decidable-emb :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} → X ↪d Y → X ↪ Y
pr1 (emb-decidable-emb e) = map-decidable-emb e
pr2 (emb-decidable-emb e) = is-emb-map-decidable-emb e
```

## Properties

### Being a decidably propositional map is a proposition

```agda
abstract
  is-prop-is-decidable-prop-map :
    {l1 l2 : Level} {X : UU l1} {Y : UU l2} (f : X → Y) →
    is-prop (is-decidable-prop-map f)
  is-prop-is-decidable-prop-map f =
    is-prop-Π (λ y → is-prop-is-decidable-prop (fib f y))
```

### Any map of which the fibers are decidable propositions is a decidable embedding

```agda
module _
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} {f : X → Y}
  where
  
  abstract
    is-decidable-emb-is-decidable-prop-map :
      is-decidable-prop-map f → is-decidable-emb f
    pr1 (is-decidable-emb-is-decidable-prop-map H) =
      is-emb-is-prop-map (is-prop-map-is-decidable-prop-map H)
    pr2 (is-decidable-emb-is-decidable-prop-map H) =
      is-decidable-map-is-decidable-prop-map H

  abstract
    is-prop-map-is-decidable-emb : is-decidable-emb f → is-prop-map f
    is-prop-map-is-decidable-emb H =
      is-prop-map-is-emb (is-emb-is-decidable-emb H)

  abstract
    is-decidable-prop-map-is-decidable-emb :
      is-decidable-emb f → is-decidable-prop-map f
    pr1 (is-decidable-prop-map-is-decidable-emb H y) =
      is-prop-map-is-decidable-emb H y
    pr2 (is-decidable-prop-map-is-decidable-emb H y) = pr2 H y

decidable-subtype-decidable-emb :
  {l1 l2 : Level} {X : UU l1} {Y : UU l2} →
  (X ↪d Y) → (decidable-subtype (l1 ⊔ l2) Y)
pr1 (decidable-subtype-decidable-emb f y) = fib (map-decidable-emb f) y
pr2 (decidable-subtype-decidable-emb f y) =
  is-decidable-prop-map-is-decidable-emb (pr2 f) y
```

### The type of all decidable embeddings into a type `A` is equivalent to the type of decidable subtypes of `A`

```agda
equiv-Fib-decidable-Prop :
  (l : Level) {l1 : Level} (A : UU l1) →
  Σ (UU (l1 ⊔ l)) (λ X → X ↪d A) ≃ (decidable-subtype (l1 ⊔ l) A)
equiv-Fib-decidable-Prop l A =
  ( equiv-Fib-structure l is-decidable-prop A) ∘e
  ( equiv-tot
    ( λ X →
      equiv-tot
        ( λ f →
          ( inv-distributive-Π-Σ) ∘e
          ( equiv-prod (equiv-is-prop-map-is-emb f) id-equiv))))
```

### Any equivalence is a decidable embedding

```agda
abstract
  is-decidable-emb-is-equiv :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} {f : A → B} →
    is-equiv f → is-decidable-emb f
  pr1 (is-decidable-emb-is-equiv H) = is-emb-is-equiv H
  pr2 (is-decidable-emb-is-equiv H) x = inl (center (is-contr-map-is-equiv H x))

abstract
  is-decidable-emb-id :
    {l1 : Level} {A : UU l1} → is-decidable-emb (id {A = A})
  pr1 (is-decidable-emb-id {l1} {A}) = is-emb-id
  pr2 (is-decidable-emb-id {l1} {A}) x = inl (pair x refl)

decidable-emb-id :
  {l1 : Level} {A : UU l1} → A ↪d A
pr1 (decidable-emb-id {l1} {A}) = id
pr2 (decidable-emb-id {l1} {A}) = is-decidable-emb-id
```

### Being a decidable embedding is a property

```agda
abstract
  is-prop-is-decidable-emb :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} (f : A → B) →
    is-prop (is-decidable-emb f)
  is-prop-is-decidable-emb f =
    is-prop-is-inhabited
      ( λ H →
        is-prop-prod
          ( is-prop-is-emb f)
          ( is-prop-Π
            ( λ y → is-prop-is-decidable (is-prop-map-is-emb (pr1 H) y))))
```

### Decidable embeddings are closed under composition

```agda
abstract
  is-decidable-emb-comp :
    {l1 l2 l3 : Level} {A : UU l1} {B : UU l2} {C : UU l3} {g : B → C}
    {f : A → B} →
    is-decidable-emb f → is-decidable-emb g → is-decidable-emb (g ∘ f)
  pr1 (is-decidable-emb-comp {g = g} {f} H K) =
    is-emb-comp' _ _ (pr1 K) (pr1 H)
  pr2 (is-decidable-emb-comp {g = g} {f} H K) x =
    ind-coprod
      ( λ t → is-decidable (fib (g ∘ f) x))
      ( λ u →
        is-decidable-equiv
          ( fib-comp g f x)
          ( is-decidable-equiv
          ( left-unit-law-Σ-is-contr
            ( is-proof-irrelevant-is-prop
              ( is-prop-map-is-emb (is-emb-is-decidable-emb K) x)
                ( u))
                ( u))
              ( is-decidable-map-is-decidable-emb H (pr1 u))))
      ( λ α → inr (λ t → α (pair (f (pr1 t)) (pr2 t))))
      ( pr2 K x)
```

### Decidable embeddings are closed under homotopies

```agda
abstract
  is-decidable-emb-htpy :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} {f g : A → B} →
    f ~ g → is-decidable-emb g → is-decidable-emb f
  pr1 (is-decidable-emb-htpy {f = f} {g} H K) =
    is-emb-htpy f g H (is-emb-is-decidable-emb K)
  pr2 (is-decidable-emb-htpy {f = f} {g} H K) b =
    is-decidable-equiv
      ( equiv-tot (λ a → equiv-concat (inv (H a)) b))
      ( is-decidable-map-is-decidable-emb K b)
```

### Characterizing equality in the type of decidable embeddings

```agda
htpy-decidable-emb :
  {l1 l2 : Level} {A : UU l1} {B : UU l2} (f g : A ↪d B) → UU (l1 ⊔ l2)
htpy-decidable-emb f g = map-decidable-emb f ~ map-decidable-emb g

refl-htpy-decidable-emb :
  {l1 l2 : Level} {A : UU l1} {B : UU l2} (f : A ↪d B) → htpy-decidable-emb f f
refl-htpy-decidable-emb f = refl-htpy

htpy-eq-decidable-emb :
  {l1 l2 : Level} {A : UU l1} {B : UU l2} (f g : A ↪d B) →
  Id f g → htpy-decidable-emb f g
htpy-eq-decidable-emb f .f refl = refl-htpy-decidable-emb f

abstract
  is-contr-total-htpy-decidable-emb :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} (f : A ↪d B) →
    is-contr (Σ (A ↪d B) (htpy-decidable-emb f))
  is-contr-total-htpy-decidable-emb f =
    is-contr-total-Eq-subtype
      ( is-contr-total-htpy (map-decidable-emb f))
      ( is-prop-is-decidable-emb)
      ( map-decidable-emb f)
      ( refl-htpy)
      ( is-decidable-emb-map-decidable-emb f)

abstract
  is-equiv-htpy-eq-decidable-emb :
    {l1 l2 : Level} {A : UU l1} {B : UU l2} (f g : A ↪d B) →
    is-equiv (htpy-eq-decidable-emb f g)
  is-equiv-htpy-eq-decidable-emb f =
    fundamental-theorem-id f
      ( refl-htpy-decidable-emb f)
      ( is-contr-total-htpy-decidable-emb f)
      ( htpy-eq-decidable-emb f)

eq-htpy-decidable-emb :
  {l1 l2 : Level} {A : UU l1} {B : UU l2} {f g : A ↪d B} →
  htpy-decidable-emb f g → Id f g
eq-htpy-decidable-emb {f = f} {g} =
  map-inv-is-equiv (is-equiv-htpy-eq-decidable-emb f g)
```

### Precomposing decidable embeddings with equivalences

```agda
equiv-precomp-decidable-emb-equiv :
  {l1 l2 l3 : Level} {A : UU l1} {B : UU l2} (e : A ≃ B) →
  (C : UU l3) → (B ↪d C) ≃ (A ↪d C)
equiv-precomp-decidable-emb-equiv e C =
  equiv-Σ
    ( is-decidable-emb)
    ( equiv-precomp e C)
    ( λ g →
      equiv-prop
        ( is-prop-is-decidable-emb g)
        ( is-prop-is-decidable-emb (g ∘ map-equiv e))
        ( is-decidable-emb-comp (is-decidable-emb-is-equiv (pr2 e)))
        ( λ d →
          is-decidable-emb-htpy
            ( λ b → ap g (inv (issec-map-inv-equiv e b)))
            ( is-decidable-emb-comp
              ( is-decidable-emb-is-equiv (is-equiv-map-inv-equiv e))
              ( d))))
```

### Any map out of the empty type is a decidable embedding

```agda
abstract
  is-decidable-emb-ex-falso :
    {l : Level} {X : UU l} → is-decidable-emb (ex-falso {l} {X})
  pr1 (is-decidable-emb-ex-falso {l} {X}) = is-emb-ex-falso
  pr2 (is-decidable-emb-ex-falso {l} {X}) x = inr pr1
```
