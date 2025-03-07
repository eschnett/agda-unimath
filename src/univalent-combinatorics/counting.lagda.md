---
title: Counting in type theory
---

```agda
{-# OPTIONS --without-K --exact-split #-}

module univalent-combinatorics.counting where

open import elementary-number-theory.natural-numbers using
  ( ℕ; zero-ℕ; succ-ℕ; is-zero-ℕ; is-one-ℕ)

open import foundation.contractible-types using
  ( is-contr; equiv-is-contr; is-contr-equiv'; center; eq-is-contr')
open import foundation.coproduct-types using (inr; inl)
open import foundation.decidable-equality using
  ( has-decidable-equality; has-decidable-equality-equiv')
open import foundation.decidable-types using (is-inhabited-or-empty)
open import foundation.dependent-pair-types using (Σ; pair; pr1; pr2)
open import foundation.empty-types using
  ( is-empty; ex-falso; is-equiv-is-empty'; empty; is-empty-type-trunc-Prop)
open import foundation.equivalences using
  ( _≃_; map-equiv; map-inv-equiv; inv-equiv; id-equiv; _∘e_; is-equiv;
    issec-map-inv-equiv; isretr-map-inv-equiv)
open import foundation.functions using (_∘_; id)
open import foundation.homotopies using (_~_)
open import foundation.identity-types using (Id; refl)
open import foundation.injective-maps using (is-injective-map-equiv)
open import foundation.propositional-truncations using
  ( unit-trunc-Prop; type-trunc-Prop; is-prop-type-trunc-Prop)
open import foundation.propositions using (is-proof-irrelevant-is-prop)
open import foundation.sets using (is-set; is-set-equiv')
open import foundation.unit-type using (unit; star; is-contr-unit)
open import foundation.universe-levels using (UU; Level)

open import univalent-combinatorics.equality-standard-finite-types using
  ( is-set-Fin; Eq-Fin-eq; has-decidable-equality-Fin)
open import univalent-combinatorics.standard-finite-types using
  ( Fin; zero-Fin; is-contr-Fin-one-ℕ; neg-one-Fin)
```

## Idea

The elements of a type `X` can be counted by establishing an equivalence `Fin n ≃ X`.

## Definition

```agda
count : {l : Level} → UU l → UU l
count X = Σ ℕ (λ k → Fin k ≃ X)

module _
  {l : Level} {X : UU l} (e : count X)
  where
  
  number-of-elements-count : ℕ
  number-of-elements-count = pr1 e
  
  equiv-count : Fin number-of-elements-count ≃ X
  equiv-count = pr2 e
  
  map-equiv-count : Fin number-of-elements-count → X
  map-equiv-count = map-equiv equiv-count
  
  map-inv-equiv-count : X → Fin number-of-elements-count
  map-inv-equiv-count = map-inv-equiv equiv-count

  issec-map-inv-equiv-count : (map-equiv-count ∘ map-inv-equiv-count) ~ id
  issec-map-inv-equiv-count = issec-map-inv-equiv equiv-count

  isretr-map-inv-equiv-count : (map-inv-equiv-count ∘ map-equiv-count) ~ id
  isretr-map-inv-equiv-count = isretr-map-inv-equiv equiv-count
  
  inv-equiv-count : X ≃ Fin number-of-elements-count
  inv-equiv-count = inv-equiv equiv-count
  
  is-set-count : is-set X
  is-set-count =
    is-set-equiv'
      ( Fin number-of-elements-count)
      ( equiv-count)
      ( is-set-Fin number-of-elements-count)
```

## Properties

### The elements of the standard finite types can be counted

```agda
count-Fin : (k : ℕ) → count (Fin k)
pr1 (count-Fin k) = k
pr2 (count-Fin k) = id-equiv
```

### Types equipped with countings are closed under equivalences

```agda
module _
  {l1 l2 : Level} {X : UU l1} {Y : UU l2}
  where
  
  abstract
    equiv-count-equiv :
      (e : X ≃ Y) (f : count X) → Fin (number-of-elements-count f) ≃ Y
    equiv-count-equiv e f = e ∘e (equiv-count f)

  count-equiv : X ≃ Y → count X → count Y
  pr1 (count-equiv e f) = number-of-elements-count f
  pr2 (count-equiv e f) = equiv-count-equiv e f

  abstract
    equiv-count-equiv' :
      (e : X ≃ Y) (f : count Y) → Fin (number-of-elements-count f) ≃ X
    equiv-count-equiv' e f = inv-equiv e ∘e (equiv-count f)
  
  count-equiv' : X ≃ Y → count Y → count X
  pr1 (count-equiv' e f) = number-of-elements-count f
  pr2 (count-equiv' e f) = equiv-count-equiv' e f
  
  count-is-equiv : {f : X → Y} → is-equiv f → count X → count Y
  count-is-equiv H = count-equiv (pair _ H)
  
  count-is-equiv' :
    {f : X → Y} → is-equiv f → count Y → count X
  count-is-equiv' H = count-equiv' (pair _ H)
```

