# Induction principles on W-types

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.induction-w-types where

open import elementary-number-theory.natural-numbers using (ℕ; zero-ℕ; succ-ℕ)

open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.elementhood-relation-w-types using (_∈-𝕎_)
open import foundation.equivalences using (_≃_; id-equiv; is-equiv)
open import foundation.fibers-of-maps using (fib)
open import foundation.functions using (_∘_)
open import foundation.function-extensionality using (eq-htpy)
open import foundation.identity-types using (Id; ap; refl; tr)
open import foundation.inequality-w-types using
  ( _le-𝕎_; le-∈-𝕎; propagate-le-𝕎)
open import foundation.negation using (¬)
open import foundation.universe-levels using (Level; UU; _⊔_)
open import foundation.w-types using (𝕎; component-𝕎; tree-𝕎)
```

## Idea

There are several induction principles on W-types, besided the induction principle that each W-type comes equipped with by definition. The first is an induction principle formulated with respect to the elementhood relation on W-types. The second is a strong induction principle, analogous to the strong induction principle for the natural numbers.

## Properties

### Induction principle with respect to the elementhood relation

```agda
module _
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2}
  where

  □-∈-𝕎 : (𝕎 A B → UU l3) → (𝕎 A B → UU (l1 ⊔ l2 ⊔ l3))
  □-∈-𝕎 P x = (y : 𝕎 A B) → (y ∈-𝕎 x) → P y

  η-□-∈-𝕎 :
    (P : 𝕎 A B → UU l3) → ((x : 𝕎 A B) → P x) → ((x : 𝕎 A B) → □-∈-𝕎 P x)
  η-□-∈-𝕎 P f x y e = f y

  ε-□-∈-𝕎 :
    (P : 𝕎 A B → UU l3) (h : (y : 𝕎 A B) → □-∈-𝕎 P y → P y) →
    ((x : 𝕎 A B) → □-∈-𝕎 P x) → (x : 𝕎 A B) → P x
  ε-□-∈-𝕎 P h f x = h x (f x)

  ind-□-∈-𝕎 :
    (P : 𝕎 A B → UU l3) (h : (y : 𝕎 A B) → □-∈-𝕎 P y → P y) →
    (x : 𝕎 A B) → □-∈-𝕎 P x
  ind-□-∈-𝕎 P h (tree-𝕎 x α) .(α b) (pair b refl) =
    h (α b) (ind-□-∈-𝕎 P h (α b))

  comp-□-∈-𝕎 :
    (P : 𝕎 A B → UU l3) (h : (y : 𝕎 A B) → □-∈-𝕎 P y → P y) →
    (x y : 𝕎 A B) (e : y ∈-𝕎 x) →
    Id (ind-□-∈-𝕎 P h x y e) (h y (ind-□-∈-𝕎 P h y))
  comp-□-∈-𝕎 P h (tree-𝕎 x α) .(α b) (pair b refl) = refl
  
  ind-∈-𝕎 :
    (P : 𝕎 A B → UU l3) (h : (y : 𝕎 A B) → □-∈-𝕎 P y → P y) →
    (x : 𝕎 A B) → P x
  ind-∈-𝕎 P h = ε-□-∈-𝕎 P h (ind-□-∈-𝕎 P h)

  comp-∈-𝕎 :
    (P : 𝕎 A B → UU l3) (h : (y : 𝕎 A B) → □-∈-𝕎 P y → P y) →
    (x : 𝕎 A B) → Id (ind-∈-𝕎 P h x) (h x (λ y e → ind-∈-𝕎 P h y))
  comp-∈-𝕎 P h x =
    ap (h x) (eq-htpy (λ y → eq-htpy (λ e → comp-□-∈-𝕎 P h x y e)))
```

### Strong induction for W-types

#### We define an operation □-𝕎 that acts on families over 𝕎 A B

```agda
module _
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2} (P : 𝕎 A B → UU l3)
  where

  □-𝕎 : 𝕎 A B → UU (l1 ⊔ l2 ⊔ l3)
  □-𝕎 x = (y : 𝕎 A B) → (y le-𝕎 x) → P y
