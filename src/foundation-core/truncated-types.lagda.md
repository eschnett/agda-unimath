# Truncated types

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation-core.truncated-types where

open import foundation-core.cartesian-product-types using (_×_)
open import foundation-core.contractible-types using
  ( is-contr; eq-is-contr; is-contr-is-equiv; is-contr-retract-of;
    is-contr-Σ'; is-contr-left-factor-prod; is-contr-right-factor-prod)
open import foundation-core.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation-core.embeddings using
  ( is-emb; _↪_; map-emb; is-emb-map-emb)
open import foundation-core.equality-cartesian-product-types using
  ( Eq-prod; equiv-pair-eq)
open import foundation-core.equality-dependent-pair-types using
  ( equiv-pair-eq-Σ)
open import foundation-core.equivalences using
  ( is-equiv; _≃_; map-inv-is-equiv; is-equiv-map-inv-is-equiv)
open import foundation-core.identity-types using (Id; refl; left-inv; ap; tr)
open import foundation-core.retractions using (_retract-of_; retract-eq)
open import foundation-core.truncation-levels using (𝕋; neg-two-𝕋; succ-𝕋)
open import foundation-core.universe-levels using (Level; UU; lsuc; _⊔_)
```

## Idea

The truncatedness of a type is a measure of the complexity of its identity types. The simplest case is a contractible type. This is the base case of the inductive definition of truncatedness for types. A type is (k+1)-truncated if its identity types are k-truncated.

## Definition

### The condition of truncatedness

```agda
is-trunc : {i : Level} (k : 𝕋) → UU i → UU i
is-trunc neg-two-𝕋 A = is-contr A
is-trunc (succ-𝕋 k) A = (x y : A) → is-trunc k (Id x y)
```

### The universe of truncated types

```agda
Truncated-Type : (l : Level) → 𝕋 → UU (lsuc l)
Truncated-Type l k = Σ (UU l) (is-trunc k)

module _
  {k : 𝕋} {l : Level}
  where
  
  type-Truncated-Type : Truncated-Type l k → UU l
  type-Truncated-Type = pr1

  abstract
    is-trunc-type-Truncated-Type :
      (A : Truncated-Type l k) → is-trunc k (type-Truncated-Type A)
    is-trunc-type-Truncated-Type = pr2
```

## Properties

### If a type is k-truncated, then it is (k+1)-truncated.

```agda
abstract
  is-trunc-succ-is-trunc :
    (k : 𝕋) {i : Level} {A : UU i} → is-trunc k A → is-trunc (succ-𝕋 k) A
  pr1 (is-trunc-succ-is-trunc neg-two-𝕋 H x y) = eq-is-contr H
  pr2 (is-trunc-succ-is-trunc neg-two-𝕋 H x .x) refl = left-inv (pr2 H x)
  is-trunc-succ-is-trunc (succ-𝕋 k) H x y = is-trunc-succ-is-trunc k (H x y)

truncated-type-succ-Truncated-Type :
  (k : 𝕋) {l : Level} → Truncated-Type l k → Truncated-Type l (succ-𝕋 k)
pr1 (truncated-type-succ-Truncated-Type k A) = type-Truncated-Type A
pr2 (truncated-type-succ-Truncated-Type k A) =
  is-trunc-succ-is-trunc k (is-trunc-type-Truncated-Type A)
```

### The identity type of a k-truncated type is k-truncated

```agda
abstract
  is-trunc-Id :
    {l : Level} {k : 𝕋} {A : UU l} →
    is-trunc k A → (x y : A) → is-trunc k (Id x y)
  is-trunc-Id {l} {k}= is-trunc-succ-is-trunc k

Id-Truncated-Type :
  {l : Level} {k : 𝕋} (A : Truncated-Type l (succ-𝕋 k)) →
  (x y : type-Truncated-Type A) → Truncated-Type l k
pr1 (Id-Truncated-Type A x y) = Id x y
pr2 (Id-Truncated-Type A x y) = is-trunc-type-Truncated-Type A x y

Id-Truncated-Type' :
  {l : Level} {k : 𝕋} (A : Truncated-Type l k) →
  (x y : type-Truncated-Type A) → Truncated-Type l k
pr1 (Id-Truncated-Type' A x y) = Id x y
pr2 (Id-Truncated-Type' A x y) =
  is-trunc-Id (is-trunc-type-Truncated-Type A) x y
```

### k-truncated types are closed under retracts

```agda
module _
  {l1 l2 : Level}
  where

  is-trunc-retract-of :
    {k : 𝕋} {A : UU l1} {B : UU l2} →
    A retract-of B → is-trunc k B → is-trunc k A
  is-trunc-retract-of {neg-two-𝕋} = is-contr-retract-of _
  is-trunc-retract-of {succ-𝕋 k} R H x y =
    is-trunc-retract-of (retract-eq R x y) (H (pr1 R x) (pr1 R y))
```

### k-truncated types are closed under equivalences

```agda
abstract
  is-trunc-is-equiv :
    {i j : Level} (k : 𝕋) {A : UU i} (B : UU j) (f : A → B) → is-equiv f →
    is-trunc k B → is-trunc k A
  is-trunc-is-equiv k B f is-equiv-f =
    is-trunc-retract-of (pair f (pr2 is-equiv-f))

abstract
  is-trunc-equiv :
    {i j : Level} (k : 𝕋) {A : UU i} (B : UU  j) (e : A ≃ B) →
    is-trunc k B → is-trunc k A
  is-trunc-equiv k B (pair f is-equiv-f) =
    is-trunc-is-equiv k B f is-equiv-f

abstract
  is-trunc-is-equiv' :
    {i j : Level} (k : 𝕋) (A : UU i) {B : UU j} (f : A → B) →
    is-equiv f → is-trunc k A → is-trunc k B
  is-trunc-is-equiv' k A  f is-equiv-f is-trunc-A =
    is-trunc-is-equiv k A
      ( map-inv-is-equiv is-equiv-f)
      ( is-equiv-map-inv-is-equiv is-equiv-f)
      ( is-trunc-A)

abstract
  is-trunc-equiv' :
    {i j : Level} (k : 𝕋) (A : UU i) {B : UU j} (e : A ≃ B) →
    is-trunc k A → is-trunc k B
  is-trunc-equiv' k A (pair f is-equiv-f) =
    is-trunc-is-equiv' k A f is-equiv-f

```

### If a type embeds into a (k+1)-truncated type, then it is (k+1)-truncated

```agda
abstract
  is-trunc-is-emb :
    {i j : Level} (k : 𝕋) {A : UU i} {B : UU j} (f : A → B) →
    is-emb f → is-trunc (succ-𝕋 k) B → is-trunc (succ-𝕋 k) A
  is-trunc-is-emb k f Ef H x y =
    is-trunc-is-equiv k (Id (f x) (f y)) (ap f {x} {y}) (Ef x y) (H (f x) (f y))

abstract
  is-trunc-emb :
    {i j : Level} (k : 𝕋) {A : UU i} {B : UU j} (f : A ↪ B) →
    is-trunc (succ-𝕋 k) B → is-trunc (succ-𝕋 k) A
  is-trunc-emb k f = is-trunc-is-emb k (map-emb f) (is-emb-map-emb f)
```

### Truncated types are closed under dependent pair types

```agda
abstract
  is-trunc-Σ :
    {l1 l2 : Level} {k : 𝕋} {A : UU l1} {B : A → UU l2} →
    is-trunc k A → ((x : A) → is-trunc k (B x)) → is-trunc k (Σ A B)
  is-trunc-Σ {k = neg-two-𝕋} is-trunc-A is-trunc-B =
    is-contr-Σ' is-trunc-A is-trunc-B
  is-trunc-Σ {k = succ-𝕋 k} {B = B} is-trunc-A is-trunc-B s t =
    is-trunc-equiv k
      ( Σ (Id (pr1 s) (pr1 t)) (λ p → Id (tr B p (pr2 s)) (pr2 t)))
      ( equiv-pair-eq-Σ s t)
      ( is-trunc-Σ
        ( is-trunc-A (pr1 s) (pr1 t))
        ( λ p → is-trunc-B (pr1 t) (tr B p (pr2 s)) (pr2 t)))

Σ-Truncated-Type :
  {l1 l2 : Level} {k : 𝕋} (A : Truncated-Type l1 k)
  (B : type-Truncated-Type A → Truncated-Type l2 k) →
  Truncated-Type (l1 ⊔ l2) k
pr1 (Σ-Truncated-Type A B) =
  Σ (type-Truncated-Type A) (λ a → type-Truncated-Type (B a))
pr2 (Σ-Truncated-Type A B) =
  is-trunc-Σ
    ( is-trunc-type-Truncated-Type A)
    ( λ a → is-trunc-type-Truncated-Type (B a))

fib-Truncated-Type :
  {l1 l2 : Level} {k : 𝕋} (A : Truncated-Type l1 k)
  (B : Truncated-Type l2 k)
  (f : type-Truncated-Type A → type-Truncated-Type B) →
  type-Truncated-Type B → Truncated-Type (l1 ⊔ l2) k
fib-Truncated-Type A B f b =
  Σ-Truncated-Type A (λ a → Id-Truncated-Type' B (f a) b)
```

### Products of truncated types are truncated

```agda
abstract
  is-trunc-prod :
    {l1 l2 : Level} (k : 𝕋) {A : UU l1} {B : UU l2} →
    is-trunc k A → is-trunc k B → is-trunc k (A × B)
  is-trunc-prod k is-trunc-A is-trunc-B =
    is-trunc-Σ is-trunc-A (λ x → is-trunc-B)

is-trunc-prod' :
  {l1 l2 : Level} (k : 𝕋) {A : UU l1} {B : UU l2} →
  (B → is-trunc (succ-𝕋 k) A) → (A → is-trunc (succ-𝕋 k) B) →
  is-trunc (succ-𝕋 k) (A × B)
is-trunc-prod' k f g (pair a b) (pair a' b') =
  is-trunc-equiv k
    ( Eq-prod (pair a b) (pair a' b'))
    ( equiv-pair-eq (pair a b) (pair a' b'))
    ( is-trunc-prod k (f b a a') (g a b b'))

is-trunc-left-factor-prod :
  {l1 l2 : Level} (k : 𝕋) {A : UU l1} {B : UU l2} →
  is-trunc k (A × B) → B → is-trunc k A
is-trunc-left-factor-prod neg-two-𝕋 {A} {B} H b =
  is-contr-left-factor-prod A B H
is-trunc-left-factor-prod (succ-𝕋 k) H b a a' =
  is-trunc-left-factor-prod k {A = Id a a'} {B = Id b b}
    ( is-trunc-equiv' k
      ( Id (pair a b) (pair a' b))
      ( equiv-pair-eq (pair a b) (pair a' b))
      ( H (pair a b) (pair a' b)))
    ( refl)

is-trunc-right-factor-prod :
  {l1 l2 : Level} (k : 𝕋) {A : UU l1} {B : UU l2} →
  is-trunc k (A × B) → A → is-trunc k B
is-trunc-right-factor-prod neg-two-𝕋 {A} {B} H a =
  is-contr-right-factor-prod A B H
is-trunc-right-factor-prod (succ-𝕋 k) {A} {B} H a b b' =
  is-trunc-right-factor-prod k {A = Id a a} {B = Id b b'}
    ( is-trunc-equiv' k
      ( Id (pair a b) (pair a b'))
      ( equiv-pair-eq (pair a b) (pair a b'))
      ( H (pair a b) (pair a b')))
    ( refl)
```