### A type as 0 elements if and only if it is empty

```agda
abstract
  is-empty-is-zero-number-of-elements-count :
    {l : Level} {X : UU l} (e : count X) →
    is-zero-ℕ (number-of-elements-count e) → is-empty X
  is-empty-is-zero-number-of-elements-count (pair .zero-ℕ e) refl x =
    map-inv-equiv e x

abstract
  is-zero-number-of-elements-count-is-empty :
    {l : Level} {X : UU l} (e : count X) →
    is-empty X → is-zero-ℕ (number-of-elements-count e)
  is-zero-number-of-elements-count-is-empty (pair zero-ℕ e) H = refl
  is-zero-number-of-elements-count-is-empty (pair (succ-ℕ k) e) H =
    ex-falso (H (map-equiv e zero-Fin))

count-is-empty :
  {l : Level} {X : UU l} → is-empty X → count X
pr1 (count-is-empty H) = zero-ℕ
pr2 (count-is-empty H) = inv-equiv (pair H (is-equiv-is-empty' H))

count-empty : count empty
count-empty = count-Fin zero-ℕ
```

### A type has 1 element if and only if it is contractible

```agda
count-is-contr :
  {l : Level} {X : UU l} → is-contr X → count X
pr1 (count-is-contr H) = 1
pr2 (count-is-contr H) = equiv-is-contr is-contr-Fin-one-ℕ H

abstract
  is-contr-is-one-number-of-elements-count :
    {l : Level} {X : UU l} (e : count X) →
    is-one-ℕ (number-of-elements-count e) → is-contr X
  is-contr-is-one-number-of-elements-count (pair .(succ-ℕ zero-ℕ) e) refl =
    is-contr-equiv' (Fin 1) e is-contr-Fin-one-ℕ

abstract
  is-one-number-of-elements-count-is-contr :
    {l : Level} {X : UU l} (e : count X) →
    is-contr X → is-one-ℕ (number-of-elements-count e)
  is-one-number-of-elements-count-is-contr (pair zero-ℕ e) H =
    ex-falso (map-inv-equiv e (center H))
  is-one-number-of-elements-count-is-contr (pair (succ-ℕ zero-ℕ) e) H =
    refl
  is-one-number-of-elements-count-is-contr (pair (succ-ℕ (succ-ℕ k)) e) H =
    ex-falso
      ( Eq-Fin-eq
        ( is-injective-map-equiv e
          ( eq-is-contr' H (map-equiv e zero-Fin) (map-equiv e neg-one-Fin))))

count-unit : count unit
count-unit = count-is-contr is-contr-unit
```

### Types with a count have decidable equality

```agda
has-decidable-equality-count :
  {l : Level} {X : UU l} → count X → has-decidable-equality X
has-decidable-equality-count (pair k e) =
  has-decidable-equality-equiv' e has-decidable-equality-Fin
```

### This with a count are either inhabited or empty

```agda
is-inhabited-or-empty-count :
  {l1 : Level} {A : UU l1} → count A → is-inhabited-or-empty A
is-inhabited-or-empty-count (pair zero-ℕ e) =
  inr (is-empty-is-zero-number-of-elements-count (pair zero-ℕ e) refl)
is-inhabited-or-empty-count (pair (succ-ℕ k) e) =
  inl (unit-trunc-Prop (map-equiv e zero-Fin))
```

### If the elements of a type can be counted, then the elements of its propositional truncation can be counted

```agda
count-type-trunc-Prop :
  {l1 : Level} {A : UU l1} → count A → count (type-trunc-Prop A)
count-type-trunc-Prop (pair zero-ℕ e) =
  count-is-empty
    ( is-empty-type-trunc-Prop
      ( is-empty-is-zero-number-of-elements-count (pair zero-ℕ e) refl))
count-type-trunc-Prop (pair (succ-ℕ k) e) =
  count-is-contr
    ( is-proof-irrelevant-is-prop
      ( is-prop-type-trunc-Prop)
      ( unit-trunc-Prop (map-equiv e zero-Fin)))
```
