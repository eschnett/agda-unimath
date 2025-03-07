# Natural isomorphisms between functors on large precategories

```agda
{-# OPTIONS --without-K --exact-split #-}

module category-theory.natural-isomorphisms-large-precategories where

open import Agda.Primitive using (Setω)
open import category-theory.functors-large-precategories using
  ( functor-Large-Precat; obj-functor-Large-Precat;
    hom-functor-Large-Precat)
open import category-theory.isomorphisms-large-precategories using
  ( iso-Large-Precat; hom-iso-Large-Precat)
open import category-theory.large-precategories using
  ( Large-Precat; obj-Large-Precat; type-hom-Large-Precat)
open import category-theory.natural-transformations-large-precategories using
  ( square-Large-Precat; natural-transformation-Large-Precat;
    obj-natural-transformation-Large-Precat;
    coherence-square-natural-transformation-Large-Precat)
open import foundation.universe-levels using (Level)
```

## Idea

A natural isomorphism `γ` from functor `F : C → D` to `G : C → D` is a natural transformation from `F` to `G` such that the morphism `γ x : hom (F x) (G x)` is an isomorphism, for every object `x` in `C`.

## Definition

```agda
module _
  {αC αD γF γG : Level → Level} {βC βD : Level → Level → Level}
  {C : Large-Precat αC βC} {D : Large-Precat αD βD}
  (F : functor-Large-Precat C D γF) (G : functor-Large-Precat C D γG)
  where

  record natural-isomorphism-Large-Precat : Setω
    where
    constructor make-natural-isomorphism
    field
      obj-natural-isomorphism-Large-Precat :
        {l1 : Level} (X : obj-Large-Precat C l1) →
        iso-Large-Precat D
          ( obj-functor-Large-Precat F X)
          ( obj-functor-Large-Precat G X)
      coherence-square-natural-isomorphism-Large-Precat :
        {l1 l2 : Level} {X : obj-Large-Precat C l1}
        {Y : obj-Large-Precat C l2} (f : type-hom-Large-Precat C X Y) →
        square-Large-Precat D
          ( hom-iso-Large-Precat D
            ( obj-functor-Large-Precat F X)
            ( obj-functor-Large-Precat G X)
            ( obj-natural-isomorphism-Large-Precat X))
          ( hom-functor-Large-Precat F f)
          ( hom-functor-Large-Precat G f)
          ( hom-iso-Large-Precat D
            ( obj-functor-Large-Precat F Y)
            ( obj-functor-Large-Precat G Y)
            ( obj-natural-isomorphism-Large-Precat Y))
               
  open natural-isomorphism-Large-Precat public

  natural-transformation-natural-isomorphism-Large-Precat :
    natural-isomorphism-Large-Precat → (natural-transformation-Large-Precat F G)
  obj-natural-transformation-Large-Precat
    (natural-transformation-natural-isomorphism-Large-Precat γ) X =
      hom-iso-Large-Precat D
        ( obj-functor-Large-Precat F X)
        ( obj-functor-Large-Precat G X)
        ( obj-natural-isomorphism-Large-Precat γ X)
  coherence-square-natural-transformation-Large-Precat
    (natural-transformation-natural-isomorphism-Large-Precat γ) =
      coherence-square-natural-isomorphism-Large-Precat γ
```
