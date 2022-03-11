# Univalent mathematics in Agda

Welcome to the website of the `agda-unimath` formalization project.

[![build](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml)

<pre class="Agda"><a id="281" class="Symbol">{-#</a> <a id="285" class="Keyword">OPTIONS</a> <a id="293" class="Pragma">--without-K</a> <a id="305" class="Pragma">--exact-split</a> <a id="319" class="Symbol">#-}</a>
</pre>
## Categories

<pre class="Agda"><a id="351" class="Keyword">open</a> <a id="356" class="Keyword">import</a> <a id="363" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="411" class="Keyword">open</a> <a id="416" class="Keyword">import</a> <a id="423" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="450" class="Keyword">open</a> <a id="455" class="Keyword">import</a> <a id="462" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="502" class="Keyword">open</a> <a id="507" class="Keyword">import</a> <a id="514" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="563" class="Keyword">open</a> <a id="568" class="Keyword">import</a> <a id="575" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="618" class="Keyword">open</a> <a id="623" class="Keyword">import</a> <a id="630" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="666" class="Keyword">open</a> <a id="671" class="Keyword">import</a> <a id="678" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="723" class="Keyword">open</a> <a id="728" class="Keyword">import</a> <a id="735" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="774" class="Keyword">open</a> <a id="779" class="Keyword">import</a> <a id="786" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="857" class="Keyword">open</a> <a id="862" class="Keyword">import</a> <a id="869" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="909" class="Keyword">open</a> <a id="914" class="Keyword">import</a> <a id="921" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="970" class="Keyword">open</a> <a id="975" class="Keyword">import</a> <a id="982" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="1025" class="Keyword">open</a> <a id="1030" class="Keyword">import</a> <a id="1037" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="1070" class="Keyword">open</a> <a id="1075" class="Keyword">import</a> <a id="1082" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="1118" class="Keyword">open</a> <a id="1123" class="Keyword">import</a> <a id="1130" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="1180" class="Keyword">open</a> <a id="1185" class="Keyword">import</a> <a id="1192" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="1240" class="Keyword">open</a> <a id="1245" class="Keyword">import</a> <a id="1252" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="1309" class="Keyword">open</a> <a id="1314" class="Keyword">import</a> <a id="1321" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="1372" class="Keyword">open</a> <a id="1377" class="Keyword">import</a> <a id="1384" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="1435" class="Keyword">open</a> <a id="1440" class="Keyword">import</a> <a id="1447" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="1507" class="Keyword">open</a> <a id="1512" class="Keyword">import</a> <a id="1519" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="1573" class="Keyword">open</a> <a id="1578" class="Keyword">import</a> <a id="1585" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="1657" class="Keyword">open</a> <a id="1662" class="Keyword">import</a> <a id="1669" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="1694" class="Keyword">open</a> <a id="1699" class="Keyword">import</a> <a id="1706" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="1755" class="Keyword">open</a> <a id="1760" class="Keyword">import</a> <a id="1767" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="1810" class="Keyword">open</a> <a id="1815" class="Keyword">import</a> <a id="1822" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="1872" class="Keyword">open</a> <a id="1877" class="Keyword">import</a> <a id="1884" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="1931" class="Keyword">open</a> <a id="1936" class="Keyword">import</a> <a id="1943" href="elementary-number-theory.classical-finite-types.html" class="Module">elementary-number-theory.classical-finite-types</a>
<a id="1991" class="Keyword">open</a> <a id="1996" class="Keyword">import</a> <a id="2003" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="2046" class="Keyword">open</a> <a id="2051" class="Keyword">import</a> <a id="2058" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="2102" class="Keyword">open</a> <a id="2107" class="Keyword">import</a> <a id="2114" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="2159" class="Keyword">open</a> <a id="2164" class="Keyword">import</a> <a id="2171" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="2223" class="Keyword">open</a> <a id="2228" class="Keyword">import</a> <a id="2235" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="2295" class="Keyword">open</a> <a id="2300" class="Keyword">import</a> <a id="2307" href="elementary-number-theory.decidable-dependent-pair-types.html" class="Module">elementary-number-theory.decidable-dependent-pair-types</a>
<a id="2363" class="Keyword">open</a> <a id="2368" class="Keyword">import</a> <a id="2375" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="2420" class="Keyword">open</a> <a id="2425" class="Keyword">import</a> <a id="2432" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="2475" class="Keyword">open</a> <a id="2480" class="Keyword">import</a> <a id="2487" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="2537" class="Keyword">open</a> <a id="2542" class="Keyword">import</a> <a id="2549" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="2596" class="Keyword">open</a> <a id="2601" class="Keyword">import</a> <a id="2608" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="2662" class="Keyword">open</a> <a id="2667" class="Keyword">import</a> <a id="2674" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="2734" class="Keyword">open</a> <a id="2739" class="Keyword">import</a> <a id="2746" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="2789" class="Keyword">open</a> <a id="2794" class="Keyword">import</a> <a id="2801" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="2851" class="Keyword">open</a> <a id="2856" class="Keyword">import</a> <a id="2863" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="2923" class="Keyword">open</a> <a id="2928" class="Keyword">import</a> <a id="2935" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="2984" class="Keyword">open</a> <a id="2989" class="Keyword">import</a> <a id="2996" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="3052" class="Keyword">open</a> <a id="3057" class="Keyword">import</a> <a id="3064" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="3100" class="Keyword">open</a> <a id="3105" class="Keyword">import</a> <a id="3112" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="3156" class="Keyword">open</a> <a id="3161" class="Keyword">import</a> <a id="3168" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="3212" class="Keyword">open</a> <a id="3217" class="Keyword">import</a> <a id="3224" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="3274" class="Keyword">open</a> <a id="3279" class="Keyword">import</a> <a id="3286" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="3332" class="Keyword">open</a> <a id="3337" class="Keyword">import</a> <a id="3344" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="3379" class="Keyword">open</a> <a id="3384" class="Keyword">import</a> <a id="3391" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="3436" class="Keyword">open</a> <a id="3441" class="Keyword">import</a> <a id="3448" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="3506" class="Keyword">open</a> <a id="3511" class="Keyword">import</a> <a id="3518" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="3583" class="Keyword">open</a> <a id="3588" class="Keyword">import</a> <a id="3595" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="3640" class="Keyword">open</a> <a id="3645" class="Keyword">import</a> <a id="3652" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="3704" class="Keyword">open</a> <a id="3709" class="Keyword">import</a> <a id="3716" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="3774" class="Keyword">open</a> <a id="3779" class="Keyword">import</a> <a id="3786" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="3832" class="Keyword">open</a> <a id="3837" class="Keyword">import</a> <a id="3844" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="3878" class="Keyword">open</a> <a id="3883" class="Keyword">import</a> <a id="3890" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="3935" class="Keyword">open</a> <a id="3940" class="Keyword">import</a> <a id="3947" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="4001" class="Keyword">open</a> <a id="4006" class="Keyword">import</a> <a id="4013" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="4079" class="Keyword">open</a> <a id="4084" class="Keyword">import</a> <a id="4091" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="4135" class="Keyword">open</a> <a id="4140" class="Keyword">import</a> <a id="4147" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="4196" class="Keyword">open</a> <a id="4201" class="Keyword">import</a> <a id="4208" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="4264" class="Keyword">open</a> <a id="4269" class="Keyword">import</a> <a id="4276" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="4317" class="Keyword">open</a> <a id="4322" class="Keyword">import</a> <a id="4329" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="4388" class="Keyword">open</a> <a id="4393" class="Keyword">import</a> <a id="4400" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="4439" class="Keyword">open</a> <a id="4444" class="Keyword">import</a> <a id="4451" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="4504" class="Keyword">open</a> <a id="4509" class="Keyword">import</a> <a id="4516" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="4573" class="Keyword">open</a> <a id="4578" class="Keyword">import</a> <a id="4585" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="4627" class="Keyword">open</a> <a id="4632" class="Keyword">import</a> <a id="4639" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="4690" class="Keyword">open</a> <a id="4695" class="Keyword">import</a> <a id="4702" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="4760" class="Keyword">open</a> <a id="4765" class="Keyword">import</a> <a id="4772" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="4836" class="Keyword">open</a> <a id="4841" class="Keyword">import</a> <a id="4848" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="4901" class="Keyword">open</a> <a id="4906" class="Keyword">import</a> <a id="4913" href="elementary-number-theory.retracts-of-standard-finite-types.html" class="Module">elementary-number-theory.retracts-of-standard-finite-types</a>
<a id="4972" class="Keyword">open</a> <a id="4977" class="Keyword">import</a> <a id="4984" href="elementary-number-theory.skipping-element-standard-finite-type.html" class="Module">elementary-number-theory.skipping-element-standard-finite-type</a>
<a id="5047" class="Keyword">open</a> <a id="5052" class="Keyword">import</a> <a id="5059" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="5120" class="Keyword">open</a> <a id="5125" class="Keyword">import</a> <a id="5132" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="5190" class="Keyword">open</a> <a id="5195" class="Keyword">import</a> <a id="5202" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="5251" class="Keyword">open</a> <a id="5256" class="Keyword">import</a> <a id="5263" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="5307" class="Keyword">open</a> <a id="5312" class="Keyword">import</a> <a id="5319" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="5366" class="Keyword">open</a> <a id="5371" class="Keyword">import</a> <a id="5378" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="5438" class="Keyword">open</a> <a id="5443" class="Keyword">import</a> <a id="5450" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="5504" class="Keyword">open</a> <a id="5509" class="Keyword">import</a> <a id="5516" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="5581" class="Keyword">open</a> <a id="5586" class="Keyword">import</a> <a id="5593" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite groups

<pre class="Agda"><a id="5695" class="Keyword">open</a> <a id="5700" class="Keyword">import</a> <a id="5707" href="finite-groups.abstract-quaternion-group.html" class="Module">finite-groups.abstract-quaternion-group</a>
<a id="5747" class="Keyword">open</a> <a id="5752" class="Keyword">import</a> <a id="5759" href="finite-groups.concrete-quaternion-group.html" class="Module">finite-groups.concrete-quaternion-group</a>
<a id="5799" class="Keyword">open</a> <a id="5804" class="Keyword">import</a> <a id="5811" href="finite-groups.finite-groups.html" class="Module">finite-groups.finite-groups</a>
<a id="5839" class="Keyword">open</a> <a id="5844" class="Keyword">import</a> <a id="5851" href="finite-groups.orbits-permutations.html" class="Module">finite-groups.orbits-permutations</a>
<a id="5885" class="Keyword">open</a> <a id="5890" class="Keyword">import</a> <a id="5897" href="finite-groups.transpositions.html" class="Module">finite-groups.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="5954" class="Keyword">open</a> <a id="5959" class="Keyword">import</a> <a id="5966" href="foundation.html" class="Module">foundation</a>
<a id="5977" class="Keyword">open</a> <a id="5982" class="Keyword">import</a> <a id="5989" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="6007" class="Keyword">open</a> <a id="6012" class="Keyword">import</a> <a id="6019" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="6038" class="Keyword">open</a> <a id="6043" class="Keyword">import</a> <a id="6050" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="6069" class="Keyword">open</a> <a id="6074" class="Keyword">import</a> <a id="6081" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="6125" class="Keyword">open</a> <a id="6130" class="Keyword">import</a> <a id="6137" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="6162" class="Keyword">open</a> <a id="6167" class="Keyword">import</a> <a id="6174" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="6201" class="Keyword">open</a> <a id="6206" class="Keyword">import</a> <a id="6213" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="6242" class="Keyword">open</a> <a id="6247" class="Keyword">import</a> <a id="6254" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="6285" class="Keyword">open</a> <a id="6290" class="Keyword">import</a> <a id="6297" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="6325" class="Keyword">open</a> <a id="6330" class="Keyword">import</a> <a id="6337" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="6367" class="Keyword">open</a> <a id="6372" class="Keyword">import</a> <a id="6379" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="6399" class="Keyword">open</a> <a id="6404" class="Keyword">import</a> <a id="6411" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="6448" class="Keyword">open</a> <a id="6453" class="Keyword">import</a> <a id="6460" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="6495" class="Keyword">open</a> <a id="6500" class="Keyword">import</a> <a id="6507" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="6565" class="Keyword">open</a> <a id="6570" class="Keyword">import</a> <a id="6577" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="6615" class="Keyword">open</a> <a id="6620" class="Keyword">import</a> <a id="6627" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="6656" class="Keyword">open</a> <a id="6661" class="Keyword">import</a> <a id="6668" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="6691" class="Keyword">open</a> <a id="6696" class="Keyword">import</a> <a id="6703" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="6726" class="Keyword">open</a> <a id="6731" class="Keyword">import</a> <a id="6738" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="6780" class="Keyword">open</a> <a id="6785" class="Keyword">import</a> <a id="6792" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="6824" class="Keyword">open</a> <a id="6829" class="Keyword">import</a> <a id="6836" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="6863" class="Keyword">open</a> <a id="6868" class="Keyword">import</a> <a id="6875" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="6900" class="Keyword">open</a> <a id="6905" class="Keyword">import</a> <a id="6912" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="6941" class="Keyword">open</a> <a id="6946" class="Keyword">import</a> <a id="6953" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="6983" class="Keyword">open</a> <a id="6988" class="Keyword">import</a> <a id="6995" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="7022" class="Keyword">open</a> <a id="7027" class="Keyword">import</a> <a id="7034" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="7053" class="Keyword">open</a> <a id="7058" class="Keyword">import</a> <a id="7065" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="7111" class="Keyword">open</a> <a id="7116" class="Keyword">import</a> <a id="7123" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="7165" class="Keyword">open</a> <a id="7170" class="Keyword">import</a> <a id="7177" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="7209" class="Keyword">open</a> <a id="7214" class="Keyword">import</a> <a id="7221" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="7251" class="Keyword">open</a> <a id="7256" class="Keyword">import</a> <a id="7263" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="7289" class="Keyword">open</a> <a id="7294" class="Keyword">import</a> <a id="7301" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="7335" class="Keyword">open</a> <a id="7340" class="Keyword">import</a> <a id="7347" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="7377" class="Keyword">open</a> <a id="7382" class="Keyword">import</a> <a id="7389" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="7416" class="Keyword">open</a> <a id="7421" class="Keyword">import</a> <a id="7428" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="7460" class="Keyword">open</a> <a id="7465" class="Keyword">import</a> <a id="7472" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="7506" class="Keyword">open</a> <a id="7511" class="Keyword">import</a> <a id="7518" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="7541" class="Keyword">open</a> <a id="7546" class="Keyword">import</a> <a id="7553" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="7623" class="Keyword">open</a> <a id="7628" class="Keyword">import</a> <a id="7635" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="7705" class="Keyword">open</a> <a id="7710" class="Keyword">import</a> <a id="7717" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="7744" class="Keyword">open</a> <a id="7749" class="Keyword">import</a> <a id="7756" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="7804" class="Keyword">open</a> <a id="7809" class="Keyword">import</a> <a id="7816" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="7856" class="Keyword">open</a> <a id="7861" class="Keyword">import</a> <a id="7868" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="7890" class="Keyword">open</a> <a id="7895" class="Keyword">import</a> <a id="7902" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="7925" class="Keyword">open</a> <a id="7930" class="Keyword">import</a> <a id="7937" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="7982" class="Keyword">open</a> <a id="7987" class="Keyword">import</a> <a id="7994" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="8038" class="Keyword">open</a> <a id="8043" class="Keyword">import</a> <a id="8050" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="8086" class="Keyword">open</a> <a id="8091" class="Keyword">import</a> <a id="8098" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="8143" class="Keyword">open</a> <a id="8148" class="Keyword">import</a> <a id="8155" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="8196" class="Keyword">open</a> <a id="8201" class="Keyword">import</a> <a id="8208" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="8243" class="Keyword">open</a> <a id="8248" class="Keyword">import</a> <a id="8255" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="8286" class="Keyword">open</a> <a id="8291" class="Keyword">import</a> <a id="8298" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="8331" class="Keyword">open</a> <a id="8336" class="Keyword">import</a> <a id="8343" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="8376" class="Keyword">open</a> <a id="8381" class="Keyword">import</a> <a id="8388" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="8418" class="Keyword">open</a> <a id="8423" class="Keyword">import</a> <a id="8430" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="8454" class="Keyword">open</a> <a id="8459" class="Keyword">import</a> <a id="8466" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="8504" class="Keyword">open</a> <a id="8509" class="Keyword">import</a> <a id="8516" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="8547" class="Keyword">open</a> <a id="8552" class="Keyword">import</a> <a id="8559" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="8584" class="Keyword">open</a> <a id="8589" class="Keyword">import</a> <a id="8596" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="8624" class="Keyword">open</a> <a id="8629" class="Keyword">import</a> <a id="8636" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="8660" class="Keyword">open</a> <a id="8665" class="Keyword">import</a> <a id="8672" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="8698" class="Keyword">open</a> <a id="8703" class="Keyword">import</a> <a id="8710" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="8745" class="Keyword">open</a> <a id="8750" class="Keyword">import</a> <a id="8757" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="8778" class="Keyword">open</a> <a id="8783" class="Keyword">import</a> <a id="8790" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="8839" class="Keyword">open</a> <a id="8844" class="Keyword">import</a> <a id="8851" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="8892" class="Keyword">open</a> <a id="8897" class="Keyword">import</a> <a id="8904" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="8954" class="Keyword">open</a> <a id="8959" class="Keyword">import</a> <a id="8966" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="9012" class="Keyword">open</a> <a id="9017" class="Keyword">import</a> <a id="9024" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="9064" class="Keyword">open</a> <a id="9069" class="Keyword">import</a> <a id="9076" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="9126" class="Keyword">open</a> <a id="9131" class="Keyword">import</a> <a id="9138" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="9177" class="Keyword">open</a> <a id="9182" class="Keyword">import</a> <a id="9189" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="9229" class="Keyword">open</a> <a id="9234" class="Keyword">import</a> <a id="9241" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="9274" class="Keyword">open</a> <a id="9279" class="Keyword">import</a> <a id="9286" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="9335" class="Keyword">open</a> <a id="9340" class="Keyword">import</a> <a id="9347" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="9372" class="Keyword">open</a> <a id="9377" class="Keyword">import</a> <a id="9384" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="9406" class="Keyword">open</a> <a id="9411" class="Keyword">import</a> <a id="9418" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="9446" class="Keyword">open</a> <a id="9451" class="Keyword">import</a> <a id="9458" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="9484" class="Keyword">open</a> <a id="9489" class="Keyword">import</a> <a id="9496" href="foundation.images.html" class="Module">foundation.images</a>
<a id="9514" class="Keyword">open</a> <a id="9519" class="Keyword">import</a> <a id="9526" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="9561" class="Keyword">open</a> <a id="9566" class="Keyword">import</a> <a id="9573" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="9600" class="Keyword">open</a> <a id="9605" class="Keyword">import</a> <a id="9612" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="9668" class="Keyword">open</a> <a id="9673" class="Keyword">import</a> <a id="9680" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="9709" class="Keyword">open</a> <a id="9714" class="Keyword">import</a> <a id="9721" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="9751" class="Keyword">open</a> <a id="9756" class="Keyword">import</a> <a id="9763" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="9789" class="Keyword">open</a> <a id="9794" class="Keyword">import</a> <a id="9801" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="9828" class="Keyword">open</a> <a id="9833" class="Keyword">import</a> <a id="9840" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="9863" class="Keyword">open</a> <a id="9868" class="Keyword">import</a> <a id="9875" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="9902" class="Keyword">open</a> <a id="9907" class="Keyword">import</a> <a id="9914" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="9946" class="Keyword">open</a> <a id="9951" class="Keyword">import</a> <a id="9958" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="9992" class="Keyword">open</a> <a id="9997" class="Keyword">import</a> <a id="10004" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="10044" class="Keyword">open</a> <a id="10049" class="Keyword">import</a> <a id="10056" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="10087" class="Keyword">open</a> <a id="10092" class="Keyword">import</a> <a id="10099" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="10131" class="Keyword">open</a> <a id="10136" class="Keyword">import</a> <a id="10143" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="10160" class="Keyword">open</a> <a id="10165" class="Keyword">import</a> <a id="10172" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="10197" class="Keyword">open</a> <a id="10202" class="Keyword">import</a> <a id="10209" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="10238" class="Keyword">open</a> <a id="10243" class="Keyword">import</a> <a id="10250" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="10275" class="Keyword">open</a> <a id="10280" class="Keyword">import</a> <a id="10287" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="10308" class="Keyword">open</a> <a id="10313" class="Keyword">import</a> <a id="10320" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="10340" class="Keyword">open</a> <a id="10345" class="Keyword">import</a> <a id="10352" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="10386" class="Keyword">open</a> <a id="10391" class="Keyword">import</a> <a id="10398" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="10422" class="Keyword">open</a> <a id="10427" class="Keyword">import</a> <a id="10434" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="10461" class="Keyword">open</a> <a id="10466" class="Keyword">import</a> <a id="10473" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="10508" class="Keyword">open</a> <a id="10513" class="Keyword">import</a> <a id="10520" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="10560" class="Keyword">open</a> <a id="10565" class="Keyword">import</a> <a id="10572" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="10602" class="Keyword">open</a> <a id="10607" class="Keyword">import</a> <a id="10614" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="10651" class="Keyword">open</a> <a id="10656" class="Keyword">import</a> <a id="10663" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="10687" class="Keyword">open</a> <a id="10692" class="Keyword">import</a> <a id="10699" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="10720" class="Keyword">open</a> <a id="10725" class="Keyword">import</a> <a id="10732" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="10767" class="Keyword">open</a> <a id="10772" class="Keyword">import</a> <a id="10779" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="10816" class="Keyword">open</a> <a id="10821" class="Keyword">import</a> <a id="10828" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="10877" class="Keyword">open</a> <a id="10882" class="Keyword">import</a> <a id="10889" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="10912" class="Keyword">open</a> <a id="10917" class="Keyword">import</a> <a id="10924" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="10947" class="Keyword">open</a> <a id="10952" class="Keyword">import</a> <a id="10959" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="10987" class="Keyword">open</a> <a id="10992" class="Keyword">import</a> <a id="10999" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="11019" class="Keyword">open</a> <a id="11024" class="Keyword">import</a> <a id="11031" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="11062" class="Keyword">open</a> <a id="11067" class="Keyword">import</a> <a id="11074" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="11101" class="Keyword">open</a> <a id="11106" class="Keyword">import</a> <a id="11113" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="11129" class="Keyword">open</a> <a id="11134" class="Keyword">import</a> <a id="11141" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="11172" class="Keyword">open</a> <a id="11177" class="Keyword">import</a> <a id="11184" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="11201" class="Keyword">open</a> <a id="11206" class="Keyword">import</a> <a id="11213" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="11235" class="Keyword">open</a> <a id="11240" class="Keyword">import</a> <a id="11247" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="11274" class="Keyword">open</a> <a id="11279" class="Keyword">import</a> <a id="11286" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="11309" class="Keyword">open</a> <a id="11314" class="Keyword">import</a> <a id="11321" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="11348" class="Keyword">open</a> <a id="11353" class="Keyword">import</a> <a id="11360" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="11393" class="Keyword">open</a> <a id="11398" class="Keyword">import</a> <a id="11405" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="11445" class="Keyword">open</a> <a id="11450" class="Keyword">import</a> <a id="11457" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="11478" class="Keyword">open</a> <a id="11483" class="Keyword">import</a> <a id="11490" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="11519" class="Keyword">open</a> <a id="11524" class="Keyword">import</a> <a id="11531" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="11569" class="Keyword">open</a> <a id="11574" class="Keyword">import</a> <a id="11581" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="11601" class="Keyword">open</a> <a id="11606" class="Keyword">import</a> <a id="11613" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="11637" class="Keyword">open</a> <a id="11642" class="Keyword">import</a> <a id="11649" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="11676" class="Keyword">open</a> <a id="11681" class="Keyword">import</a> <a id="11688" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="11714" class="Keyword">open</a> <a id="11719" class="Keyword">import</a> <a id="11726" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="11753" class="Keyword">open</a> <a id="11758" class="Keyword">import</a> <a id="11765" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="11794" class="Keyword">open</a> <a id="11799" class="Keyword">import</a> <a id="11806" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="11829" class="Keyword">open</a> <a id="11834" class="Keyword">import</a> <a id="11841" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="11892" class="Keyword">open</a> <a id="11897" class="Keyword">import</a> <a id="11904" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="11947" class="Keyword">open</a> <a id="11952" class="Keyword">import</a> <a id="11959" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="12007" class="Keyword">open</a> <a id="12012" class="Keyword">import</a> <a id="12019" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="12057" class="Keyword">open</a> <a id="12062" class="Keyword">import</a> <a id="12069" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="12106" class="Keyword">open</a> <a id="12111" class="Keyword">import</a> <a id="12118" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="12146" class="Keyword">open</a> <a id="12151" class="Keyword">import</a> <a id="12158" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="12194" class="Keyword">open</a> <a id="12199" class="Keyword">import</a> <a id="12206" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="12244" class="Keyword">open</a> <a id="12249" class="Keyword">import</a> <a id="12256" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="12289" class="Keyword">open</a> <a id="12294" class="Keyword">import</a> <a id="12301" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="12322" class="Keyword">open</a> <a id="12327" class="Keyword">import</a> <a id="12334" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="12388" class="Keyword">open</a> <a id="12393" class="Keyword">import</a> <a id="12400" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="12422" class="Keyword">open</a> <a id="12427" class="Keyword">import</a> <a id="12434" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="12469" class="Keyword">open</a> <a id="12474" class="Keyword">import</a> <a id="12481" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="12511" class="Keyword">open</a> <a id="12516" class="Keyword">import</a> <a id="12523" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="12562" class="Keyword">open</a> <a id="12567" class="Keyword">import</a> <a id="12574" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="12628" class="Keyword">open</a> <a id="12633" class="Keyword">import</a> <a id="12640" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="12686" class="Keyword">open</a> <a id="12691" class="Keyword">import</a> <a id="12698" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="12749" class="Keyword">open</a> <a id="12754" class="Keyword">import</a> <a id="12761" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="12802" class="Keyword">open</a> <a id="12807" class="Keyword">import</a> <a id="12814" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="12859" class="Keyword">open</a> <a id="12864" class="Keyword">import</a> <a id="12871" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="12916" class="Keyword">open</a> <a id="12921" class="Keyword">import</a> <a id="12928" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="12964" class="Keyword">open</a> <a id="12969" class="Keyword">import</a> <a id="12976" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="13012" class="Keyword">open</a> <a id="13017" class="Keyword">import</a> <a id="13024" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="13089" class="Keyword">open</a> <a id="13094" class="Keyword">import</a> <a id="13101" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="13156" class="Keyword">open</a> <a id="13161" class="Keyword">import</a> <a id="13168" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="13208" class="Keyword">open</a> <a id="13213" class="Keyword">import</a> <a id="13220" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="13264" class="Keyword">open</a> <a id="13269" class="Keyword">import</a> <a id="13276" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="13321" class="Keyword">open</a> <a id="13326" class="Keyword">import</a> <a id="13333" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="13374" class="Keyword">open</a> <a id="13379" class="Keyword">import</a> <a id="13386" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="13426" class="Keyword">open</a> <a id="13431" class="Keyword">import</a> <a id="13438" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="13465" class="Keyword">open</a> <a id="13470" class="Keyword">import</a> <a id="13477" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="13504" class="Keyword">open</a> <a id="13509" class="Keyword">import</a> <a id="13516" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="13535" class="Keyword">open</a> <a id="13540" class="Keyword">import</a> <a id="13547" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="13587" class="Keyword">open</a> <a id="13592" class="Keyword">import</a> <a id="13599" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="13664" class="Keyword">open</a> <a id="13669" class="Keyword">import</a> <a id="13676" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="13699" class="Keyword">open</a> <a id="13704" class="Keyword">import</a> <a id="13711" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="13735" class="Keyword">open</a> <a id="13740" class="Keyword">import</a> <a id="13747" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="13787" class="Keyword">open</a> <a id="13792" class="Keyword">import</a> <a id="13799" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="13842" class="Keyword">open</a> <a id="13847" class="Keyword">import</a> <a id="13854" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="13888" class="Keyword">open</a> <a id="13893" class="Keyword">import</a> <a id="13900" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="13930" class="Keyword">open</a> <a id="13935" class="Keyword">import</a> <a id="13942" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="13976" class="Keyword">open</a> <a id="13981" class="Keyword">import</a> <a id="13988" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="14023" class="Keyword">open</a> <a id="14028" class="Keyword">import</a> <a id="14035" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="14072" class="Keyword">open</a> <a id="14077" class="Keyword">import</a> <a id="14084" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="14111" class="Keyword">open</a> <a id="14116" class="Keyword">import</a> <a id="14123" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="14151" class="Keyword">open</a> <a id="14156" class="Keyword">import</a> <a id="14163" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="14212" class="Keyword">open</a> <a id="14217" class="Keyword">import</a> <a id="14224" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="14270" class="Keyword">open</a> <a id="14275" class="Keyword">import</a> <a id="14282" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="14322" class="Keyword">open</a> <a id="14327" class="Keyword">import</a> <a id="14334" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="14372" class="Keyword">open</a> <a id="14377" class="Keyword">import</a> <a id="14384" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="14413" class="Keyword">open</a> <a id="14418" class="Keyword">import</a> <a id="14425" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="14455" class="Keyword">open</a> <a id="14460" class="Keyword">import</a> <a id="14467" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="14498" class="Keyword">open</a> <a id="14503" class="Keyword">import</a> <a id="14510" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="14536" class="Keyword">open</a> <a id="14541" class="Keyword">import</a> <a id="14548" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="14599" class="Keyword">open</a> <a id="14604" class="Keyword">import</a> <a id="14611" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="14665" class="Keyword">open</a> <a id="14670" class="Keyword">import</a> <a id="14677" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="14704" class="Keyword">open</a> <a id="14709" class="Keyword">import</a> <a id="14716" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="14749" class="Keyword">open</a> <a id="14754" class="Keyword">import</a> <a id="14761" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="14792" class="Keyword">open</a> <a id="14797" class="Keyword">import</a> <a id="14804" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="14841" class="Keyword">open</a> <a id="14846" class="Keyword">import</a> <a id="14853" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="14878" class="Keyword">open</a> <a id="14883" class="Keyword">import</a> <a id="14890" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="14922" class="Keyword">open</a> <a id="14927" class="Keyword">import</a> <a id="14934" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="14969" class="Keyword">open</a> <a id="14974" class="Keyword">import</a> <a id="14981" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="15010" class="Keyword">open</a> <a id="15015" class="Keyword">import</a> <a id="15022" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="15050" class="Keyword">open</a> <a id="15055" class="Keyword">import</a> <a id="15062" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="15087" class="Keyword">open</a> <a id="15092" class="Keyword">import</a> <a id="15099" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="15120" class="Keyword">open</a> <a id="15125" class="Keyword">import</a> <a id="15132" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="15168" class="Keyword">open</a> <a id="15173" class="Keyword">import</a> <a id="15180" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="15223" class="Keyword">open</a> <a id="15228" class="Keyword">import</a> <a id="15235" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="15260" class="Keyword">open</a> <a id="15265" class="Keyword">import</a> <a id="15272" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="15303" class="Keyword">open</a> <a id="15308" class="Keyword">import</a> <a id="15315" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="15347" class="Keyword">open</a> <a id="15352" class="Keyword">import</a> <a id="15359" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="15393" class="Keyword">open</a> <a id="15398" class="Keyword">import</a> <a id="15405" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="15461" class="Keyword">open</a> <a id="15466" class="Keyword">import</a> <a id="15473" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="15526" class="Keyword">open</a> <a id="15531" class="Keyword">import</a> <a id="15538" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="15565" class="Keyword">open</a> <a id="15570" class="Keyword">import</a> <a id="15577" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="15639" class="Keyword">open</a> <a id="15644" class="Keyword">import</a> <a id="15651" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="15680" class="Keyword">open</a> <a id="15685" class="Keyword">import</a> <a id="15692" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="15719" class="Keyword">open</a> <a id="15724" class="Keyword">import</a> <a id="15731" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="15753" class="Keyword">open</a> <a id="15758" class="Keyword">import</a> <a id="15765" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="15795" class="Keyword">open</a> <a id="15800" class="Keyword">import</a> <a id="15807" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
</pre>
## Groups 

<pre class="Agda"><a id="15863" class="Keyword">open</a> <a id="15868" class="Keyword">import</a> <a id="15875" href="groups.html" class="Module">groups</a>
<a id="15882" class="Keyword">open</a> <a id="15887" class="Keyword">import</a> <a id="15894" href="groups.abstract-abelian-groups.html" class="Module">groups.abstract-abelian-groups</a>
<a id="15925" class="Keyword">open</a> <a id="15930" class="Keyword">import</a> <a id="15937" href="groups.abstract-abelian-subgroups.html" class="Module">groups.abstract-abelian-subgroups</a>
<a id="15971" class="Keyword">open</a> <a id="15976" class="Keyword">import</a> <a id="15983" href="groups.abstract-group-actions.html" class="Module">groups.abstract-group-actions</a>
<a id="16013" class="Keyword">open</a> <a id="16018" class="Keyword">import</a> <a id="16025" href="groups.abstract-group-torsors.html" class="Module">groups.abstract-group-torsors</a>
<a id="16055" class="Keyword">open</a> <a id="16060" class="Keyword">import</a> <a id="16067" href="groups.abstract-groups.html" class="Module">groups.abstract-groups</a>
<a id="16090" class="Keyword">open</a> <a id="16095" class="Keyword">import</a> <a id="16102" href="groups.abstract-subgroups.html" class="Module">groups.abstract-subgroups</a>
<a id="16128" class="Keyword">open</a> <a id="16133" class="Keyword">import</a> <a id="16140" href="groups.concrete-group-actions.html" class="Module">groups.concrete-group-actions</a>
<a id="16170" class="Keyword">open</a> <a id="16175" class="Keyword">import</a> <a id="16182" href="groups.concrete-groups.html" class="Module">groups.concrete-groups</a>
<a id="16205" class="Keyword">open</a> <a id="16210" class="Keyword">import</a> <a id="16217" href="groups.concrete-subgroups.html" class="Module">groups.concrete-subgroups</a>
<a id="16243" class="Keyword">open</a> <a id="16248" class="Keyword">import</a> <a id="16255" href="groups.examples-higher-groups.html" class="Module">groups.examples-higher-groups</a>
<a id="16285" class="Keyword">open</a> <a id="16290" class="Keyword">import</a> <a id="16297" href="groups.furstenberg-groups.html" class="Module">groups.furstenberg-groups</a>
<a id="16323" class="Keyword">open</a> <a id="16328" class="Keyword">import</a> <a id="16335" href="groups.higher-groups.html" class="Module">groups.higher-groups</a>
<a id="16356" class="Keyword">open</a> <a id="16361" class="Keyword">import</a> <a id="16368" href="groups.sheargroups.html" class="Module">groups.sheargroups</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="16419" class="Keyword">open</a> <a id="16424" class="Keyword">import</a> <a id="16431" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="16455" class="Keyword">open</a> <a id="16460" class="Keyword">import</a> <a id="16467" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="16520" class="Keyword">open</a> <a id="16525" class="Keyword">import</a> <a id="16532" href="order-theory.html" class="Module">order-theory</a>
<a id="16545" class="Keyword">open</a> <a id="16550" class="Keyword">import</a> <a id="16557" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="16584" class="Keyword">open</a> <a id="16589" class="Keyword">import</a> <a id="16596" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="16626" class="Keyword">open</a> <a id="16631" class="Keyword">import</a> <a id="16638" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="16674" class="Keyword">open</a> <a id="16679" class="Keyword">import</a> <a id="16686" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="16719" class="Keyword">open</a> <a id="16724" class="Keyword">import</a> <a id="16731" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="16751" class="Keyword">open</a> <a id="16756" class="Keyword">import</a> <a id="16763" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="16813" class="Keyword">open</a> <a id="16818" class="Keyword">import</a> <a id="16825" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Rings

<pre class="Agda"><a id="16877" class="Keyword">open</a> <a id="16882" class="Keyword">import</a> <a id="16889" href="rings.html" class="Module">rings</a>
<a id="16895" class="Keyword">open</a> <a id="16900" class="Keyword">import</a> <a id="16907" href="rings.eisenstein-integers.html" class="Module">rings.eisenstein-integers</a>
<a id="16933" class="Keyword">open</a> <a id="16938" class="Keyword">import</a> <a id="16945" href="rings.gaussian-integers.html" class="Module">rings.gaussian-integers</a>
<a id="16969" class="Keyword">open</a> <a id="16974" class="Keyword">import</a> <a id="16981" href="rings.ideals.html" class="Module">rings.ideals</a>
<a id="16994" class="Keyword">open</a> <a id="16999" class="Keyword">import</a> <a id="17006" href="rings.localizations-rings.html" class="Module">rings.localizations-rings</a>
<a id="17032" class="Keyword">open</a> <a id="17037" class="Keyword">import</a> <a id="17044" href="rings.rings-with-properties.html" class="Module">rings.rings-with-properties</a>
<a id="17072" class="Keyword">open</a> <a id="17077" class="Keyword">import</a> <a id="17084" href="rings.rings.html" class="Module">rings.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="17139" class="Keyword">open</a> <a id="17144" class="Keyword">import</a> <a id="17151" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="17177" class="Keyword">open</a> <a id="17182" class="Keyword">import</a> <a id="17189" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="17228" class="Keyword">open</a> <a id="17233" class="Keyword">import</a> <a id="17240" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="17278" class="Keyword">open</a> <a id="17283" class="Keyword">import</a> <a id="17290" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="17336" class="Keyword">open</a> <a id="17341" class="Keyword">import</a> <a id="17348" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="17385" class="Keyword">open</a> <a id="17390" class="Keyword">import</a> <a id="17397" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="17437" class="Keyword">open</a> <a id="17442" class="Keyword">import</a> <a id="17449" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="17488" class="Keyword">open</a> <a id="17493" class="Keyword">import</a> <a id="17500" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="17533" class="Keyword">open</a> <a id="17538" class="Keyword">import</a> <a id="17545" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="17584" class="Keyword">open</a> <a id="17589" class="Keyword">import</a> <a id="17596" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="17641" class="Keyword">open</a> <a id="17646" class="Keyword">import</a> <a id="17653" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="17705" class="Keyword">open</a> <a id="17710" class="Keyword">import</a> <a id="17717" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="17765" class="Keyword">open</a> <a id="17770" class="Keyword">import</a> <a id="17777" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="17817" class="Keyword">open</a> <a id="17822" class="Keyword">import</a> <a id="17829" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="17876" class="Keyword">open</a> <a id="17881" class="Keyword">import</a> <a id="17888" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="17926" class="Keyword">open</a> <a id="17931" class="Keyword">import</a> <a id="17938" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="17992" class="Keyword">open</a> <a id="17997" class="Keyword">import</a> <a id="18004" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="18051" class="Keyword">open</a> <a id="18056" class="Keyword">import</a> <a id="18063" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="18115" class="Keyword">open</a> <a id="18120" class="Keyword">import</a> <a id="18127" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="18172" class="Keyword">open</a> <a id="18177" class="Keyword">import</a> <a id="18184" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="18223" class="Keyword">open</a> <a id="18228" class="Keyword">import</a> <a id="18235" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="18275" class="Keyword">open</a> <a id="18280" class="Keyword">import</a> <a id="18287" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="18320" class="Keyword">open</a> <a id="18325" class="Keyword">import</a> <a id="18332" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="18377" class="Keyword">open</a> <a id="18382" class="Keyword">import</a> <a id="18389" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="18465" class="Keyword">open</a> <a id="18470" class="Keyword">import</a> <a id="18477" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="18539" class="Keyword">open</a> <a id="18544" class="Keyword">import</a> <a id="18551" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="18575" class="Keyword">open</a> <a id="18580" class="Keyword">import</a> <a id="18587" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="18627" class="Keyword">open</a> <a id="18632" class="Keyword">import</a> <a id="18639" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="18678" class="Keyword">open</a> <a id="18683" class="Keyword">import</a> <a id="18690" href="univalent-combinatorics.cartesian-product-finite-types.html" class="Module">univalent-combinatorics.cartesian-product-finite-types</a>
<a id="18745" class="Keyword">open</a> <a id="18750" class="Keyword">import</a> <a id="18757" href="univalent-combinatorics.coproduct-finite-types.html" class="Module">univalent-combinatorics.coproduct-finite-types</a>
<a id="18804" class="Keyword">open</a> <a id="18809" class="Keyword">import</a> <a id="18816" href="univalent-combinatorics.counting-cartesian-product-types.html" class="Module">univalent-combinatorics.counting-cartesian-product-types</a>
<a id="18873" class="Keyword">open</a> <a id="18878" class="Keyword">import</a> <a id="18885" href="univalent-combinatorics.counting-coproduct-types.html" class="Module">univalent-combinatorics.counting-coproduct-types</a>
<a id="18934" class="Keyword">open</a> <a id="18939" class="Keyword">import</a> <a id="18946" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="18998" class="Keyword">open</a> <a id="19003" class="Keyword">import</a> <a id="19010" href="univalent-combinatorics.counting-dependent-function-types.html" class="Module">univalent-combinatorics.counting-dependent-function-types</a>
<a id="19068" class="Keyword">open</a> <a id="19073" class="Keyword">import</a> <a id="19080" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="19134" class="Keyword">open</a> <a id="19139" class="Keyword">import</a> <a id="19146" href="univalent-combinatorics.counting-fibers-of-maps.html" class="Module">univalent-combinatorics.counting-fibers-of-maps</a>
<a id="19194" class="Keyword">open</a> <a id="19199" class="Keyword">import</a> <a id="19206" href="univalent-combinatorics.counting-function-types.html" class="Module">univalent-combinatorics.counting-function-types</a>
<a id="19254" class="Keyword">open</a> <a id="19259" class="Keyword">import</a> <a id="19266" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="19305" class="Keyword">open</a> <a id="19310" class="Keyword">import</a> <a id="19317" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="19350" class="Keyword">open</a> <a id="19355" class="Keyword">import</a> <a id="19362" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="19421" class="Keyword">open</a> <a id="19426" class="Keyword">import</a> <a id="19433" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="19488" class="Keyword">open</a> <a id="19493" class="Keyword">import</a> <a id="19500" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="19543" class="Keyword">open</a> <a id="19548" class="Keyword">import</a> <a id="19555" href="univalent-combinatorics.dependent-product-finite-types.html" class="Module">univalent-combinatorics.dependent-product-finite-types</a>
<a id="19610" class="Keyword">open</a> <a id="19615" class="Keyword">import</a> <a id="19622" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="19673" class="Keyword">open</a> <a id="19678" class="Keyword">import</a> <a id="19685" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="19763" class="Keyword">open</a> <a id="19768" class="Keyword">import</a> <a id="19775" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="19815" class="Keyword">open</a> <a id="19820" class="Keyword">import</a> <a id="19827" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="19884" class="Keyword">open</a> <a id="19889" class="Keyword">import</a> <a id="19896" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="19931" class="Keyword">open</a> <a id="19936" class="Keyword">import</a> <a id="19943" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="19989" class="Keyword">open</a> <a id="19994" class="Keyword">import</a> <a id="20001" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="20056" class="Keyword">open</a> <a id="20061" class="Keyword">import</a> <a id="20068" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="20127" class="Keyword">open</a> <a id="20132" class="Keyword">import</a> <a id="20139" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="20176" class="Keyword">open</a> <a id="20181" class="Keyword">import</a> <a id="20188" href="univalent-combinatorics.fibers-of-maps-between-finite-types.html" class="Module">univalent-combinatorics.fibers-of-maps-between-finite-types</a>
<a id="20248" class="Keyword">open</a> <a id="20253" class="Keyword">import</a> <a id="20260" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="20298" class="Keyword">open</a> <a id="20303" class="Keyword">import</a> <a id="20310" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="20362" class="Keyword">open</a> <a id="20367" class="Keyword">import</a> <a id="20374" href="univalent-combinatorics.finite-function-types.html" class="Module">univalent-combinatorics.finite-function-types</a>
<a id="20420" class="Keyword">open</a> <a id="20425" class="Keyword">import</a> <a id="20432" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="20477" class="Keyword">open</a> <a id="20482" class="Keyword">import</a> <a id="20489" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="20526" class="Keyword">open</a> <a id="20531" class="Keyword">import</a> <a id="20538" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="20587" class="Keyword">open</a> <a id="20592" class="Keyword">import</a> <a id="20599" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="20637" class="Keyword">open</a> <a id="20642" class="Keyword">import</a> <a id="20649" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="20704" class="Keyword">open</a> <a id="20709" class="Keyword">import</a> <a id="20716" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="20755" class="Keyword">open</a> <a id="20760" class="Keyword">import</a> <a id="20767" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="20797" class="Keyword">open</a> <a id="20802" class="Keyword">import</a> <a id="20809" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="20839" class="Keyword">open</a> <a id="20844" class="Keyword">import</a> <a id="20851" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="20891" class="Keyword">open</a> <a id="20896" class="Keyword">import</a> <a id="20903" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="20948" class="Keyword">open</a> <a id="20953" class="Keyword">import</a> <a id="20960" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="21010" class="Keyword">open</a> <a id="21015" class="Keyword">import</a> <a id="21022" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="21060" class="Keyword">open</a> <a id="21065" class="Keyword">import</a> <a id="21072" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="21121" class="Keyword">open</a> <a id="21126" class="Keyword">import</a> <a id="21133" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="21186" class="Keyword">open</a> <a id="21191" class="Keyword">import</a> <a id="21198" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="21244" class="Keyword">open</a> <a id="21249" class="Keyword">import</a> <a id="21256" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="21302" class="Keyword">open</a> <a id="21307" class="Keyword">import</a> <a id="21314" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="21362" class="Keyword">open</a> <a id="21367" class="Keyword">import</a> <a id="21374" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Univalent foundation

<pre class="Agda"><a id="21452" class="Keyword">open</a> <a id="21457" class="Keyword">import</a> <a id="21464" href="univalent-foundations.isolated-points.html" class="Module">univalent-foundations.isolated-points</a>
</pre>
### Wild algebra

<pre class="Agda"><a id="21533" class="Keyword">open</a> <a id="21538" class="Keyword">import</a> <a id="21545" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="21565" class="Keyword">open</a> <a id="21570" class="Keyword">import</a> <a id="21577" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="21628" class="Keyword">open</a> <a id="21633" class="Keyword">import</a> <a id="21640" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="21665" class="Keyword">open</a> <a id="21670" class="Keyword">import</a> <a id="21677" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="21703" class="Keyword">open</a> <a id="21708" class="Keyword">import</a> <a id="21715" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

