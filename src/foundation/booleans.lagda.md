# The booleans

```agda
{-# OPTIONS --without-K --exact-split #-}

module foundation.booleans where

open import foundation-core.constant-maps using (const)
open import foundation-core.dependent-pair-types using (pair; pr1; pr2)
open import foundation-core.empty-types using (empty; is-prop-empty)
open import foundation-core.equivalences using (is-equiv; _≃_)
open import foundation-core.functions using (id; _∘_)
open import foundation-core.homotopies using (_~_)
open import foundation-core.identity-types using (Id; refl; inv)
open import foundation.injective-maps using (is-injective)
open import foundation-core.negation using (¬)
open import foundation-core.propositions using (is-prop)
open import foundation-core.sets using (is-set; UU-Set; is-set-prop-in-id)
open import foundation.unit-type using (unit; star; is-prop-unit)
open import foundation-core.universe-levels using (lzero; UU)
```

## Idea

The type of booleans is a 2-element type with elements `true false : bool`, which is used for reasoning with decidable propositions.

## Definition

```agda
data bool : UU lzero where
  true false : bool

{-# BUILTIN BOOL bool #-}
{-# BUILTIN TRUE  true  #-}
{-# BUILTIN FALSE false #-}
```

### Equality on the booleans

```agda
Eq-bool : bool → bool → UU lzero
Eq-bool true true = unit
Eq-bool true false = empty
Eq-bool false true = empty
Eq-bool false false = unit

refl-Eq-bool : (x : bool) → Eq-bool x x
refl-Eq-bool true = star
refl-Eq-bool false = star

Eq-eq-bool :
  {x y : bool} → Id x y → Eq-bool x y
Eq-eq-bool {x = x} refl = refl-Eq-bool x

eq-Eq-bool :
  {x y : bool} → Eq-bool x y → Id x y
eq-Eq-bool {true} {true} star = refl
eq-Eq-bool {false} {false} star = refl

neq-false-true-bool :
  ¬ (Id false true)
neq-false-true-bool ()
```

## Structure

### The boolean operators

```agda
neg-bool : bool → bool
neg-bool true = false
neg-bool false = true

conjunction-bool : bool → (bool → bool)
conjunction-bool true true = true
conjunction-bool true false = false
conjunction-bool false true = false
conjunction-bool false false = false

disjunction-bool : bool → (bool → bool)
disjunction-bool true true = true
disjunction-bool true false = true
disjunction-bool false true = true
disjunction-bool false false = false
```

## Properties

### The booleans are a set

```agda
abstract
  is-prop-Eq-bool : (x y : bool) → is-prop (Eq-bool x y)
  is-prop-Eq-bool true true = is-prop-unit
  is-prop-Eq-bool true false = is-prop-empty
  is-prop-Eq-bool false true = is-prop-empty
  is-prop-Eq-bool false false = is-prop-unit

abstract
  is-set-bool : is-set bool
  is-set-bool =
    is-set-prop-in-id
      ( Eq-bool)
      ( is-prop-Eq-bool)
      ( refl-Eq-bool)
      ( λ x y → eq-Eq-bool)

bool-Set : UU-Set lzero
pr1 bool-Set = bool
pr2 bool-Set = is-set-bool
```


```agda
neq-neg-bool : (b : bool) → ¬ (Id b (neg-bool b))
neq-neg-bool true ()
neq-neg-bool false ()

neg-neg-bool : (neg-bool ∘ neg-bool) ~ id
neg-neg-bool true = refl
neg-neg-bool false = refl

abstract
  is-equiv-neg-bool : is-equiv neg-bool
  pr1 (pr1 is-equiv-neg-bool) = neg-bool
  pr2 (pr1 is-equiv-neg-bool) = neg-neg-bool
  pr1 (pr2 is-equiv-neg-bool) = neg-bool
  pr2 (pr2 is-equiv-neg-bool) = neg-neg-bool

equiv-neg-bool : bool ≃ bool
pr1 equiv-neg-bool = neg-bool
pr2 equiv-neg-bool = is-equiv-neg-bool
```

### The constant function `const bool bool b` is not an equivalence

```agda
abstract
  not-equiv-const :
    (b : bool) → ¬ (is-equiv (const bool bool b))
  not-equiv-const true (pair (pair g G) (pair h H)) =
    neq-false-true-bool (inv (G false))
  not-equiv-const false (pair (pair g G) (pair h H)) =
    neq-false-true-bool (G true)
```

### The constant function `const bool bool b` is injective

```agda
abstract
  is-injective-const-true : is-injective (const unit bool true)
  is-injective-const-true {star} {star} p = refl

abstract
  is-injective-const-false : is-injective (const unit bool false)
  is-injective-const-false {star} {star} p = refl
```
