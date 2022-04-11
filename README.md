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
<a id="9006" class="Keyword">open</a> <a id="9011" class="Keyword">import</a> <a id="9018" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="9055" class="Keyword">open</a> <a id="9060" class="Keyword">import</a> <a id="9067" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="9115" class="Keyword">open</a> <a id="9120" class="Keyword">import</a> <a id="9127" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="9167" class="Keyword">open</a> <a id="9172" class="Keyword">import</a> <a id="9179" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="9201" class="Keyword">open</a> <a id="9206" class="Keyword">import</a> <a id="9213" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="9236" class="Keyword">open</a> <a id="9241" class="Keyword">import</a> <a id="9248" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="9293" class="Keyword">open</a> <a id="9298" class="Keyword">import</a> <a id="9305" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="9349" class="Keyword">open</a> <a id="9354" class="Keyword">import</a> <a id="9361" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="9397" class="Keyword">open</a> <a id="9402" class="Keyword">import</a> <a id="9409" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="9454" class="Keyword">open</a> <a id="9459" class="Keyword">import</a> <a id="9466" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="9507" class="Keyword">open</a> <a id="9512" class="Keyword">import</a> <a id="9519" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="9554" class="Keyword">open</a> <a id="9559" class="Keyword">import</a> <a id="9566" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="9597" class="Keyword">open</a> <a id="9602" class="Keyword">import</a> <a id="9609" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="9642" class="Keyword">open</a> <a id="9647" class="Keyword">import</a> <a id="9654" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="9687" class="Keyword">open</a> <a id="9692" class="Keyword">import</a> <a id="9699" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="9729" class="Keyword">open</a> <a id="9734" class="Keyword">import</a> <a id="9741" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="9765" class="Keyword">open</a> <a id="9770" class="Keyword">import</a> <a id="9777" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="9815" class="Keyword">open</a> <a id="9820" class="Keyword">import</a> <a id="9827" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="9858" class="Keyword">open</a> <a id="9863" class="Keyword">import</a> <a id="9870" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="9895" class="Keyword">open</a> <a id="9900" class="Keyword">import</a> <a id="9907" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="9935" class="Keyword">open</a> <a id="9940" class="Keyword">import</a> <a id="9947" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="9971" class="Keyword">open</a> <a id="9976" class="Keyword">import</a> <a id="9983" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="10009" class="Keyword">open</a> <a id="10014" class="Keyword">import</a> <a id="10021" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="10056" class="Keyword">open</a> <a id="10061" class="Keyword">import</a> <a id="10068" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="10089" class="Keyword">open</a> <a id="10094" class="Keyword">import</a> <a id="10101" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="10150" class="Keyword">open</a> <a id="10155" class="Keyword">import</a> <a id="10162" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="10203" class="Keyword">open</a> <a id="10208" class="Keyword">import</a> <a id="10215" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="10265" class="Keyword">open</a> <a id="10270" class="Keyword">import</a> <a id="10277" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="10323" class="Keyword">open</a> <a id="10328" class="Keyword">import</a> <a id="10335" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="10375" class="Keyword">open</a> <a id="10380" class="Keyword">import</a> <a id="10387" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="10437" class="Keyword">open</a> <a id="10442" class="Keyword">import</a> <a id="10449" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="10488" class="Keyword">open</a> <a id="10493" class="Keyword">import</a> <a id="10500" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="10540" class="Keyword">open</a> <a id="10545" class="Keyword">import</a> <a id="10552" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="10585" class="Keyword">open</a> <a id="10590" class="Keyword">import</a> <a id="10597" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="10646" class="Keyword">open</a> <a id="10651" class="Keyword">import</a> <a id="10658" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="10683" class="Keyword">open</a> <a id="10688" class="Keyword">import</a> <a id="10695" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="10733" class="Keyword">open</a> <a id="10738" class="Keyword">import</a> <a id="10745" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="10767" class="Keyword">open</a> <a id="10772" class="Keyword">import</a> <a id="10779" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="10807" class="Keyword">open</a> <a id="10812" class="Keyword">import</a> <a id="10819" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="10845" class="Keyword">open</a> <a id="10850" class="Keyword">import</a> <a id="10857" href="foundation.images.html" class="Module">foundation.images</a>
<a id="10875" class="Keyword">open</a> <a id="10880" class="Keyword">import</a> <a id="10887" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="10922" class="Keyword">open</a> <a id="10927" class="Keyword">import</a> <a id="10934" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="10961" class="Keyword">open</a> <a id="10966" class="Keyword">import</a> <a id="10973" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="11029" class="Keyword">open</a> <a id="11034" class="Keyword">import</a> <a id="11041" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="11070" class="Keyword">open</a> <a id="11075" class="Keyword">import</a> <a id="11082" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="11112" class="Keyword">open</a> <a id="11117" class="Keyword">import</a> <a id="11124" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="11150" class="Keyword">open</a> <a id="11155" class="Keyword">import</a> <a id="11162" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="11189" class="Keyword">open</a> <a id="11194" class="Keyword">import</a> <a id="11201" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="11224" class="Keyword">open</a> <a id="11229" class="Keyword">import</a> <a id="11236" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="11263" class="Keyword">open</a> <a id="11268" class="Keyword">import</a> <a id="11275" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="11307" class="Keyword">open</a> <a id="11312" class="Keyword">import</a> <a id="11319" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="11353" class="Keyword">open</a> <a id="11358" class="Keyword">import</a> <a id="11365" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="11405" class="Keyword">open</a> <a id="11410" class="Keyword">import</a> <a id="11417" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="11448" class="Keyword">open</a> <a id="11453" class="Keyword">import</a> <a id="11460" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="11492" class="Keyword">open</a> <a id="11497" class="Keyword">import</a> <a id="11504" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="11535" class="Keyword">open</a> <a id="11540" class="Keyword">import</a> <a id="11547" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="11564" class="Keyword">open</a> <a id="11569" class="Keyword">import</a> <a id="11576" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="11601" class="Keyword">open</a> <a id="11606" class="Keyword">import</a> <a id="11613" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="11642" class="Keyword">open</a> <a id="11647" class="Keyword">import</a> <a id="11654" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="11679" class="Keyword">open</a> <a id="11684" class="Keyword">import</a> <a id="11691" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="11712" class="Keyword">open</a> <a id="11717" class="Keyword">import</a> <a id="11724" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="11744" class="Keyword">open</a> <a id="11749" class="Keyword">import</a> <a id="11756" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="11790" class="Keyword">open</a> <a id="11795" class="Keyword">import</a> <a id="11802" href="foundation.pairs-of-distinct-elements.html" class="Module">foundation.pairs-of-distinct-elements</a>
<a id="11840" class="Keyword">open</a> <a id="11845" class="Keyword">import</a> <a id="11852" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="11876" class="Keyword">open</a> <a id="11881" class="Keyword">import</a> <a id="11888" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="11915" class="Keyword">open</a> <a id="11920" class="Keyword">import</a> <a id="11927" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="11962" class="Keyword">open</a> <a id="11967" class="Keyword">import</a> <a id="11974" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="12010" class="Keyword">open</a> <a id="12015" class="Keyword">import</a> <a id="12022" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="12062" class="Keyword">open</a> <a id="12067" class="Keyword">import</a> <a id="12074" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="12104" class="Keyword">open</a> <a id="12109" class="Keyword">import</a> <a id="12116" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="12153" class="Keyword">open</a> <a id="12158" class="Keyword">import</a> <a id="12165" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="12189" class="Keyword">open</a> <a id="12194" class="Keyword">import</a> <a id="12201" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="12222" class="Keyword">open</a> <a id="12227" class="Keyword">import</a> <a id="12234" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="12269" class="Keyword">open</a> <a id="12274" class="Keyword">import</a> <a id="12281" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="12318" class="Keyword">open</a> <a id="12323" class="Keyword">import</a> <a id="12330" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="12379" class="Keyword">open</a> <a id="12384" class="Keyword">import</a> <a id="12391" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="12414" class="Keyword">open</a> <a id="12419" class="Keyword">import</a> <a id="12426" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="12449" class="Keyword">open</a> <a id="12454" class="Keyword">import</a> <a id="12461" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="12489" class="Keyword">open</a> <a id="12494" class="Keyword">import</a> <a id="12501" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="12521" class="Keyword">open</a> <a id="12526" class="Keyword">import</a> <a id="12533" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="12564" class="Keyword">open</a> <a id="12569" class="Keyword">import</a> <a id="12576" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="12603" class="Keyword">open</a> <a id="12608" class="Keyword">import</a> <a id="12615" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="12631" class="Keyword">open</a> <a id="12636" class="Keyword">import</a> <a id="12643" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="12674" class="Keyword">open</a> <a id="12679" class="Keyword">import</a> <a id="12686" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="12703" class="Keyword">open</a> <a id="12708" class="Keyword">import</a> <a id="12715" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="12737" class="Keyword">open</a> <a id="12742" class="Keyword">import</a> <a id="12749" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="12776" class="Keyword">open</a> <a id="12781" class="Keyword">import</a> <a id="12788" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="12811" class="Keyword">open</a> <a id="12816" class="Keyword">import</a> <a id="12823" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="12850" class="Keyword">open</a> <a id="12855" class="Keyword">import</a> <a id="12862" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="12895" class="Keyword">open</a> <a id="12900" class="Keyword">import</a> <a id="12907" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="12947" class="Keyword">open</a> <a id="12952" class="Keyword">import</a> <a id="12959" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="12980" class="Keyword">open</a> <a id="12985" class="Keyword">import</a> <a id="12992" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="13021" class="Keyword">open</a> <a id="13026" class="Keyword">import</a> <a id="13033" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="13071" class="Keyword">open</a> <a id="13076" class="Keyword">import</a> <a id="13083" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="13103" class="Keyword">open</a> <a id="13108" class="Keyword">import</a> <a id="13115" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="13139" class="Keyword">open</a> <a id="13144" class="Keyword">import</a> <a id="13151" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="13178" class="Keyword">open</a> <a id="13183" class="Keyword">import</a> <a id="13190" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="13220" class="Keyword">open</a> <a id="13225" class="Keyword">import</a> <a id="13232" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="13258" class="Keyword">open</a> <a id="13263" class="Keyword">import</a> <a id="13270" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="13297" class="Keyword">open</a> <a id="13302" class="Keyword">import</a> <a id="13309" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="13338" class="Keyword">open</a> <a id="13343" class="Keyword">import</a> <a id="13350" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="13373" class="Keyword">open</a> <a id="13378" class="Keyword">import</a> <a id="13385" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="13436" class="Keyword">open</a> <a id="13441" class="Keyword">import</a> <a id="13448" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="13491" class="Keyword">open</a> <a id="13496" class="Keyword">import</a> <a id="13503" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="13551" class="Keyword">open</a> <a id="13556" class="Keyword">import</a> <a id="13563" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="13601" class="Keyword">open</a> <a id="13606" class="Keyword">import</a> <a id="13613" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="13650" class="Keyword">open</a> <a id="13655" class="Keyword">import</a> <a id="13662" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="13690" class="Keyword">open</a> <a id="13695" class="Keyword">import</a> <a id="13702" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="13738" class="Keyword">open</a> <a id="13743" class="Keyword">import</a> <a id="13750" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="13788" class="Keyword">open</a> <a id="13793" class="Keyword">import</a> <a id="13800" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="13833" class="Keyword">open</a> <a id="13838" class="Keyword">import</a> <a id="13845" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="13866" class="Keyword">open</a> <a id="13871" class="Keyword">import</a> <a id="13878" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="13932" class="Keyword">open</a> <a id="13937" class="Keyword">import</a> <a id="13944" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="13966" class="Keyword">open</a> <a id="13971" class="Keyword">import</a> <a id="13978" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="14013" class="Keyword">open</a> <a id="14018" class="Keyword">import</a> <a id="14025" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="14055" class="Keyword">open</a> <a id="14060" class="Keyword">import</a> <a id="14067" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="14106" class="Keyword">open</a> <a id="14111" class="Keyword">import</a> <a id="14118" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="14172" class="Keyword">open</a> <a id="14177" class="Keyword">import</a> <a id="14184" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="14230" class="Keyword">open</a> <a id="14235" class="Keyword">import</a> <a id="14242" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="14293" class="Keyword">open</a> <a id="14298" class="Keyword">import</a> <a id="14305" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="14346" class="Keyword">open</a> <a id="14351" class="Keyword">import</a> <a id="14358" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="14403" class="Keyword">open</a> <a id="14408" class="Keyword">import</a> <a id="14415" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="14460" class="Keyword">open</a> <a id="14465" class="Keyword">import</a> <a id="14472" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="14508" class="Keyword">open</a> <a id="14513" class="Keyword">import</a> <a id="14520" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="14556" class="Keyword">open</a> <a id="14561" class="Keyword">import</a> <a id="14568" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="14633" class="Keyword">open</a> <a id="14638" class="Keyword">import</a> <a id="14645" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="14700" class="Keyword">open</a> <a id="14705" class="Keyword">import</a> <a id="14712" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="14752" class="Keyword">open</a> <a id="14757" class="Keyword">import</a> <a id="14764" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="14808" class="Keyword">open</a> <a id="14813" class="Keyword">import</a> <a id="14820" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="14865" class="Keyword">open</a> <a id="14870" class="Keyword">import</a> <a id="14877" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="14918" class="Keyword">open</a> <a id="14923" class="Keyword">import</a> <a id="14930" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="14970" class="Keyword">open</a> <a id="14975" class="Keyword">import</a> <a id="14982" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="15009" class="Keyword">open</a> <a id="15014" class="Keyword">import</a> <a id="15021" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="15048" class="Keyword">open</a> <a id="15053" class="Keyword">import</a> <a id="15060" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="15079" class="Keyword">open</a> <a id="15084" class="Keyword">import</a> <a id="15091" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="15131" class="Keyword">open</a> <a id="15136" class="Keyword">import</a> <a id="15143" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="15208" class="Keyword">open</a> <a id="15213" class="Keyword">import</a> <a id="15220" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="15243" class="Keyword">open</a> <a id="15248" class="Keyword">import</a> <a id="15255" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="15279" class="Keyword">open</a> <a id="15284" class="Keyword">import</a> <a id="15291" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="15331" class="Keyword">open</a> <a id="15336" class="Keyword">import</a> <a id="15343" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="15386" class="Keyword">open</a> <a id="15391" class="Keyword">import</a> <a id="15398" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="15432" class="Keyword">open</a> <a id="15437" class="Keyword">import</a> <a id="15444" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="15474" class="Keyword">open</a> <a id="15479" class="Keyword">import</a> <a id="15486" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="15520" class="Keyword">open</a> <a id="15525" class="Keyword">import</a> <a id="15532" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="15567" class="Keyword">open</a> <a id="15572" class="Keyword">import</a> <a id="15579" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="15616" class="Keyword">open</a> <a id="15621" class="Keyword">import</a> <a id="15628" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="15655" class="Keyword">open</a> <a id="15660" class="Keyword">import</a> <a id="15667" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="15695" class="Keyword">open</a> <a id="15700" class="Keyword">import</a> <a id="15707" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="15756" class="Keyword">open</a> <a id="15761" class="Keyword">import</a> <a id="15768" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="15814" class="Keyword">open</a> <a id="15819" class="Keyword">import</a> <a id="15826" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="15866" class="Keyword">open</a> <a id="15871" class="Keyword">import</a> <a id="15878" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="15916" class="Keyword">open</a> <a id="15921" class="Keyword">import</a> <a id="15928" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="15957" class="Keyword">open</a> <a id="15962" class="Keyword">import</a> <a id="15969" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="15999" class="Keyword">open</a> <a id="16004" class="Keyword">import</a> <a id="16011" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="16042" class="Keyword">open</a> <a id="16047" class="Keyword">import</a> <a id="16054" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="16080" class="Keyword">open</a> <a id="16085" class="Keyword">import</a> <a id="16092" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="16143" class="Keyword">open</a> <a id="16148" class="Keyword">import</a> <a id="16155" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="16209" class="Keyword">open</a> <a id="16214" class="Keyword">import</a> <a id="16221" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="16248" class="Keyword">open</a> <a id="16253" class="Keyword">import</a> <a id="16260" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="16293" class="Keyword">open</a> <a id="16298" class="Keyword">import</a> <a id="16305" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="16336" class="Keyword">open</a> <a id="16341" class="Keyword">import</a> <a id="16348" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="16385" class="Keyword">open</a> <a id="16390" class="Keyword">import</a> <a id="16397" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="16422" class="Keyword">open</a> <a id="16427" class="Keyword">import</a> <a id="16434" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="16466" class="Keyword">open</a> <a id="16471" class="Keyword">import</a> <a id="16478" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="16513" class="Keyword">open</a> <a id="16518" class="Keyword">import</a> <a id="16525" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="16554" class="Keyword">open</a> <a id="16559" class="Keyword">import</a> <a id="16566" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="16594" class="Keyword">open</a> <a id="16599" class="Keyword">import</a> <a id="16606" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="16631" class="Keyword">open</a> <a id="16636" class="Keyword">import</a> <a id="16643" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="16664" class="Keyword">open</a> <a id="16669" class="Keyword">import</a> <a id="16676" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="16712" class="Keyword">open</a> <a id="16717" class="Keyword">import</a> <a id="16724" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="16767" class="Keyword">open</a> <a id="16772" class="Keyword">import</a> <a id="16779" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="16804" class="Keyword">open</a> <a id="16809" class="Keyword">import</a> <a id="16816" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="16847" class="Keyword">open</a> <a id="16852" class="Keyword">import</a> <a id="16859" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="16891" class="Keyword">open</a> <a id="16896" class="Keyword">import</a> <a id="16903" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="16937" class="Keyword">open</a> <a id="16942" class="Keyword">import</a> <a id="16949" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="17005" class="Keyword">open</a> <a id="17010" class="Keyword">import</a> <a id="17017" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="17070" class="Keyword">open</a> <a id="17075" class="Keyword">import</a> <a id="17082" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="17109" class="Keyword">open</a> <a id="17114" class="Keyword">import</a> <a id="17121" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="17183" class="Keyword">open</a> <a id="17188" class="Keyword">import</a> <a id="17195" href="graph-theory.html" class="Module">graph-theory</a>
<a id="17208" class="Keyword">open</a> <a id="17213" class="Keyword">import</a> <a id="17220" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="17261" class="Keyword">open</a> <a id="17266" class="Keyword">import</a> <a id="17273" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="17302" class="Keyword">open</a> <a id="17307" class="Keyword">import</a> <a id="17314" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="17359" class="Keyword">open</a> <a id="17364" class="Keyword">import</a> <a id="17371" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="17415" class="Keyword">open</a> <a id="17420" class="Keyword">import</a> <a id="17427" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="17454" class="Keyword">open</a> <a id="17459" class="Keyword">import</a> <a id="17466" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="17507" class="Keyword">open</a> <a id="17512" class="Keyword">import</a> <a id="17519" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="17542" class="Keyword">open</a> <a id="17547" class="Keyword">import</a> <a id="17554" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="17603" class="Keyword">open</a> <a id="17608" class="Keyword">import</a> <a id="17615" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="17654" class="Keyword">open</a> <a id="17659" class="Keyword">import</a> <a id="17666" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="17707" class="Keyword">open</a> <a id="17712" class="Keyword">import</a> <a id="17719" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="17763" class="Keyword">open</a> <a id="17768" class="Keyword">import</a> <a id="17775" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="17812" class="Keyword">open</a> <a id="17817" class="Keyword">import</a> <a id="17824" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="17846" class="Keyword">open</a> <a id="17851" class="Keyword">import</a> <a id="17858" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="17888" class="Keyword">open</a> <a id="17893" class="Keyword">import</a> <a id="17900" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="17939" class="Keyword">open</a> <a id="17944" class="Keyword">import</a> <a id="17951" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="17989" class="Keyword">open</a> <a id="17994" class="Keyword">import</a> <a id="18001" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="18032" class="Keyword">open</a> <a id="18037" class="Keyword">import</a> <a id="18044" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="18102" class="Keyword">open</a> <a id="18107" class="Keyword">import</a> <a id="18114" href="group-theory.html" class="Module">group-theory</a>
<a id="18127" class="Keyword">open</a> <a id="18132" class="Keyword">import</a> <a id="18139" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="18167" class="Keyword">open</a> <a id="18172" class="Keyword">import</a> <a id="18179" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="18210" class="Keyword">open</a> <a id="18215" class="Keyword">import</a> <a id="18222" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="18258" class="Keyword">open</a> <a id="18263" class="Keyword">import</a> <a id="18270" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="18321" class="Keyword">open</a> <a id="18326" class="Keyword">import</a> <a id="18333" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="18365" class="Keyword">open</a> <a id="18370" class="Keyword">import</a> <a id="18377" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="18413" class="Keyword">open</a> <a id="18418" class="Keyword">import</a> <a id="18425" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="18454" class="Keyword">open</a> <a id="18459" class="Keyword">import</a> <a id="18466" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="18502" class="Keyword">open</a> <a id="18507" class="Keyword">import</a> <a id="18514" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="18543" class="Keyword">open</a> <a id="18548" class="Keyword">import</a> <a id="18555" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="18587" class="Keyword">open</a> <a id="18592" class="Keyword">import</a> <a id="18599" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="18624" class="Keyword">open</a> <a id="18629" class="Keyword">import</a> <a id="18636" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="18667" class="Keyword">open</a> <a id="18672" class="Keyword">import</a> <a id="18679" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="18726" class="Keyword">open</a> <a id="18731" class="Keyword">import</a> <a id="18738" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="18778" class="Keyword">open</a> <a id="18783" class="Keyword">import</a> <a id="18790" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="18827" class="Keyword">open</a> <a id="18832" class="Keyword">import</a> <a id="18839" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="18875" class="Keyword">open</a> <a id="18880" class="Keyword">import</a> <a id="18887" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="18919" class="Keyword">open</a> <a id="18924" class="Keyword">import</a> <a id="18931" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="18958" class="Keyword">open</a> <a id="18963" class="Keyword">import</a> <a id="18970" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="18990" class="Keyword">open</a> <a id="18995" class="Keyword">import</a> <a id="19002" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="19029" class="Keyword">open</a> <a id="19034" class="Keyword">import</a> <a id="19041" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="19083" class="Keyword">open</a> <a id="19088" class="Keyword">import</a> <a id="19095" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="19136" class="Keyword">open</a> <a id="19141" class="Keyword">import</a> <a id="19148" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="19182" class="Keyword">open</a> <a id="19187" class="Keyword">import</a> <a id="19194" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="19229" class="Keyword">open</a> <a id="19234" class="Keyword">import</a> <a id="19241" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="19279" class="Keyword">open</a> <a id="19284" class="Keyword">import</a> <a id="19291" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="19323" class="Keyword">open</a> <a id="19328" class="Keyword">import</a> <a id="19335" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="19376" class="Keyword">open</a> <a id="19381" class="Keyword">import</a> <a id="19388" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="19429" class="Keyword">open</a> <a id="19434" class="Keyword">import</a> <a id="19441" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="19481" class="Keyword">open</a> <a id="19486" class="Keyword">import</a> <a id="19493" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="19526" class="Keyword">open</a> <a id="19531" class="Keyword">import</a> <a id="19538" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="19575" class="Keyword">open</a> <a id="19580" class="Keyword">import</a> <a id="19587" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="19632" class="Keyword">open</a> <a id="19637" class="Keyword">import</a> <a id="19644" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="19665" class="Keyword">open</a> <a id="19670" class="Keyword">import</a> <a id="19677" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="19711" class="Keyword">open</a> <a id="19716" class="Keyword">import</a> <a id="19723" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="19765" class="Keyword">open</a> <a id="19770" class="Keyword">import</a> <a id="19777" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="19812" class="Keyword">open</a> <a id="19817" class="Keyword">import</a> <a id="19824" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="19863" class="Keyword">open</a> <a id="19868" class="Keyword">import</a> <a id="19875" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="19912" class="Keyword">open</a> <a id="19917" class="Keyword">import</a> <a id="19924" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="19948" class="Keyword">open</a> <a id="19953" class="Keyword">import</a> <a id="19960" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="19985" class="Keyword">open</a> <a id="19990" class="Keyword">import</a> <a id="19997" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="20028" class="Keyword">open</a> <a id="20033" class="Keyword">import</a> <a id="20040" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="20063" class="Keyword">open</a> <a id="20068" class="Keyword">import</a> <a id="20075" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="20123" class="Keyword">open</a> <a id="20128" class="Keyword">import</a> <a id="20135" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="20165" class="Keyword">open</a> <a id="20170" class="Keyword">import</a> <a id="20177" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="20247" class="Keyword">open</a> <a id="20252" class="Keyword">import</a> <a id="20259" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="20274" class="Keyword">open</a> <a id="20279" class="Keyword">import</a> <a id="20286" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="20319" class="Keyword">open</a> <a id="20324" class="Keyword">import</a> <a id="20331" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="20363" class="Keyword">open</a> <a id="20368" class="Keyword">import</a> <a id="20375" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="20417" class="Keyword">open</a> <a id="20422" class="Keyword">import</a> <a id="20429" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="20467" class="Keyword">open</a> <a id="20472" class="Keyword">import</a> <a id="20479" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="20516" class="Keyword">open</a> <a id="20521" class="Keyword">import</a> <a id="20528" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="20561" class="Keyword">open</a> <a id="20566" class="Keyword">import</a> <a id="20573" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="20597" class="Keyword">open</a> <a id="20602" class="Keyword">import</a> <a id="20609" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="20648" class="Keyword">open</a> <a id="20653" class="Keyword">import</a> <a id="20660" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="20706" class="Keyword">open</a> <a id="20711" class="Keyword">import</a> <a id="20718" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="20763" class="Keyword">open</a> <a id="20768" class="Keyword">import</a> <a id="20775" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="20813" class="Keyword">open</a> <a id="20818" class="Keyword">import</a> <a id="20825" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="20857" class="Keyword">open</a> <a id="20862" class="Keyword">import</a> <a id="20869" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="20922" class="Keyword">open</a> <a id="20927" class="Keyword">import</a> <a id="20934" href="order-theory.html" class="Module">order-theory</a>
<a id="20947" class="Keyword">open</a> <a id="20952" class="Keyword">import</a> <a id="20959" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="20986" class="Keyword">open</a> <a id="20991" class="Keyword">import</a> <a id="20998" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="21028" class="Keyword">open</a> <a id="21033" class="Keyword">import</a> <a id="21040" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="21073" class="Keyword">open</a> <a id="21078" class="Keyword">import</a> <a id="21085" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="21121" class="Keyword">open</a> <a id="21126" class="Keyword">import</a> <a id="21133" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="21160" class="Keyword">open</a> <a id="21165" class="Keyword">import</a> <a id="21172" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="21202" class="Keyword">open</a> <a id="21207" class="Keyword">import</a> <a id="21214" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="21250" class="Keyword">open</a> <a id="21255" class="Keyword">import</a> <a id="21262" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="21304" class="Keyword">open</a> <a id="21309" class="Keyword">import</a> <a id="21316" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="21348" class="Keyword">open</a> <a id="21353" class="Keyword">import</a> <a id="21360" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="21397" class="Keyword">open</a> <a id="21402" class="Keyword">import</a> <a id="21409" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="21449" class="Keyword">open</a> <a id="21454" class="Keyword">import</a> <a id="21461" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="21496" class="Keyword">open</a> <a id="21501" class="Keyword">import</a> <a id="21508" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="21546" class="Keyword">open</a> <a id="21551" class="Keyword">import</a> <a id="21558" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="21593" class="Keyword">open</a> <a id="21598" class="Keyword">import</a> <a id="21605" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="21640" class="Keyword">open</a> <a id="21645" class="Keyword">import</a> <a id="21652" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="21690" class="Keyword">open</a> <a id="21695" class="Keyword">import</a> <a id="21702" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="21733" class="Keyword">open</a> <a id="21738" class="Keyword">import</a> <a id="21745" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="21778" class="Keyword">open</a> <a id="21783" class="Keyword">import</a> <a id="21790" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="21810" class="Keyword">open</a> <a id="21815" class="Keyword">import</a> <a id="21822" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="21845" class="Keyword">open</a> <a id="21850" class="Keyword">import</a> <a id="21857" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="21880" class="Keyword">open</a> <a id="21885" class="Keyword">import</a> <a id="21892" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="21918" class="Keyword">open</a> <a id="21923" class="Keyword">import</a> <a id="21930" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="21956" class="Keyword">open</a> <a id="21961" class="Keyword">import</a> <a id="21968" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="22024" class="Keyword">open</a> <a id="22029" class="Keyword">import</a> <a id="22036" href="polytopes.html" class="Module">polytopes</a>
<a id="22046" class="Keyword">open</a> <a id="22051" class="Keyword">import</a> <a id="22058" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="22116" class="Keyword">open</a> <a id="22121" class="Keyword">import</a> <a id="22128" href="ring-theory.html" class="Module">ring-theory</a>
<a id="22140" class="Keyword">open</a> <a id="22145" class="Keyword">import</a> <a id="22152" href="ring-theory.commutative-rings.html" class="Module">ring-theory.commutative-rings</a>
<a id="22182" class="Keyword">open</a> <a id="22187" class="Keyword">import</a> <a id="22194" href="ring-theory.discrete-fields.html" class="Module">ring-theory.discrete-fields</a>
<a id="22222" class="Keyword">open</a> <a id="22227" class="Keyword">import</a> <a id="22234" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="22261" class="Keyword">open</a> <a id="22266" class="Keyword">import</a> <a id="22273" href="ring-theory.eisenstein-integers.html" class="Module">ring-theory.eisenstein-integers</a>
<a id="22305" class="Keyword">open</a> <a id="22310" class="Keyword">import</a> <a id="22317" href="ring-theory.gaussian-integers.html" class="Module">ring-theory.gaussian-integers</a>
<a id="22347" class="Keyword">open</a> <a id="22352" class="Keyword">import</a> <a id="22359" href="ring-theory.homomorphisms-commutative-rings.html" class="Module">ring-theory.homomorphisms-commutative-rings</a>
<a id="22403" class="Keyword">open</a> <a id="22408" class="Keyword">import</a> <a id="22415" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="22447" class="Keyword">open</a> <a id="22452" class="Keyword">import</a> <a id="22459" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="22505" class="Keyword">open</a> <a id="22510" class="Keyword">import</a> <a id="22517" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="22542" class="Keyword">open</a> <a id="22547" class="Keyword">import</a> <a id="22554" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="22592" class="Keyword">open</a> <a id="22597" class="Keyword">import</a> <a id="22604" href="ring-theory.isomorphisms-commutative-rings.html" class="Module">ring-theory.isomorphisms-commutative-rings</a>
<a id="22647" class="Keyword">open</a> <a id="22652" class="Keyword">import</a> <a id="22659" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="22690" class="Keyword">open</a> <a id="22695" class="Keyword">import</a> <a id="22702" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="22734" class="Keyword">open</a> <a id="22739" class="Keyword">import</a> <a id="22746" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="22775" class="Keyword">open</a> <a id="22780" class="Keyword">import</a> <a id="22787" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="22848" class="Keyword">open</a> <a id="22853" class="Keyword">import</a> <a id="22860" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="22886" class="Keyword">open</a> <a id="22891" class="Keyword">import</a> <a id="22898" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="22937" class="Keyword">open</a> <a id="22942" class="Keyword">import</a> <a id="22949" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="22987" class="Keyword">open</a> <a id="22992" class="Keyword">import</a> <a id="22999" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="23045" class="Keyword">open</a> <a id="23050" class="Keyword">import</a> <a id="23057" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="23094" class="Keyword">open</a> <a id="23099" class="Keyword">import</a> <a id="23106" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="23146" class="Keyword">open</a> <a id="23151" class="Keyword">import</a> <a id="23158" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="23197" class="Keyword">open</a> <a id="23202" class="Keyword">import</a> <a id="23209" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="23242" class="Keyword">open</a> <a id="23247" class="Keyword">import</a> <a id="23254" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="23303" class="Keyword">open</a> <a id="23308" class="Keyword">import</a> <a id="23315" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="23354" class="Keyword">open</a> <a id="23359" class="Keyword">import</a> <a id="23366" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="23411" class="Keyword">open</a> <a id="23416" class="Keyword">import</a> <a id="23423" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="23475" class="Keyword">open</a> <a id="23480" class="Keyword">import</a> <a id="23487" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="23540" class="Keyword">open</a> <a id="23545" class="Keyword">import</a> <a id="23552" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="23600" class="Keyword">open</a> <a id="23605" class="Keyword">import</a> <a id="23612" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="23652" class="Keyword">open</a> <a id="23657" class="Keyword">import</a> <a id="23664" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="23711" class="Keyword">open</a> <a id="23716" class="Keyword">import</a> <a id="23723" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="23761" class="Keyword">open</a> <a id="23766" class="Keyword">import</a> <a id="23773" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="23827" class="Keyword">open</a> <a id="23832" class="Keyword">import</a> <a id="23839" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="23886" class="Keyword">open</a> <a id="23891" class="Keyword">import</a> <a id="23898" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="23950" class="Keyword">open</a> <a id="23955" class="Keyword">import</a> <a id="23962" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="24007" class="Keyword">open</a> <a id="24012" class="Keyword">import</a> <a id="24019" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="24058" class="Keyword">open</a> <a id="24063" class="Keyword">import</a> <a id="24070" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="24110" class="Keyword">open</a> <a id="24115" class="Keyword">import</a> <a id="24122" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="24155" class="Keyword">open</a> <a id="24160" class="Keyword">import</a> <a id="24167" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="24212" class="Keyword">open</a> <a id="24217" class="Keyword">import</a> <a id="24224" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="24300" class="Keyword">open</a> <a id="24305" class="Keyword">import</a> <a id="24312" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="24374" class="Keyword">open</a> <a id="24379" class="Keyword">import</a> <a id="24386" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="24410" class="Keyword">open</a> <a id="24415" class="Keyword">import</a> <a id="24422" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="24475" class="Keyword">open</a> <a id="24480" class="Keyword">import</a> <a id="24487" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="24530" class="Keyword">open</a> <a id="24535" class="Keyword">import</a> <a id="24542" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="24582" class="Keyword">open</a> <a id="24587" class="Keyword">import</a> <a id="24594" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="24633" class="Keyword">open</a> <a id="24638" class="Keyword">import</a> <a id="24645" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="24693" class="Keyword">open</a> <a id="24698" class="Keyword">import</a> <a id="24705" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="24752" class="Keyword">open</a> <a id="24757" class="Keyword">import</a> <a id="24764" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="24816" class="Keyword">open</a> <a id="24821" class="Keyword">import</a> <a id="24828" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="24868" class="Keyword">open</a> <a id="24873" class="Keyword">import</a> <a id="24880" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="24932" class="Keyword">open</a> <a id="24937" class="Keyword">import</a> <a id="24944" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="24998" class="Keyword">open</a> <a id="25003" class="Keyword">import</a> <a id="25010" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="25049" class="Keyword">open</a> <a id="25054" class="Keyword">import</a> <a id="25061" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="25094" class="Keyword">open</a> <a id="25099" class="Keyword">import</a> <a id="25106" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="25136" class="Keyword">open</a> <a id="25141" class="Keyword">import</a> <a id="25148" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="25207" class="Keyword">open</a> <a id="25212" class="Keyword">import</a> <a id="25219" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="25274" class="Keyword">open</a> <a id="25279" class="Keyword">import</a> <a id="25286" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="25329" class="Keyword">open</a> <a id="25334" class="Keyword">import</a> <a id="25341" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="25390" class="Keyword">open</a> <a id="25395" class="Keyword">import</a> <a id="25402" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="25447" class="Keyword">open</a> <a id="25452" class="Keyword">import</a> <a id="25459" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="25510" class="Keyword">open</a> <a id="25515" class="Keyword">import</a> <a id="25522" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="25600" class="Keyword">open</a> <a id="25605" class="Keyword">import</a> <a id="25612" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="25652" class="Keyword">open</a> <a id="25657" class="Keyword">import</a> <a id="25664" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="25721" class="Keyword">open</a> <a id="25726" class="Keyword">import</a> <a id="25733" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="25768" class="Keyword">open</a> <a id="25773" class="Keyword">import</a> <a id="25780" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="25826" class="Keyword">open</a> <a id="25831" class="Keyword">import</a> <a id="25838" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="25893" class="Keyword">open</a> <a id="25898" class="Keyword">import</a> <a id="25905" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="25948" class="Keyword">open</a> <a id="25953" class="Keyword">import</a> <a id="25960" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="26019" class="Keyword">open</a> <a id="26024" class="Keyword">import</a> <a id="26031" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="26068" class="Keyword">open</a> <a id="26073" class="Keyword">import</a> <a id="26080" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="26119" class="Keyword">open</a> <a id="26124" class="Keyword">import</a> <a id="26131" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="26169" class="Keyword">open</a> <a id="26174" class="Keyword">import</a> <a id="26181" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="26233" class="Keyword">open</a> <a id="26238" class="Keyword">import</a> <a id="26245" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="26290" class="Keyword">open</a> <a id="26295" class="Keyword">import</a> <a id="26302" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="26339" class="Keyword">open</a> <a id="26344" class="Keyword">import</a> <a id="26351" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="26400" class="Keyword">open</a> <a id="26405" class="Keyword">import</a> <a id="26412" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="26451" class="Keyword">open</a> <a id="26456" class="Keyword">import</a> <a id="26463" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="26501" class="Keyword">open</a> <a id="26506" class="Keyword">import</a> <a id="26513" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="26568" class="Keyword">open</a> <a id="26573" class="Keyword">import</a> <a id="26580" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="26619" class="Keyword">open</a> <a id="26624" class="Keyword">import</a> <a id="26631" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="26678" class="Keyword">open</a> <a id="26683" class="Keyword">import</a> <a id="26690" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="26720" class="Keyword">open</a> <a id="26725" class="Keyword">import</a> <a id="26732" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="26762" class="Keyword">open</a> <a id="26767" class="Keyword">import</a> <a id="26774" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="26817" class="Keyword">open</a> <a id="26822" class="Keyword">import</a> <a id="26829" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="26864" class="Keyword">open</a> <a id="26869" class="Keyword">import</a> <a id="26876" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="26916" class="Keyword">open</a> <a id="26921" class="Keyword">import</a> <a id="26928" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="26973" class="Keyword">open</a> <a id="26978" class="Keyword">import</a> <a id="26985" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="27035" class="Keyword">open</a> <a id="27040" class="Keyword">import</a> <a id="27047" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="27085" class="Keyword">open</a> <a id="27090" class="Keyword">import</a> <a id="27097" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="27146" class="Keyword">open</a> <a id="27151" class="Keyword">import</a> <a id="27158" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="27221" class="Keyword">open</a> <a id="27226" class="Keyword">import</a> <a id="27233" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="27265" class="Keyword">open</a> <a id="27270" class="Keyword">import</a> <a id="27277" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="27330" class="Keyword">open</a> <a id="27335" class="Keyword">import</a> <a id="27342" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="27388" class="Keyword">open</a> <a id="27393" class="Keyword">import</a> <a id="27400" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="27446" class="Keyword">open</a> <a id="27451" class="Keyword">import</a> <a id="27458" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="27506" class="Keyword">open</a> <a id="27511" class="Keyword">import</a> <a id="27518" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="27588" class="Keyword">open</a> <a id="27593" class="Keyword">import</a> <a id="27600" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="27613" class="Keyword">open</a> <a id="27618" class="Keyword">import</a> <a id="27625" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="27645" class="Keyword">open</a> <a id="27650" class="Keyword">import</a> <a id="27657" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="27687" class="Keyword">open</a> <a id="27692" class="Keyword">import</a> <a id="27699" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="27741" class="Keyword">open</a> <a id="27746" class="Keyword">import</a> <a id="27753" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="27804" class="Keyword">open</a> <a id="27809" class="Keyword">import</a> <a id="27816" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="27841" class="Keyword">open</a> <a id="27846" class="Keyword">import</a> <a id="27853" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="27877" class="Keyword">open</a> <a id="27882" class="Keyword">import</a> <a id="27889" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="27915" class="Keyword">open</a> <a id="27920" class="Keyword">import</a> <a id="27927" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="27957" class="Keyword">open</a> <a id="27962" class="Keyword">import</a> <a id="27969" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="27998" class="Keyword">open</a> <a id="28003" class="Keyword">import</a> <a id="28010" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

