# Commuting squares

```agda
{-# OPTIONS --without-K --exact-split --safe #-}

module foundation-core.commuting-squares where

open import foundation-core.functions using (_∘_)
open import foundation-core.homotopies using (_~_; _·l_; _·r_; _∙h_)
open import foundation-core.universe-levels using (Level; UU; _⊔_)
```

## Idea

A square of maps

```md
  A ------> X
  |         |
  |         |
  |         |
  V         V
  B ------> Y
```

is said to commute if there is a homotopy between both composites.

## Definition

```agda
coherence-square :
  {l1 l2 l3 l4 : Level} {A : UU l1} {B : UU l2} {C : UU l3} {X : UU l4}
  (top : C → B) (left : C → A) (right : B → X) (bottom : A → X) →
  UU (l3 ⊔ l4)
coherence-square top left right bottom =
  (bottom ∘ left) ~ (right ∘ top)
```

## Properties

### Composing commuting squares horizontally and vertically

```agda
coherence-square-comp-horizontal :
  {l1 l2 l3 l4 l5 l6 : Level}
  {A : UU l1} {B : UU l2} {C : UU l3} {X : UU l4} {Y : UU l5} {Z : UU l6}
  (top-left : A → B) (top-right : B → C)
  (left : A → X) (mid : B → Y) (right : C → Z)
  (bottom-left : X → Y) (bottom-right : Y → Z) →
  coherence-square top-left left mid bottom-left →
  coherence-square top-right mid right bottom-right →
  coherence-square
    (top-right ∘ top-left) left right (bottom-right ∘ bottom-left)
coherence-square-comp-horizontal
  top-left top-right left mid right bottom-left bottom-right sq-left sq-right =
  (bottom-right ·l sq-left) ∙h (sq-right ·r top-left)

coherence-square-comp-vertical :
  {l1 l2 l3 l4 l5 l6 : Level}
  {A : UU l1} {B : UU l2} {C : UU l3} {X : UU l4} {Y : UU l5} {Z : UU l6}
  (top : A → X)
  (left-top : A → B) (right-top : X → Y)
  (mid : B → Y)
  (left-bottom : B → C) (right-bottom : Y → Z)
  (bottom : C → Z) →
  coherence-square top left-top right-top mid →
  coherence-square mid left-bottom right-bottom bottom →
  coherence-square
    top (left-bottom ∘ left-top) (right-bottom ∘ right-top) bottom
coherence-square-comp-vertical
  top left-top right-top mid left-bottom right-bottom bottom sq-top sq-bottom =
  (sq-bottom ·r left-top) ∙h (right-bottom ·l sq-top)
```