```

#### The unit of □-𝕎 takes sections of P to sections of □-𝕎 P

```agda
module _
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2} {P : 𝕎 A B → UU l3}
  where

  unit-□-𝕎 : ((x : 𝕎 A B) → P x) → ((x : 𝕎 A B) → □-𝕎 P x)
  unit-□-𝕎 f x y p = f y
```

#### The reflector (counit) of □-𝕎 is dual, with an extra hypothesis

```agda
module _
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2} {P : 𝕎 A B → UU l3}
  where

  reflect-□-𝕎 :
    ((x : 𝕎 A B) → □-𝕎 P x → P x) →
    ((x : 𝕎 A B) → □-𝕎 P x) → ((x : 𝕎 A B) → P x)
  reflect-□-𝕎 h f x = h x (f x)
```

#### The strong induction principle for W-types

We first prove an intermediate induction principle with computation rule, where we obtain sections of □-𝕎 P.

```agda
  □-strong-ind-𝕎 :
    ((x : 𝕎 A B) → □-𝕎 P x → P x) → (x : 𝕎 A B) → □-𝕎 P x
  □-strong-ind-𝕎 h (tree-𝕎 x α) .(α b) (le-∈-𝕎 (pair b refl)) =
    h (α b) (□-strong-ind-𝕎 h (α b))
  □-strong-ind-𝕎 h (tree-𝕎 x α) y (propagate-le-𝕎 (pair b refl) K) =
    □-strong-ind-𝕎 h (α b) y K

  □-strong-comp-𝕎 :
    (h : (x : 𝕎 A B) → □-𝕎 P x → P x)
    (x : 𝕎 A B) (y : 𝕎 A B) (p : y le-𝕎 x) →
    Id (□-strong-ind-𝕎 h x y p) (h y (□-strong-ind-𝕎 h y))
  □-strong-comp-𝕎 h (tree-𝕎 x α) .(α b) (le-∈-𝕎 (pair b refl)) =
    refl
  □-strong-comp-𝕎 h (tree-𝕎 x α) y (propagate-le-𝕎 (pair b refl) K) =
    □-strong-comp-𝕎 h (α b) y K
```

Now we prove the actual induction principle with computation rule, where we obtain sections of P.

```agda
strong-ind-𝕎 :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2} (P : 𝕎 A B → UU l3) → 
  ((x : 𝕎 A B) → □-𝕎 P x → P x) → (x : 𝕎 A B) → P x
strong-ind-𝕎 P h = reflect-□-𝕎 h (□-strong-ind-𝕎 h)
                                               
strong-comp-𝕎 :
  {l1 l2 l3 : Level} {A : UU l1} {B : A → UU l2} (P : 𝕎 A B → UU l3) →
  (h : (x : 𝕎 A B) → □-𝕎 P x → P x) (x : 𝕎 A B) →
  Id (strong-ind-𝕎 P h x) (h x (unit-□-𝕎 (strong-ind-𝕎 P h) x))
strong-comp-𝕎 P h x =
  ap (h x) (eq-htpy (λ y → eq-htpy (λ p → □-strong-comp-𝕎 h x y p)))
```

### There are no infinitely descending sequences in a W-types

```agda
no-infinite-descent-𝕎 :
  {l1 l2 : Level} {A : UU l1} {B : A → UU l2} →
  (f : ℕ → 𝕎 A B) → ¬ ((n : ℕ) → (f (succ-ℕ n) le-𝕎 (f n)))
no-infinite-descent-𝕎 {A = A} {B} f =
  strong-ind-𝕎
    ( λ x → (f : ℕ → 𝕎 A B) (p : Id (f zero-ℕ) x) →
            ¬ ((n : ℕ) → (f (succ-ℕ n)) le-𝕎 (f n)))
    ( λ x IH f p H →
      IH ( f 1)
         ( tr (λ t → (f 1) le-𝕎 t) p (H zero-ℕ))
         ( f ∘ succ-ℕ)
         ( refl)
         ( λ n → H (succ-ℕ n)))
    ( f zero-ℕ)
    ( f)
    ( refl)
```
