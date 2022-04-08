# Univalent mathematics in Agda

Welcome to the website of the `agda-unimath` formalization project.

[![build](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml)

<pre class="Agda"><a id="281" class="Symbol">{-#</a> <a id="285" class="Keyword">OPTIONS</a> <a id="293" class="Pragma">--without-K</a> <a id="305" class="Pragma">--exact-split</a> <a id="319" class="Symbol">#-}</a>
</pre>
## Category theory

<pre class="Agda"><a id="356" class="Keyword">open</a> <a id="361" class="Keyword">import</a> <a id="368" href="category-theory.html" class="Module">category-theory</a>
<a id="384" class="Keyword">open</a> <a id="389" class="Keyword">import</a> <a id="396" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="444" class="Keyword">open</a> <a id="449" class="Keyword">import</a> <a id="456" href="category-theory.anafunctors.html" class="Module">category-theory.anafunctors</a>
<a id="484" class="Keyword">open</a> <a id="489" class="Keyword">import</a> <a id="496" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="523" class="Keyword">open</a> <a id="528" class="Keyword">import</a> <a id="535" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="575" class="Keyword">open</a> <a id="580" class="Keyword">import</a> <a id="587" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="636" class="Keyword">open</a> <a id="641" class="Keyword">import</a> <a id="648" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="691" class="Keyword">open</a> <a id="696" class="Keyword">import</a> <a id="703" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="739" class="Keyword">open</a> <a id="744" class="Keyword">import</a> <a id="751" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="796" class="Keyword">open</a> <a id="801" class="Keyword">import</a> <a id="808" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="847" class="Keyword">open</a> <a id="852" class="Keyword">import</a> <a id="859" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="930" class="Keyword">open</a> <a id="935" class="Keyword">import</a> <a id="942" href="category-theory.initial-objects-precategories.html" class="Module">category-theory.initial-objects-precategories</a>
<a id="988" class="Keyword">open</a> <a id="993" class="Keyword">import</a> <a id="1000" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="1040" class="Keyword">open</a> <a id="1045" class="Keyword">import</a> <a id="1052" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="1101" class="Keyword">open</a> <a id="1106" class="Keyword">import</a> <a id="1113" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="1156" class="Keyword">open</a> <a id="1161" class="Keyword">import</a> <a id="1168" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="1201" class="Keyword">open</a> <a id="1206" class="Keyword">import</a> <a id="1213" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="1249" class="Keyword">open</a> <a id="1254" class="Keyword">import</a> <a id="1261" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="1311" class="Keyword">open</a> <a id="1316" class="Keyword">import</a> <a id="1323" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="1371" class="Keyword">open</a> <a id="1376" class="Keyword">import</a> <a id="1383" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="1440" class="Keyword">open</a> <a id="1445" class="Keyword">import</a> <a id="1452" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="1503" class="Keyword">open</a> <a id="1508" class="Keyword">import</a> <a id="1515" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="1566" class="Keyword">open</a> <a id="1571" class="Keyword">import</a> <a id="1578" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="1638" class="Keyword">open</a> <a id="1643" class="Keyword">import</a> <a id="1650" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="1704" class="Keyword">open</a> <a id="1709" class="Keyword">import</a> <a id="1716" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
<a id="1746" class="Keyword">open</a> <a id="1751" class="Keyword">import</a> <a id="1758" href="category-theory.slice-precategories.html" class="Module">category-theory.slice-precategories</a>
<a id="1794" class="Keyword">open</a> <a id="1799" class="Keyword">import</a> <a id="1806" href="category-theory.terminal-objects-precategories.html" class="Module">category-theory.terminal-objects-precategories</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="1895" class="Keyword">open</a> <a id="1900" class="Keyword">import</a> <a id="1907" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="1932" class="Keyword">open</a> <a id="1937" class="Keyword">import</a> <a id="1944" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="1993" class="Keyword">open</a> <a id="1998" class="Keyword">import</a> <a id="2005" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="2048" class="Keyword">open</a> <a id="2053" class="Keyword">import</a> <a id="2060" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="2110" class="Keyword">open</a> <a id="2115" class="Keyword">import</a> <a id="2122" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="2168" class="Keyword">open</a> <a id="2173" class="Keyword">import</a> <a id="2180" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="2227" class="Keyword">open</a> <a id="2232" class="Keyword">import</a> <a id="2239" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="2298" class="Keyword">open</a> <a id="2303" class="Keyword">import</a> <a id="2310" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="2351" class="Keyword">open</a> <a id="2356" class="Keyword">import</a> <a id="2363" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="2406" class="Keyword">open</a> <a id="2411" class="Keyword">import</a> <a id="2418" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="2462" class="Keyword">open</a> <a id="2467" class="Keyword">import</a> <a id="2474" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="2519" class="Keyword">open</a> <a id="2524" class="Keyword">import</a> <a id="2531" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="2583" class="Keyword">open</a> <a id="2588" class="Keyword">import</a> <a id="2595" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="2655" class="Keyword">open</a> <a id="2660" class="Keyword">import</a> <a id="2667" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="2708" class="Keyword">open</a> <a id="2713" class="Keyword">import</a> <a id="2720" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="2765" class="Keyword">open</a> <a id="2770" class="Keyword">import</a> <a id="2777" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="2824" class="Keyword">open</a> <a id="2829" class="Keyword">import</a> <a id="2836" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="2879" class="Keyword">open</a> <a id="2884" class="Keyword">import</a> <a id="2891" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="2941" class="Keyword">open</a> <a id="2946" class="Keyword">import</a> <a id="2953" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="3000" class="Keyword">open</a> <a id="3005" class="Keyword">import</a> <a id="3012" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="3069" class="Keyword">open</a> <a id="3074" class="Keyword">import</a> <a id="3081" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="3135" class="Keyword">open</a> <a id="3140" class="Keyword">import</a> <a id="3147" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="3207" class="Keyword">open</a> <a id="3212" class="Keyword">import</a> <a id="3219" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="3262" class="Keyword">open</a> <a id="3267" class="Keyword">import</a> <a id="3274" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="3324" class="Keyword">open</a> <a id="3329" class="Keyword">import</a> <a id="3336" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="3396" class="Keyword">open</a> <a id="3401" class="Keyword">import</a> <a id="3408" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="3457" class="Keyword">open</a> <a id="3462" class="Keyword">import</a> <a id="3469" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="3525" class="Keyword">open</a> <a id="3530" class="Keyword">import</a> <a id="3537" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="3573" class="Keyword">open</a> <a id="3578" class="Keyword">import</a> <a id="3585" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="3629" class="Keyword">open</a> <a id="3634" class="Keyword">import</a> <a id="3641" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="3685" class="Keyword">open</a> <a id="3690" class="Keyword">import</a> <a id="3697" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="3747" class="Keyword">open</a> <a id="3752" class="Keyword">import</a> <a id="3759" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="3805" class="Keyword">open</a> <a id="3810" class="Keyword">import</a> <a id="3817" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="3852" class="Keyword">open</a> <a id="3857" class="Keyword">import</a> <a id="3864" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="3909" class="Keyword">open</a> <a id="3914" class="Keyword">import</a> <a id="3921" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="3979" class="Keyword">open</a> <a id="3984" class="Keyword">import</a> <a id="3991" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="4056" class="Keyword">open</a> <a id="4061" class="Keyword">import</a> <a id="4068" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="4111" class="Keyword">open</a> <a id="4116" class="Keyword">import</a> <a id="4123" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="4177" class="Keyword">open</a> <a id="4182" class="Keyword">import</a> <a id="4189" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="4234" class="Keyword">open</a> <a id="4239" class="Keyword">import</a> <a id="4246" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="4298" class="Keyword">open</a> <a id="4303" class="Keyword">import</a> <a id="4310" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="4368" class="Keyword">open</a> <a id="4373" class="Keyword">import</a> <a id="4380" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="4426" class="Keyword">open</a> <a id="4431" class="Keyword">import</a> <a id="4438" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="4472" class="Keyword">open</a> <a id="4477" class="Keyword">import</a> <a id="4484" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="4529" class="Keyword">open</a> <a id="4534" class="Keyword">import</a> <a id="4541" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="4595" class="Keyword">open</a> <a id="4600" class="Keyword">import</a> <a id="4607" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="4656" class="Keyword">open</a> <a id="4661" class="Keyword">import</a> <a id="4668" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="4709" class="Keyword">open</a> <a id="4714" class="Keyword">import</a> <a id="4721" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="4770" class="Keyword">open</a> <a id="4775" class="Keyword">import</a> <a id="4782" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="4848" class="Keyword">open</a> <a id="4853" class="Keyword">import</a> <a id="4860" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="4904" class="Keyword">open</a> <a id="4909" class="Keyword">import</a> <a id="4916" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="4965" class="Keyword">open</a> <a id="4970" class="Keyword">import</a> <a id="4977" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="5033" class="Keyword">open</a> <a id="5038" class="Keyword">import</a> <a id="5045" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="5086" class="Keyword">open</a> <a id="5091" class="Keyword">import</a> <a id="5098" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="5147" class="Keyword">open</a> <a id="5152" class="Keyword">import</a> <a id="5159" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="5218" class="Keyword">open</a> <a id="5223" class="Keyword">import</a> <a id="5230" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="5269" class="Keyword">open</a> <a id="5274" class="Keyword">import</a> <a id="5281" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="5334" class="Keyword">open</a> <a id="5339" class="Keyword">import</a> <a id="5346" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="5403" class="Keyword">open</a> <a id="5408" class="Keyword">import</a> <a id="5415" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="5457" class="Keyword">open</a> <a id="5462" class="Keyword">import</a> <a id="5469" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="5520" class="Keyword">open</a> <a id="5525" class="Keyword">import</a> <a id="5532" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="5590" class="Keyword">open</a> <a id="5595" class="Keyword">import</a> <a id="5602" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="5666" class="Keyword">open</a> <a id="5671" class="Keyword">import</a> <a id="5678" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="5731" class="Keyword">open</a> <a id="5736" class="Keyword">import</a> <a id="5743" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="5796" class="Keyword">open</a> <a id="5801" class="Keyword">import</a> <a id="5808" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="5869" class="Keyword">open</a> <a id="5874" class="Keyword">import</a> <a id="5881" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="5939" class="Keyword">open</a> <a id="5944" class="Keyword">import</a> <a id="5951" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="6000" class="Keyword">open</a> <a id="6005" class="Keyword">import</a> <a id="6012" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="6056" class="Keyword">open</a> <a id="6061" class="Keyword">import</a> <a id="6068" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="6111" class="Keyword">open</a> <a id="6116" class="Keyword">import</a> <a id="6123" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="6170" class="Keyword">open</a> <a id="6175" class="Keyword">import</a> <a id="6182" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="6243" class="Keyword">open</a> <a id="6248" class="Keyword">import</a> <a id="6255" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="6318" class="Keyword">open</a> <a id="6323" class="Keyword">import</a> <a id="6330" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="6390" class="Keyword">open</a> <a id="6395" class="Keyword">import</a> <a id="6402" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="6456" class="Keyword">open</a> <a id="6461" class="Keyword">import</a> <a id="6468" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="6533" class="Keyword">open</a> <a id="6538" class="Keyword">import</a> <a id="6545" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="6653" class="Keyword">open</a> <a id="6658" class="Keyword">import</a> <a id="6665" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="6685" class="Keyword">open</a> <a id="6690" class="Keyword">import</a> <a id="6697" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="6743" class="Keyword">open</a> <a id="6748" class="Keyword">import</a> <a id="6755" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="6801" class="Keyword">open</a> <a id="6806" class="Keyword">import</a> <a id="6813" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="6847" class="Keyword">open</a> <a id="6852" class="Keyword">import</a> <a id="6859" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="6894" class="Keyword">open</a> <a id="6899" class="Keyword">import</a> <a id="6906" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="6944" class="Keyword">open</a> <a id="6949" class="Keyword">import</a> <a id="6956" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="6994" class="Keyword">open</a> <a id="6999" class="Keyword">import</a> <a id="7006" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="7046" class="Keyword">open</a> <a id="7051" class="Keyword">import</a> <a id="7058" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="7091" class="Keyword">open</a> <a id="7096" class="Keyword">import</a> <a id="7103" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="7141" class="Keyword">open</a> <a id="7146" class="Keyword">import</a> <a id="7153" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="7216" class="Keyword">open</a> <a id="7221" class="Keyword">import</a> <a id="7228" href="foundation.html" class="Module">foundation</a>
<a id="7239" class="Keyword">open</a> <a id="7244" class="Keyword">import</a> <a id="7251" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="7269" class="Keyword">open</a> <a id="7274" class="Keyword">import</a> <a id="7281" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="7300" class="Keyword">open</a> <a id="7305" class="Keyword">import</a> <a id="7312" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="7331" class="Keyword">open</a> <a id="7336" class="Keyword">import</a> <a id="7343" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="7387" class="Keyword">open</a> <a id="7392" class="Keyword">import</a> <a id="7399" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="7424" class="Keyword">open</a> <a id="7429" class="Keyword">import</a> <a id="7436" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="7463" class="Keyword">open</a> <a id="7468" class="Keyword">import</a> <a id="7475" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="7504" class="Keyword">open</a> <a id="7509" class="Keyword">import</a> <a id="7516" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="7547" class="Keyword">open</a> <a id="7552" class="Keyword">import</a> <a id="7559" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="7587" class="Keyword">open</a> <a id="7592" class="Keyword">import</a> <a id="7599" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="7629" class="Keyword">open</a> <a id="7634" class="Keyword">import</a> <a id="7641" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="7661" class="Keyword">open</a> <a id="7666" class="Keyword">import</a> <a id="7673" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="7710" class="Keyword">open</a> <a id="7715" class="Keyword">import</a> <a id="7722" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="7757" class="Keyword">open</a> <a id="7762" class="Keyword">import</a> <a id="7769" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="7827" class="Keyword">open</a> <a id="7832" class="Keyword">import</a> <a id="7839" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="7877" class="Keyword">open</a> <a id="7882" class="Keyword">import</a> <a id="7889" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="7918" class="Keyword">open</a> <a id="7923" class="Keyword">import</a> <a id="7930" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="7953" class="Keyword">open</a> <a id="7958" class="Keyword">import</a> <a id="7965" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="7988" class="Keyword">open</a> <a id="7993" class="Keyword">import</a> <a id="8000" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="8042" class="Keyword">open</a> <a id="8047" class="Keyword">import</a> <a id="8054" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="8086" class="Keyword">open</a> <a id="8091" class="Keyword">import</a> <a id="8098" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="8125" class="Keyword">open</a> <a id="8130" class="Keyword">import</a> <a id="8137" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="8162" class="Keyword">open</a> <a id="8167" class="Keyword">import</a> <a id="8174" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="8203" class="Keyword">open</a> <a id="8208" class="Keyword">import</a> <a id="8215" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="8245" class="Keyword">open</a> <a id="8250" class="Keyword">import</a> <a id="8257" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="8284" class="Keyword">open</a> <a id="8289" class="Keyword">import</a> <a id="8296" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="8315" class="Keyword">open</a> <a id="8320" class="Keyword">import</a> <a id="8327" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="8373" class="Keyword">open</a> <a id="8378" class="Keyword">import</a> <a id="8385" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="8427" class="Keyword">open</a> <a id="8432" class="Keyword">import</a> <a id="8439" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="8471" class="Keyword">open</a> <a id="8476" class="Keyword">import</a> <a id="8483" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="8513" class="Keyword">open</a> <a id="8518" class="Keyword">import</a> <a id="8525" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="8551" class="Keyword">open</a> <a id="8556" class="Keyword">import</a> <a id="8563" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="8597" class="Keyword">open</a> <a id="8602" class="Keyword">import</a> <a id="8609" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="8639" class="Keyword">open</a> <a id="8644" class="Keyword">import</a> <a id="8651" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="8678" class="Keyword">open</a> <a id="8683" class="Keyword">import</a> <a id="8690" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="8722" class="Keyword">open</a> <a id="8727" class="Keyword">import</a> <a id="8734" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="8768" class="Keyword">open</a> <a id="8773" class="Keyword">import</a> <a id="8780" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="8803" class="Keyword">open</a> <a id="8808" class="Keyword">import</a> <a id="8815" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="8885" class="Keyword">open</a> <a id="8890" class="Keyword">import</a> <a id="8897" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="8967" class="Keyword">open</a> <a id="8972" class="Keyword">import</a> <a id="8979" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="9006" class="Keyword">open</a> <a id="9011" class="Keyword">import</a> <a id="9018" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="9066" class="Keyword">open</a> <a id="9071" class="Keyword">import</a> <a id="9078" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="9118" class="Keyword">open</a> <a id="9123" class="Keyword">import</a> <a id="9130" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="9152" class="Keyword">open</a> <a id="9157" class="Keyword">import</a> <a id="9164" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="9187" class="Keyword">open</a> <a id="9192" class="Keyword">import</a> <a id="9199" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="9244" class="Keyword">open</a> <a id="9249" class="Keyword">import</a> <a id="9256" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="9300" class="Keyword">open</a> <a id="9305" class="Keyword">import</a> <a id="9312" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="9348" class="Keyword">open</a> <a id="9353" class="Keyword">import</a> <a id="9360" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="9405" class="Keyword">open</a> <a id="9410" class="Keyword">import</a> <a id="9417" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="9458" class="Keyword">open</a> <a id="9463" class="Keyword">import</a> <a id="9470" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="9505" class="Keyword">open</a> <a id="9510" class="Keyword">import</a> <a id="9517" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="9548" class="Keyword">open</a> <a id="9553" class="Keyword">import</a> <a id="9560" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="9593" class="Keyword">open</a> <a id="9598" class="Keyword">import</a> <a id="9605" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="9638" class="Keyword">open</a> <a id="9643" class="Keyword">import</a> <a id="9650" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="9680" class="Keyword">open</a> <a id="9685" class="Keyword">import</a> <a id="9692" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="9716" class="Keyword">open</a> <a id="9721" class="Keyword">import</a> <a id="9728" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="9766" class="Keyword">open</a> <a id="9771" class="Keyword">import</a> <a id="9778" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="9809" class="Keyword">open</a> <a id="9814" class="Keyword">import</a> <a id="9821" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="9846" class="Keyword">open</a> <a id="9851" class="Keyword">import</a> <a id="9858" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="9886" class="Keyword">open</a> <a id="9891" class="Keyword">import</a> <a id="9898" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="9922" class="Keyword">open</a> <a id="9927" class="Keyword">import</a> <a id="9934" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="9960" class="Keyword">open</a> <a id="9965" class="Keyword">import</a> <a id="9972" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="10007" class="Keyword">open</a> <a id="10012" class="Keyword">import</a> <a id="10019" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="10040" class="Keyword">open</a> <a id="10045" class="Keyword">import</a> <a id="10052" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="10101" class="Keyword">open</a> <a id="10106" class="Keyword">import</a> <a id="10113" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="10154" class="Keyword">open</a> <a id="10159" class="Keyword">import</a> <a id="10166" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="10216" class="Keyword">open</a> <a id="10221" class="Keyword">import</a> <a id="10228" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="10274" class="Keyword">open</a> <a id="10279" class="Keyword">import</a> <a id="10286" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="10326" class="Keyword">open</a> <a id="10331" class="Keyword">import</a> <a id="10338" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="10388" class="Keyword">open</a> <a id="10393" class="Keyword">import</a> <a id="10400" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="10439" class="Keyword">open</a> <a id="10444" class="Keyword">import</a> <a id="10451" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="10491" class="Keyword">open</a> <a id="10496" class="Keyword">import</a> <a id="10503" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="10536" class="Keyword">open</a> <a id="10541" class="Keyword">import</a> <a id="10548" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="10597" class="Keyword">open</a> <a id="10602" class="Keyword">import</a> <a id="10609" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="10634" class="Keyword">open</a> <a id="10639" class="Keyword">import</a> <a id="10646" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="10684" class="Keyword">open</a> <a id="10689" class="Keyword">import</a> <a id="10696" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="10718" class="Keyword">open</a> <a id="10723" class="Keyword">import</a> <a id="10730" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="10758" class="Keyword">open</a> <a id="10763" class="Keyword">import</a> <a id="10770" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="10796" class="Keyword">open</a> <a id="10801" class="Keyword">import</a> <a id="10808" href="foundation.images.html" class="Module">foundation.images</a>
<a id="10826" class="Keyword">open</a> <a id="10831" class="Keyword">import</a> <a id="10838" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="10873" class="Keyword">open</a> <a id="10878" class="Keyword">import</a> <a id="10885" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="10912" class="Keyword">open</a> <a id="10917" class="Keyword">import</a> <a id="10924" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="10980" class="Keyword">open</a> <a id="10985" class="Keyword">import</a> <a id="10992" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="11021" class="Keyword">open</a> <a id="11026" class="Keyword">import</a> <a id="11033" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="11063" class="Keyword">open</a> <a id="11068" class="Keyword">import</a> <a id="11075" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="11101" class="Keyword">open</a> <a id="11106" class="Keyword">import</a> <a id="11113" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="11140" class="Keyword">open</a> <a id="11145" class="Keyword">import</a> <a id="11152" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="11175" class="Keyword">open</a> <a id="11180" class="Keyword">import</a> <a id="11187" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="11214" class="Keyword">open</a> <a id="11219" class="Keyword">import</a> <a id="11226" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="11258" class="Keyword">open</a> <a id="11263" class="Keyword">import</a> <a id="11270" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="11304" class="Keyword">open</a> <a id="11309" class="Keyword">import</a> <a id="11316" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="11356" class="Keyword">open</a> <a id="11361" class="Keyword">import</a> <a id="11368" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="11399" class="Keyword">open</a> <a id="11404" class="Keyword">import</a> <a id="11411" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="11443" class="Keyword">open</a> <a id="11448" class="Keyword">import</a> <a id="11455" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="11486" class="Keyword">open</a> <a id="11491" class="Keyword">import</a> <a id="11498" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="11515" class="Keyword">open</a> <a id="11520" class="Keyword">import</a> <a id="11527" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="11552" class="Keyword">open</a> <a id="11557" class="Keyword">import</a> <a id="11564" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="11593" class="Keyword">open</a> <a id="11598" class="Keyword">import</a> <a id="11605" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="11630" class="Keyword">open</a> <a id="11635" class="Keyword">import</a> <a id="11642" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="11663" class="Keyword">open</a> <a id="11668" class="Keyword">import</a> <a id="11675" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="11695" class="Keyword">open</a> <a id="11700" class="Keyword">import</a> <a id="11707" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="11741" class="Keyword">open</a> <a id="11746" class="Keyword">import</a> <a id="11753" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="11777" class="Keyword">open</a> <a id="11782" class="Keyword">import</a> <a id="11789" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="11816" class="Keyword">open</a> <a id="11821" class="Keyword">import</a> <a id="11828" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="11863" class="Keyword">open</a> <a id="11868" class="Keyword">import</a> <a id="11875" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="11915" class="Keyword">open</a> <a id="11920" class="Keyword">import</a> <a id="11927" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="11957" class="Keyword">open</a> <a id="11962" class="Keyword">import</a> <a id="11969" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="12006" class="Keyword">open</a> <a id="12011" class="Keyword">import</a> <a id="12018" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="12042" class="Keyword">open</a> <a id="12047" class="Keyword">import</a> <a id="12054" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="12075" class="Keyword">open</a> <a id="12080" class="Keyword">import</a> <a id="12087" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="12122" class="Keyword">open</a> <a id="12127" class="Keyword">import</a> <a id="12134" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="12171" class="Keyword">open</a> <a id="12176" class="Keyword">import</a> <a id="12183" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="12232" class="Keyword">open</a> <a id="12237" class="Keyword">import</a> <a id="12244" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="12267" class="Keyword">open</a> <a id="12272" class="Keyword">import</a> <a id="12279" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="12302" class="Keyword">open</a> <a id="12307" class="Keyword">import</a> <a id="12314" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="12342" class="Keyword">open</a> <a id="12347" class="Keyword">import</a> <a id="12354" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="12374" class="Keyword">open</a> <a id="12379" class="Keyword">import</a> <a id="12386" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="12417" class="Keyword">open</a> <a id="12422" class="Keyword">import</a> <a id="12429" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="12456" class="Keyword">open</a> <a id="12461" class="Keyword">import</a> <a id="12468" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="12484" class="Keyword">open</a> <a id="12489" class="Keyword">import</a> <a id="12496" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="12527" class="Keyword">open</a> <a id="12532" class="Keyword">import</a> <a id="12539" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="12556" class="Keyword">open</a> <a id="12561" class="Keyword">import</a> <a id="12568" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="12590" class="Keyword">open</a> <a id="12595" class="Keyword">import</a> <a id="12602" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="12629" class="Keyword">open</a> <a id="12634" class="Keyword">import</a> <a id="12641" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="12664" class="Keyword">open</a> <a id="12669" class="Keyword">import</a> <a id="12676" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="12703" class="Keyword">open</a> <a id="12708" class="Keyword">import</a> <a id="12715" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="12748" class="Keyword">open</a> <a id="12753" class="Keyword">import</a> <a id="12760" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="12800" class="Keyword">open</a> <a id="12805" class="Keyword">import</a> <a id="12812" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="12833" class="Keyword">open</a> <a id="12838" class="Keyword">import</a> <a id="12845" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="12874" class="Keyword">open</a> <a id="12879" class="Keyword">import</a> <a id="12886" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="12924" class="Keyword">open</a> <a id="12929" class="Keyword">import</a> <a id="12936" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="12956" class="Keyword">open</a> <a id="12961" class="Keyword">import</a> <a id="12968" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="12992" class="Keyword">open</a> <a id="12997" class="Keyword">import</a> <a id="13004" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="13031" class="Keyword">open</a> <a id="13036" class="Keyword">import</a> <a id="13043" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="13073" class="Keyword">open</a> <a id="13078" class="Keyword">import</a> <a id="13085" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="13111" class="Keyword">open</a> <a id="13116" class="Keyword">import</a> <a id="13123" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="13150" class="Keyword">open</a> <a id="13155" class="Keyword">import</a> <a id="13162" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="13191" class="Keyword">open</a> <a id="13196" class="Keyword">import</a> <a id="13203" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="13226" class="Keyword">open</a> <a id="13231" class="Keyword">import</a> <a id="13238" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="13289" class="Keyword">open</a> <a id="13294" class="Keyword">import</a> <a id="13301" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="13344" class="Keyword">open</a> <a id="13349" class="Keyword">import</a> <a id="13356" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="13404" class="Keyword">open</a> <a id="13409" class="Keyword">import</a> <a id="13416" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="13454" class="Keyword">open</a> <a id="13459" class="Keyword">import</a> <a id="13466" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="13503" class="Keyword">open</a> <a id="13508" class="Keyword">import</a> <a id="13515" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="13543" class="Keyword">open</a> <a id="13548" class="Keyword">import</a> <a id="13555" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="13591" class="Keyword">open</a> <a id="13596" class="Keyword">import</a> <a id="13603" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="13641" class="Keyword">open</a> <a id="13646" class="Keyword">import</a> <a id="13653" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="13686" class="Keyword">open</a> <a id="13691" class="Keyword">import</a> <a id="13698" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="13719" class="Keyword">open</a> <a id="13724" class="Keyword">import</a> <a id="13731" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="13785" class="Keyword">open</a> <a id="13790" class="Keyword">import</a> <a id="13797" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="13819" class="Keyword">open</a> <a id="13824" class="Keyword">import</a> <a id="13831" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="13866" class="Keyword">open</a> <a id="13871" class="Keyword">import</a> <a id="13878" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="13908" class="Keyword">open</a> <a id="13913" class="Keyword">import</a> <a id="13920" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="13959" class="Keyword">open</a> <a id="13964" class="Keyword">import</a> <a id="13971" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="14025" class="Keyword">open</a> <a id="14030" class="Keyword">import</a> <a id="14037" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="14083" class="Keyword">open</a> <a id="14088" class="Keyword">import</a> <a id="14095" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="14146" class="Keyword">open</a> <a id="14151" class="Keyword">import</a> <a id="14158" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="14199" class="Keyword">open</a> <a id="14204" class="Keyword">import</a> <a id="14211" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="14256" class="Keyword">open</a> <a id="14261" class="Keyword">import</a> <a id="14268" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="14313" class="Keyword">open</a> <a id="14318" class="Keyword">import</a> <a id="14325" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="14361" class="Keyword">open</a> <a id="14366" class="Keyword">import</a> <a id="14373" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="14409" class="Keyword">open</a> <a id="14414" class="Keyword">import</a> <a id="14421" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="14486" class="Keyword">open</a> <a id="14491" class="Keyword">import</a> <a id="14498" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="14553" class="Keyword">open</a> <a id="14558" class="Keyword">import</a> <a id="14565" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="14605" class="Keyword">open</a> <a id="14610" class="Keyword">import</a> <a id="14617" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="14661" class="Keyword">open</a> <a id="14666" class="Keyword">import</a> <a id="14673" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="14718" class="Keyword">open</a> <a id="14723" class="Keyword">import</a> <a id="14730" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="14771" class="Keyword">open</a> <a id="14776" class="Keyword">import</a> <a id="14783" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="14823" class="Keyword">open</a> <a id="14828" class="Keyword">import</a> <a id="14835" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="14862" class="Keyword">open</a> <a id="14867" class="Keyword">import</a> <a id="14874" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="14901" class="Keyword">open</a> <a id="14906" class="Keyword">import</a> <a id="14913" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="14932" class="Keyword">open</a> <a id="14937" class="Keyword">import</a> <a id="14944" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="14984" class="Keyword">open</a> <a id="14989" class="Keyword">import</a> <a id="14996" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="15061" class="Keyword">open</a> <a id="15066" class="Keyword">import</a> <a id="15073" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="15096" class="Keyword">open</a> <a id="15101" class="Keyword">import</a> <a id="15108" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="15132" class="Keyword">open</a> <a id="15137" class="Keyword">import</a> <a id="15144" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="15184" class="Keyword">open</a> <a id="15189" class="Keyword">import</a> <a id="15196" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="15239" class="Keyword">open</a> <a id="15244" class="Keyword">import</a> <a id="15251" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="15285" class="Keyword">open</a> <a id="15290" class="Keyword">import</a> <a id="15297" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="15327" class="Keyword">open</a> <a id="15332" class="Keyword">import</a> <a id="15339" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="15373" class="Keyword">open</a> <a id="15378" class="Keyword">import</a> <a id="15385" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="15420" class="Keyword">open</a> <a id="15425" class="Keyword">import</a> <a id="15432" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="15469" class="Keyword">open</a> <a id="15474" class="Keyword">import</a> <a id="15481" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="15508" class="Keyword">open</a> <a id="15513" class="Keyword">import</a> <a id="15520" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="15548" class="Keyword">open</a> <a id="15553" class="Keyword">import</a> <a id="15560" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="15609" class="Keyword">open</a> <a id="15614" class="Keyword">import</a> <a id="15621" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="15667" class="Keyword">open</a> <a id="15672" class="Keyword">import</a> <a id="15679" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="15719" class="Keyword">open</a> <a id="15724" class="Keyword">import</a> <a id="15731" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="15769" class="Keyword">open</a> <a id="15774" class="Keyword">import</a> <a id="15781" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="15810" class="Keyword">open</a> <a id="15815" class="Keyword">import</a> <a id="15822" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="15852" class="Keyword">open</a> <a id="15857" class="Keyword">import</a> <a id="15864" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="15895" class="Keyword">open</a> <a id="15900" class="Keyword">import</a> <a id="15907" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="15933" class="Keyword">open</a> <a id="15938" class="Keyword">import</a> <a id="15945" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="15996" class="Keyword">open</a> <a id="16001" class="Keyword">import</a> <a id="16008" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="16062" class="Keyword">open</a> <a id="16067" class="Keyword">import</a> <a id="16074" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="16101" class="Keyword">open</a> <a id="16106" class="Keyword">import</a> <a id="16113" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="16146" class="Keyword">open</a> <a id="16151" class="Keyword">import</a> <a id="16158" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="16189" class="Keyword">open</a> <a id="16194" class="Keyword">import</a> <a id="16201" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="16238" class="Keyword">open</a> <a id="16243" class="Keyword">import</a> <a id="16250" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="16275" class="Keyword">open</a> <a id="16280" class="Keyword">import</a> <a id="16287" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="16319" class="Keyword">open</a> <a id="16324" class="Keyword">import</a> <a id="16331" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="16366" class="Keyword">open</a> <a id="16371" class="Keyword">import</a> <a id="16378" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="16407" class="Keyword">open</a> <a id="16412" class="Keyword">import</a> <a id="16419" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="16447" class="Keyword">open</a> <a id="16452" class="Keyword">import</a> <a id="16459" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="16484" class="Keyword">open</a> <a id="16489" class="Keyword">import</a> <a id="16496" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="16517" class="Keyword">open</a> <a id="16522" class="Keyword">import</a> <a id="16529" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="16565" class="Keyword">open</a> <a id="16570" class="Keyword">import</a> <a id="16577" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="16620" class="Keyword">open</a> <a id="16625" class="Keyword">import</a> <a id="16632" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="16657" class="Keyword">open</a> <a id="16662" class="Keyword">import</a> <a id="16669" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="16700" class="Keyword">open</a> <a id="16705" class="Keyword">import</a> <a id="16712" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="16744" class="Keyword">open</a> <a id="16749" class="Keyword">import</a> <a id="16756" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="16790" class="Keyword">open</a> <a id="16795" class="Keyword">import</a> <a id="16802" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="16858" class="Keyword">open</a> <a id="16863" class="Keyword">import</a> <a id="16870" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="16923" class="Keyword">open</a> <a id="16928" class="Keyword">import</a> <a id="16935" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="16962" class="Keyword">open</a> <a id="16967" class="Keyword">import</a> <a id="16974" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="17036" class="Keyword">open</a> <a id="17041" class="Keyword">import</a> <a id="17048" href="graph-theory.html" class="Module">graph-theory</a>
<a id="17061" class="Keyword">open</a> <a id="17066" class="Keyword">import</a> <a id="17073" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="17114" class="Keyword">open</a> <a id="17119" class="Keyword">import</a> <a id="17126" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="17155" class="Keyword">open</a> <a id="17160" class="Keyword">import</a> <a id="17167" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="17212" class="Keyword">open</a> <a id="17217" class="Keyword">import</a> <a id="17224" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="17268" class="Keyword">open</a> <a id="17273" class="Keyword">import</a> <a id="17280" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="17307" class="Keyword">open</a> <a id="17312" class="Keyword">import</a> <a id="17319" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="17360" class="Keyword">open</a> <a id="17365" class="Keyword">import</a> <a id="17372" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="17395" class="Keyword">open</a> <a id="17400" class="Keyword">import</a> <a id="17407" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="17456" class="Keyword">open</a> <a id="17461" class="Keyword">import</a> <a id="17468" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="17507" class="Keyword">open</a> <a id="17512" class="Keyword">import</a> <a id="17519" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="17560" class="Keyword">open</a> <a id="17565" class="Keyword">import</a> <a id="17572" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="17616" class="Keyword">open</a> <a id="17621" class="Keyword">import</a> <a id="17628" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="17665" class="Keyword">open</a> <a id="17670" class="Keyword">import</a> <a id="17677" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="17699" class="Keyword">open</a> <a id="17704" class="Keyword">import</a> <a id="17711" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="17741" class="Keyword">open</a> <a id="17746" class="Keyword">import</a> <a id="17753" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="17792" class="Keyword">open</a> <a id="17797" class="Keyword">import</a> <a id="17804" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="17842" class="Keyword">open</a> <a id="17847" class="Keyword">import</a> <a id="17854" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="17885" class="Keyword">open</a> <a id="17890" class="Keyword">import</a> <a id="17897" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="17955" class="Keyword">open</a> <a id="17960" class="Keyword">import</a> <a id="17967" href="group-theory.html" class="Module">group-theory</a>
<a id="17980" class="Keyword">open</a> <a id="17985" class="Keyword">import</a> <a id="17992" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="18020" class="Keyword">open</a> <a id="18025" class="Keyword">import</a> <a id="18032" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="18063" class="Keyword">open</a> <a id="18068" class="Keyword">import</a> <a id="18075" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="18111" class="Keyword">open</a> <a id="18116" class="Keyword">import</a> <a id="18123" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="18174" class="Keyword">open</a> <a id="18179" class="Keyword">import</a> <a id="18186" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="18218" class="Keyword">open</a> <a id="18223" class="Keyword">import</a> <a id="18230" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="18266" class="Keyword">open</a> <a id="18271" class="Keyword">import</a> <a id="18278" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="18307" class="Keyword">open</a> <a id="18312" class="Keyword">import</a> <a id="18319" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="18355" class="Keyword">open</a> <a id="18360" class="Keyword">import</a> <a id="18367" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="18396" class="Keyword">open</a> <a id="18401" class="Keyword">import</a> <a id="18408" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="18440" class="Keyword">open</a> <a id="18445" class="Keyword">import</a> <a id="18452" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="18477" class="Keyword">open</a> <a id="18482" class="Keyword">import</a> <a id="18489" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="18520" class="Keyword">open</a> <a id="18525" class="Keyword">import</a> <a id="18532" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="18579" class="Keyword">open</a> <a id="18584" class="Keyword">import</a> <a id="18591" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="18631" class="Keyword">open</a> <a id="18636" class="Keyword">import</a> <a id="18643" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="18680" class="Keyword">open</a> <a id="18685" class="Keyword">import</a> <a id="18692" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="18728" class="Keyword">open</a> <a id="18733" class="Keyword">import</a> <a id="18740" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="18772" class="Keyword">open</a> <a id="18777" class="Keyword">import</a> <a id="18784" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="18811" class="Keyword">open</a> <a id="18816" class="Keyword">import</a> <a id="18823" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="18843" class="Keyword">open</a> <a id="18848" class="Keyword">import</a> <a id="18855" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="18882" class="Keyword">open</a> <a id="18887" class="Keyword">import</a> <a id="18894" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="18936" class="Keyword">open</a> <a id="18941" class="Keyword">import</a> <a id="18948" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="18989" class="Keyword">open</a> <a id="18994" class="Keyword">import</a> <a id="19001" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="19035" class="Keyword">open</a> <a id="19040" class="Keyword">import</a> <a id="19047" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="19082" class="Keyword">open</a> <a id="19087" class="Keyword">import</a> <a id="19094" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="19132" class="Keyword">open</a> <a id="19137" class="Keyword">import</a> <a id="19144" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="19176" class="Keyword">open</a> <a id="19181" class="Keyword">import</a> <a id="19188" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="19229" class="Keyword">open</a> <a id="19234" class="Keyword">import</a> <a id="19241" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="19282" class="Keyword">open</a> <a id="19287" class="Keyword">import</a> <a id="19294" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="19334" class="Keyword">open</a> <a id="19339" class="Keyword">import</a> <a id="19346" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="19379" class="Keyword">open</a> <a id="19384" class="Keyword">import</a> <a id="19391" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="19428" class="Keyword">open</a> <a id="19433" class="Keyword">import</a> <a id="19440" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="19485" class="Keyword">open</a> <a id="19490" class="Keyword">import</a> <a id="19497" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="19518" class="Keyword">open</a> <a id="19523" class="Keyword">import</a> <a id="19530" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="19564" class="Keyword">open</a> <a id="19569" class="Keyword">import</a> <a id="19576" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="19618" class="Keyword">open</a> <a id="19623" class="Keyword">import</a> <a id="19630" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="19665" class="Keyword">open</a> <a id="19670" class="Keyword">import</a> <a id="19677" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="19716" class="Keyword">open</a> <a id="19721" class="Keyword">import</a> <a id="19728" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="19765" class="Keyword">open</a> <a id="19770" class="Keyword">import</a> <a id="19777" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="19801" class="Keyword">open</a> <a id="19806" class="Keyword">import</a> <a id="19813" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="19838" class="Keyword">open</a> <a id="19843" class="Keyword">import</a> <a id="19850" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="19881" class="Keyword">open</a> <a id="19886" class="Keyword">import</a> <a id="19893" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="19916" class="Keyword">open</a> <a id="19921" class="Keyword">import</a> <a id="19928" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="19976" class="Keyword">open</a> <a id="19981" class="Keyword">import</a> <a id="19988" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="20018" class="Keyword">open</a> <a id="20023" class="Keyword">import</a> <a id="20030" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="20100" class="Keyword">open</a> <a id="20105" class="Keyword">import</a> <a id="20112" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="20127" class="Keyword">open</a> <a id="20132" class="Keyword">import</a> <a id="20139" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="20172" class="Keyword">open</a> <a id="20177" class="Keyword">import</a> <a id="20184" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="20216" class="Keyword">open</a> <a id="20221" class="Keyword">import</a> <a id="20228" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="20270" class="Keyword">open</a> <a id="20275" class="Keyword">import</a> <a id="20282" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="20320" class="Keyword">open</a> <a id="20325" class="Keyword">import</a> <a id="20332" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="20369" class="Keyword">open</a> <a id="20374" class="Keyword">import</a> <a id="20381" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="20414" class="Keyword">open</a> <a id="20419" class="Keyword">import</a> <a id="20426" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="20450" class="Keyword">open</a> <a id="20455" class="Keyword">import</a> <a id="20462" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="20501" class="Keyword">open</a> <a id="20506" class="Keyword">import</a> <a id="20513" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="20559" class="Keyword">open</a> <a id="20564" class="Keyword">import</a> <a id="20571" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="20616" class="Keyword">open</a> <a id="20621" class="Keyword">import</a> <a id="20628" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="20666" class="Keyword">open</a> <a id="20671" class="Keyword">import</a> <a id="20678" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="20710" class="Keyword">open</a> <a id="20715" class="Keyword">import</a> <a id="20722" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="20775" class="Keyword">open</a> <a id="20780" class="Keyword">import</a> <a id="20787" href="order-theory.html" class="Module">order-theory</a>
<a id="20800" class="Keyword">open</a> <a id="20805" class="Keyword">import</a> <a id="20812" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="20839" class="Keyword">open</a> <a id="20844" class="Keyword">import</a> <a id="20851" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="20881" class="Keyword">open</a> <a id="20886" class="Keyword">import</a> <a id="20893" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="20926" class="Keyword">open</a> <a id="20931" class="Keyword">import</a> <a id="20938" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="20974" class="Keyword">open</a> <a id="20979" class="Keyword">import</a> <a id="20986" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="21013" class="Keyword">open</a> <a id="21018" class="Keyword">import</a> <a id="21025" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="21055" class="Keyword">open</a> <a id="21060" class="Keyword">import</a> <a id="21067" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="21103" class="Keyword">open</a> <a id="21108" class="Keyword">import</a> <a id="21115" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="21157" class="Keyword">open</a> <a id="21162" class="Keyword">import</a> <a id="21169" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="21201" class="Keyword">open</a> <a id="21206" class="Keyword">import</a> <a id="21213" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="21250" class="Keyword">open</a> <a id="21255" class="Keyword">import</a> <a id="21262" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="21302" class="Keyword">open</a> <a id="21307" class="Keyword">import</a> <a id="21314" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="21349" class="Keyword">open</a> <a id="21354" class="Keyword">import</a> <a id="21361" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="21399" class="Keyword">open</a> <a id="21404" class="Keyword">import</a> <a id="21411" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="21446" class="Keyword">open</a> <a id="21451" class="Keyword">import</a> <a id="21458" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="21493" class="Keyword">open</a> <a id="21498" class="Keyword">import</a> <a id="21505" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="21543" class="Keyword">open</a> <a id="21548" class="Keyword">import</a> <a id="21555" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="21586" class="Keyword">open</a> <a id="21591" class="Keyword">import</a> <a id="21598" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="21631" class="Keyword">open</a> <a id="21636" class="Keyword">import</a> <a id="21643" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="21663" class="Keyword">open</a> <a id="21668" class="Keyword">import</a> <a id="21675" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="21698" class="Keyword">open</a> <a id="21703" class="Keyword">import</a> <a id="21710" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="21733" class="Keyword">open</a> <a id="21738" class="Keyword">import</a> <a id="21745" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="21771" class="Keyword">open</a> <a id="21776" class="Keyword">import</a> <a id="21783" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="21809" class="Keyword">open</a> <a id="21814" class="Keyword">import</a> <a id="21821" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="21877" class="Keyword">open</a> <a id="21882" class="Keyword">import</a> <a id="21889" href="polytopes.html" class="Module">polytopes</a>
<a id="21899" class="Keyword">open</a> <a id="21904" class="Keyword">import</a> <a id="21911" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="21969" class="Keyword">open</a> <a id="21974" class="Keyword">import</a> <a id="21981" href="ring-theory.html" class="Module">ring-theory</a>
<a id="21993" class="Keyword">open</a> <a id="21998" class="Keyword">import</a> <a id="22005" href="ring-theory.commutative-rings.html" class="Module">ring-theory.commutative-rings</a>
<a id="22035" class="Keyword">open</a> <a id="22040" class="Keyword">import</a> <a id="22047" href="ring-theory.discrete-fields.html" class="Module">ring-theory.discrete-fields</a>
<a id="22075" class="Keyword">open</a> <a id="22080" class="Keyword">import</a> <a id="22087" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="22114" class="Keyword">open</a> <a id="22119" class="Keyword">import</a> <a id="22126" href="ring-theory.eisenstein-integers.html" class="Module">ring-theory.eisenstein-integers</a>
<a id="22158" class="Keyword">open</a> <a id="22163" class="Keyword">import</a> <a id="22170" href="ring-theory.gaussian-integers.html" class="Module">ring-theory.gaussian-integers</a>
<a id="22200" class="Keyword">open</a> <a id="22205" class="Keyword">import</a> <a id="22212" href="ring-theory.homomorphisms-commutative-rings.html" class="Module">ring-theory.homomorphisms-commutative-rings</a>
<a id="22256" class="Keyword">open</a> <a id="22261" class="Keyword">import</a> <a id="22268" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="22300" class="Keyword">open</a> <a id="22305" class="Keyword">import</a> <a id="22312" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="22358" class="Keyword">open</a> <a id="22363" class="Keyword">import</a> <a id="22370" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="22395" class="Keyword">open</a> <a id="22400" class="Keyword">import</a> <a id="22407" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="22445" class="Keyword">open</a> <a id="22450" class="Keyword">import</a> <a id="22457" href="ring-theory.isomorphisms-commutative-rings.html" class="Module">ring-theory.isomorphisms-commutative-rings</a>
<a id="22500" class="Keyword">open</a> <a id="22505" class="Keyword">import</a> <a id="22512" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="22543" class="Keyword">open</a> <a id="22548" class="Keyword">import</a> <a id="22555" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="22587" class="Keyword">open</a> <a id="22592" class="Keyword">import</a> <a id="22599" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="22628" class="Keyword">open</a> <a id="22633" class="Keyword">import</a> <a id="22640" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="22701" class="Keyword">open</a> <a id="22706" class="Keyword">import</a> <a id="22713" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="22739" class="Keyword">open</a> <a id="22744" class="Keyword">import</a> <a id="22751" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="22790" class="Keyword">open</a> <a id="22795" class="Keyword">import</a> <a id="22802" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="22840" class="Keyword">open</a> <a id="22845" class="Keyword">import</a> <a id="22852" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="22898" class="Keyword">open</a> <a id="22903" class="Keyword">import</a> <a id="22910" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="22947" class="Keyword">open</a> <a id="22952" class="Keyword">import</a> <a id="22959" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="22999" class="Keyword">open</a> <a id="23004" class="Keyword">import</a> <a id="23011" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="23050" class="Keyword">open</a> <a id="23055" class="Keyword">import</a> <a id="23062" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="23095" class="Keyword">open</a> <a id="23100" class="Keyword">import</a> <a id="23107" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="23156" class="Keyword">open</a> <a id="23161" class="Keyword">import</a> <a id="23168" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="23207" class="Keyword">open</a> <a id="23212" class="Keyword">import</a> <a id="23219" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="23264" class="Keyword">open</a> <a id="23269" class="Keyword">import</a> <a id="23276" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="23328" class="Keyword">open</a> <a id="23333" class="Keyword">import</a> <a id="23340" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="23393" class="Keyword">open</a> <a id="23398" class="Keyword">import</a> <a id="23405" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="23453" class="Keyword">open</a> <a id="23458" class="Keyword">import</a> <a id="23465" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="23505" class="Keyword">open</a> <a id="23510" class="Keyword">import</a> <a id="23517" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="23564" class="Keyword">open</a> <a id="23569" class="Keyword">import</a> <a id="23576" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="23614" class="Keyword">open</a> <a id="23619" class="Keyword">import</a> <a id="23626" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="23680" class="Keyword">open</a> <a id="23685" class="Keyword">import</a> <a id="23692" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="23739" class="Keyword">open</a> <a id="23744" class="Keyword">import</a> <a id="23751" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="23803" class="Keyword">open</a> <a id="23808" class="Keyword">import</a> <a id="23815" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="23860" class="Keyword">open</a> <a id="23865" class="Keyword">import</a> <a id="23872" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="23911" class="Keyword">open</a> <a id="23916" class="Keyword">import</a> <a id="23923" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="23963" class="Keyword">open</a> <a id="23968" class="Keyword">import</a> <a id="23975" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="24008" class="Keyword">open</a> <a id="24013" class="Keyword">import</a> <a id="24020" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="24065" class="Keyword">open</a> <a id="24070" class="Keyword">import</a> <a id="24077" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="24153" class="Keyword">open</a> <a id="24158" class="Keyword">import</a> <a id="24165" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="24227" class="Keyword">open</a> <a id="24232" class="Keyword">import</a> <a id="24239" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="24263" class="Keyword">open</a> <a id="24268" class="Keyword">import</a> <a id="24275" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="24328" class="Keyword">open</a> <a id="24333" class="Keyword">import</a> <a id="24340" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="24383" class="Keyword">open</a> <a id="24388" class="Keyword">import</a> <a id="24395" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="24435" class="Keyword">open</a> <a id="24440" class="Keyword">import</a> <a id="24447" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="24486" class="Keyword">open</a> <a id="24491" class="Keyword">import</a> <a id="24498" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="24546" class="Keyword">open</a> <a id="24551" class="Keyword">import</a> <a id="24558" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="24605" class="Keyword">open</a> <a id="24610" class="Keyword">import</a> <a id="24617" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="24669" class="Keyword">open</a> <a id="24674" class="Keyword">import</a> <a id="24681" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="24721" class="Keyword">open</a> <a id="24726" class="Keyword">import</a> <a id="24733" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="24785" class="Keyword">open</a> <a id="24790" class="Keyword">import</a> <a id="24797" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="24851" class="Keyword">open</a> <a id="24856" class="Keyword">import</a> <a id="24863" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="24902" class="Keyword">open</a> <a id="24907" class="Keyword">import</a> <a id="24914" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="24947" class="Keyword">open</a> <a id="24952" class="Keyword">import</a> <a id="24959" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="24989" class="Keyword">open</a> <a id="24994" class="Keyword">import</a> <a id="25001" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="25060" class="Keyword">open</a> <a id="25065" class="Keyword">import</a> <a id="25072" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="25127" class="Keyword">open</a> <a id="25132" class="Keyword">import</a> <a id="25139" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="25182" class="Keyword">open</a> <a id="25187" class="Keyword">import</a> <a id="25194" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="25243" class="Keyword">open</a> <a id="25248" class="Keyword">import</a> <a id="25255" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="25300" class="Keyword">open</a> <a id="25305" class="Keyword">import</a> <a id="25312" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="25363" class="Keyword">open</a> <a id="25368" class="Keyword">import</a> <a id="25375" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="25453" class="Keyword">open</a> <a id="25458" class="Keyword">import</a> <a id="25465" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="25505" class="Keyword">open</a> <a id="25510" class="Keyword">import</a> <a id="25517" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="25574" class="Keyword">open</a> <a id="25579" class="Keyword">import</a> <a id="25586" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="25621" class="Keyword">open</a> <a id="25626" class="Keyword">import</a> <a id="25633" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="25679" class="Keyword">open</a> <a id="25684" class="Keyword">import</a> <a id="25691" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="25746" class="Keyword">open</a> <a id="25751" class="Keyword">import</a> <a id="25758" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="25801" class="Keyword">open</a> <a id="25806" class="Keyword">import</a> <a id="25813" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="25872" class="Keyword">open</a> <a id="25877" class="Keyword">import</a> <a id="25884" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="25921" class="Keyword">open</a> <a id="25926" class="Keyword">import</a> <a id="25933" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="25972" class="Keyword">open</a> <a id="25977" class="Keyword">import</a> <a id="25984" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="26022" class="Keyword">open</a> <a id="26027" class="Keyword">import</a> <a id="26034" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="26086" class="Keyword">open</a> <a id="26091" class="Keyword">import</a> <a id="26098" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="26143" class="Keyword">open</a> <a id="26148" class="Keyword">import</a> <a id="26155" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="26192" class="Keyword">open</a> <a id="26197" class="Keyword">import</a> <a id="26204" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="26253" class="Keyword">open</a> <a id="26258" class="Keyword">import</a> <a id="26265" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="26304" class="Keyword">open</a> <a id="26309" class="Keyword">import</a> <a id="26316" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="26354" class="Keyword">open</a> <a id="26359" class="Keyword">import</a> <a id="26366" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="26421" class="Keyword">open</a> <a id="26426" class="Keyword">import</a> <a id="26433" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="26472" class="Keyword">open</a> <a id="26477" class="Keyword">import</a> <a id="26484" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="26531" class="Keyword">open</a> <a id="26536" class="Keyword">import</a> <a id="26543" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="26573" class="Keyword">open</a> <a id="26578" class="Keyword">import</a> <a id="26585" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="26615" class="Keyword">open</a> <a id="26620" class="Keyword">import</a> <a id="26627" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="26670" class="Keyword">open</a> <a id="26675" class="Keyword">import</a> <a id="26682" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="26717" class="Keyword">open</a> <a id="26722" class="Keyword">import</a> <a id="26729" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="26769" class="Keyword">open</a> <a id="26774" class="Keyword">import</a> <a id="26781" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="26826" class="Keyword">open</a> <a id="26831" class="Keyword">import</a> <a id="26838" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="26888" class="Keyword">open</a> <a id="26893" class="Keyword">import</a> <a id="26900" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="26938" class="Keyword">open</a> <a id="26943" class="Keyword">import</a> <a id="26950" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="26999" class="Keyword">open</a> <a id="27004" class="Keyword">import</a> <a id="27011" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="27074" class="Keyword">open</a> <a id="27079" class="Keyword">import</a> <a id="27086" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="27118" class="Keyword">open</a> <a id="27123" class="Keyword">import</a> <a id="27130" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="27183" class="Keyword">open</a> <a id="27188" class="Keyword">import</a> <a id="27195" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="27241" class="Keyword">open</a> <a id="27246" class="Keyword">import</a> <a id="27253" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="27299" class="Keyword">open</a> <a id="27304" class="Keyword">import</a> <a id="27311" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="27359" class="Keyword">open</a> <a id="27364" class="Keyword">import</a> <a id="27371" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="27441" class="Keyword">open</a> <a id="27446" class="Keyword">import</a> <a id="27453" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="27466" class="Keyword">open</a> <a id="27471" class="Keyword">import</a> <a id="27478" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="27498" class="Keyword">open</a> <a id="27503" class="Keyword">import</a> <a id="27510" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="27540" class="Keyword">open</a> <a id="27545" class="Keyword">import</a> <a id="27552" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="27594" class="Keyword">open</a> <a id="27599" class="Keyword">import</a> <a id="27606" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="27657" class="Keyword">open</a> <a id="27662" class="Keyword">import</a> <a id="27669" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="27694" class="Keyword">open</a> <a id="27699" class="Keyword">import</a> <a id="27706" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="27730" class="Keyword">open</a> <a id="27735" class="Keyword">import</a> <a id="27742" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="27768" class="Keyword">open</a> <a id="27773" class="Keyword">import</a> <a id="27780" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="27810" class="Keyword">open</a> <a id="27815" class="Keyword">import</a> <a id="27822" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="27851" class="Keyword">open</a> <a id="27856" class="Keyword">import</a> <a id="27863" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

