# Groups of order 2

```agda
{-# OPTIONS --without-K --exact-split --allow-unsolved-metas #-}

module finite-group-theory.groups-of-order-2 where

open import elementary-number-theory.groups-of-modular-arithmetic

open import finite-group-theory.finite-groups

open import foundation.contractible-types
open import foundation.dependent-pair-types
open import foundation.equivalences
open import foundation.fundamental-theorem-of-identity-types
open import foundation.identity-types
open import foundation.mere-equivalences
open import foundation.propositional-truncations
open import foundation.sets
open import foundation.subtype-identity-principle
open import foundation.universe-levels

open import group-theory.groups
open import group-theory.homomorphisms-groups
open import group-theory.isomorphisms-groups
open import group-theory.symmetric-groups

open import univalent-combinatorics.2-element-types
open import univalent-combinatorics.finite-types

open import univalent-combinatorics.equality-standard-finite-types
open import univalent-combinatorics.standard-finite-types
```

## Idea

The type of groups of order 2 is contractible

## Definitions

### The type of groups of order 2

```agda
Group-of-Order-2 : (l : Level) → UU (lsuc l)
Group-of-Order-2 l = Group-of-Order l 2

module _
  {l : Level} (G : Group-of-Order-2 l)
  where

  group-Group-of-Order-2 : Group l
  group-Group-of-Order-2 = pr1 G

  type-Group-of-Order-2 : UU l
  type-Group-of-Order-2 = type-Group group-Group-of-Order-2

  is-set-type-Group-of-Order-2 : is-set type-Group-of-Order-2
  is-set-type-Group-of-Order-2 = is-set-type-Group group-Group-of-Order-2

  mul-Group-of-Order-2 : (x y : type-Group-of-Order-2) → type-Group-of-Order-2
  mul-Group-of-Order-2 = mul-Group group-Group-of-Order-2

  unit-Group-of-Order-2 : type-Group-of-Order-2
  unit-Group-of-Order-2 = unit-Group group-Group-of-Order-2

  has-two-elements-Group-of-Order-2 : has-two-elements (type-Group-of-Order-2)
  has-two-elements-Group-of-Order-2 = pr2 G

  2-element-type-Group-of-Order-2 : 2-Element-Type l
  pr1 2-element-type-Group-of-Order-2 = type-Group-of-Order-2
  pr2 2-element-type-Group-of-Order-2 = has-two-elements-Group-of-Order-2
```

### The group ℤ/2 of order 2

```agda
ℤ-Mod-2-Group-of-Order-2 : Group-of-Order-2 lzero
pr1 ℤ-Mod-2-Group-of-Order-2 = ℤ-Mod-Group 2
pr2 ℤ-Mod-2-Group-of-Order-2 = refl-mere-equiv (Fin 2)
```

### The permutation group S₂ of order 2

```agda
symmetric-Group-of-Order-2 : (l : Level) → Group-of-Order-2 l
pr1 (symmetric-Group-of-Order-2 l) =
  symmetric-Group (raise-Fin-Set l 2)
pr2 (symmetric-Group-of-Order-2 l) =
  has-two-elements-Aut-2-Element-Type
    ( pair (raise-Fin l 2) (unit-trunc-Prop (equiv-raise-Fin l 2)))
```

## Properties

### Characterization of the identity type of the type of groups of order 2

```agda
iso-Group-of-Order-2 :
  {l1 l2 : Level} (G : Group-of-Order-2 l1) (H : Group-of-Order-2 l2) →
  UU (l1 ⊔ l2)
iso-Group-of-Order-2 G H =
  type-iso-Group (group-Group-of-Order-2 G) (group-Group-of-Order-2 H)

module _
  {l : Level} (G : Group-of-Order-2 l)
  where
  
  iso-eq-Group-of-Order-2 :
    (H : Group-of-Order-2 l) → Id G H → iso-Group-of-Order-2 G H
  iso-eq-Group-of-Order-2 H p =
    iso-eq-Group
      ( group-Group-of-Order-2 G)
      ( group-Group-of-Order-2 H)
      ( ap pr1 p)

  is-contr-total-iso-Group-of-Order-2 :
    is-contr (Σ (Group-of-Order-2 l) (iso-Group-of-Order-2 G))
  is-contr-total-iso-Group-of-Order-2 =
    is-contr-total-Eq-subtype
      ( is-contr-total-iso-Group (group-Group-of-Order-2 G))
      ( λ H → is-prop-type-trunc-Prop)
      ( group-Group-of-Order-2 G)
      ( id-iso-Group (group-Group-of-Order-2 G))
      ( has-two-elements-Group-of-Order-2 G)

  is-equiv-iso-eq-Group-of-Order-2 :
    (H : Group-of-Order-2 l) → is-equiv (iso-eq-Group-of-Order-2 H)
  is-equiv-iso-eq-Group-of-Order-2 =
    fundamental-theorem-id G
      ( id-iso-Group (group-Group-of-Order-2 G))
      ( is-contr-total-iso-Group-of-Order-2)
      ( iso-eq-Group-of-Order-2)

  eq-iso-Group-of-Order-2 :
    (H : Group-of-Order-2 l) → iso-Group-of-Order-2 G H → Id G H
  eq-iso-Group-of-Order-2 H =
    map-inv-is-equiv (is-equiv-iso-eq-Group-of-Order-2 H)
```

### A homomorphism from any group of order 2 to any group of order 2

```agda
module _
  {l1 l2 : Level} (G : Group-of-Order-2 l1) (H : Group-of-Order-2 l2)
  where

  equiv-Group-of-Order-2 :
    type-Group-of-Order-2 G ≃ type-Group-of-Order-2 H
  equiv-Group-of-Order-2 =
    ( equiv-point-2-Element-Type
      ( 2-element-type-Group-of-Order-2 H)
      ( unit-Group (group-Group-of-Order-2 H))) ∘e
    ( inv-equiv
      ( equiv-point-2-Element-Type
        ( 2-element-type-Group-of-Order-2 G)
        ( unit-Group (group-Group-of-Order-2 G))))

  map-specified-hom-Group-of-Order-2 :
    type-Group-of-Order-2 G → type-Group-of-Order-2 H
  map-specified-hom-Group-of-Order-2 =
    map-equiv equiv-Group-of-Order-2
  
  specified-hom-Group-of-Order-2 :
    type-hom-Group (group-Group-of-Order-2 G) (group-Group-of-Order-2 H)
  specified-hom-Group-of-Order-2 = {!!}
  
```

### The type of groups of order 2 is contractible

```agda
is-contr-Group-of-Order-2 : (l : Level) → is-contr (Group-of-Order-2 l)
pr1 (is-contr-Group-of-Order-2 l) = symmetric-Group-of-Order-2 l
pr2 (is-contr-Group-of-Order-2 l) G =
  eq-iso-Group-of-Order-2
    ( symmetric-Group-of-Order-2 l)
    ( G)
    {!!}
```
