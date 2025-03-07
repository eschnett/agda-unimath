# Commuting squares

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.commuting-squares where

open import foundation-core.commuting-squares public

open import foundation-core.identity-types using (ap; inv; _∙_)
open import foundation-core.universe-levels using (Level; UU; _⊔_)

open import foundation.equivalences using
  ( _≃_; map-equiv; is-equiv-map-equiv; map-inv-equiv; map-eq-transpose-equiv';
    issec-map-inv-equiv; map-eq-transpose-equiv)
```

## Composing and inverting squares horizontally and vertically

If the horizontal/vertical maps in a commuting square are both equivalences, then the square remains commuting if we invert those equivalences.

```agda
coherence-square-inv-horizontal :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : UU l2} {X : UU l3} {Y : UU l4}
  (top : A ≃ B) (left : A → X) (right : B → Y) (bottom : X ≃ Y) →
  coherence-square (map-equiv top) left right (map-equiv bottom) →
  coherence-square (map-inv-equiv top) right left (map-inv-equiv bottom)
coherence-square-inv-horizontal top left right bottom H b =
  map-eq-transpose-equiv' bottom
    ( ( ap right (inv (issec-map-inv-equiv top b))) ∙
      ( inv (H (map-inv-equiv top b))))

coherence-square-inv-vertical :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : UU l2} {X : UU l3} {Y : UU l4}
  (top : A → B) (left : A ≃ X) (right : B ≃ Y) (bottom : X → Y) →
  coherence-square top (map-equiv left) (map-equiv right) bottom →
  coherence-square bottom (map-inv-equiv left) (map-inv-equiv right) top
coherence-square-inv-vertical top left right bottom H x =
  map-eq-transpose-equiv right
    ( inv (H (map-inv-equiv left x)) ∙ ap bottom (issec-map-inv-equiv left x))
```
