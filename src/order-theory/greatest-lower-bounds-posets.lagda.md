# Greatest lower bounds in posets

```agda
{-# OPTIONS --without-K --exact-split #-}

module order-theory.greatest-lower-bounds-posets where

open import foundation.cartesian-product-types using (_×_)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.propositions using
  ( UU-Prop; is-prop; type-Prop; is-prop-type-Prop; all-elements-equal;
    is-prop-all-elements-equal; prod-Prop; Π-Prop; function-Prop)
open import foundation.subtypes using (eq-subtype)
open import foundation.universe-levels using (Level; UU; _⊔_)

open import order-theory.posets using
  ( Poset; element-Poset; leq-poset-Prop; antisymmetric-leq-Poset)
```

## Idea

A lower bound of two elements `x` and `y` in a poset `P` is an element `z` such that both `z ≤ x` and `z ≤ y` hold. A greatest lower bound of `x` and `y` is a lower bound `z` of `x` and `y` such that `w ≤ z` holds for any lower bound of `x` and `y`.

## Definitions

### Lower bounds of pairs of elements in a poset

```agda
module _
  {l1 l2 : Level} (P : Poset l1 l2)
  where

  is-lower-bound-poset-Prop :
    (x y z : element-Poset P) → UU-Prop l2
  is-lower-bound-poset-Prop x y z =
    prod-Prop (leq-poset-Prop P z x) (leq-poset-Prop P z y)

  is-lower-bound-Poset :
    (x y z : element-Poset P) → UU l2
  is-lower-bound-Poset x y z = type-Prop (is-lower-bound-poset-Prop x y z)

  is-prop-is-lower-bound-Poset :
    (x y z : element-Poset P) → is-prop (is-lower-bound-Poset x y z)
  is-prop-is-lower-bound-Poset x y z =
    is-prop-type-Prop (is-lower-bound-poset-Prop x y z)

  is-greatest-lower-bound-poset-Prop :
    (x y z : element-Poset P) → UU-Prop (l1 ⊔ l2)
  is-greatest-lower-bound-poset-Prop x y z =
    prod-Prop
      ( is-lower-bound-poset-Prop x y z)
      ( Π-Prop
        ( element-Poset P)
        ( λ w →
          function-Prop
            ( is-lower-bound-Poset x y w)
            ( leq-poset-Prop P w z)))

  is-greatest-lower-bound-Poset :
    (x y z : element-Poset P) → UU (l1 ⊔ l2)
  is-greatest-lower-bound-Poset x y z =
    type-Prop (is-greatest-lower-bound-poset-Prop x y z)

  is-prop-is-greatest-lower-bound-Poset :
    (x y z : element-Poset P) → is-prop (is-greatest-lower-bound-Poset x y z)
  is-prop-is-greatest-lower-bound-Poset x y z =
    is-prop-type-Prop (is-greatest-lower-bound-poset-Prop x y z)

  has-greatest-lower-bound-Poset :
    (x y : element-Poset P) → UU (l1 ⊔ l2)
  has-greatest-lower-bound-Poset x y =
    Σ (element-Poset P) (is-greatest-lower-bound-Poset x y)

  all-elements-equal-has-greatest-lower-bound-Poset :
    (x y : element-Poset P) →
    all-elements-equal (has-greatest-lower-bound-Poset x y)
  all-elements-equal-has-greatest-lower-bound-Poset x y (pair u H) (pair v K) =
    eq-subtype
      ( is-greatest-lower-bound-poset-Prop x y)
      ( antisymmetric-leq-Poset P u v
        ( pr2 K u (pr1 H))
        ( pr2 H v (pr1 K)))

  is-prop-has-greatest-lower-bound-Poset :
    (x y : element-Poset P) → is-prop (has-greatest-lower-bound-Poset x y)
  is-prop-has-greatest-lower-bound-Poset x y =
    is-prop-all-elements-equal
      ( all-elements-equal-has-greatest-lower-bound-Poset x y)

  has-greatest-lower-bound-poset-Prop :
    (x y : element-Poset P) → UU-Prop (l1 ⊔ l2)
  pr1 (has-greatest-lower-bound-poset-Prop x y) =
    has-greatest-lower-bound-Poset x y
  pr2 (has-greatest-lower-bound-poset-Prop x y) =
    is-prop-has-greatest-lower-bound-Poset x y
```
