# Univalent mathematics in Agda

Welcome to the website of the `agda-unimath` formalization project.

[![CI](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml/badge.svg)](https://github.com/UniMath/agda-unimath/actions/workflows/ci.yaml) [![pages-build-deployment](https://github.com/UniMath/agda-unimath/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/UniMath/agda-unimath/actions/workflows/pages/pages-build-deployment)

The `agda-unimath` library is a new formalisation project for univalent mathematics in Agda. Our goal is to formalize an extensive curriculum of mathematics from the univalent point of view. Furthermore, we think libraries of formalized mathematics have the potential to be useful, and informative resources for mathematicians. Our library is designed to work towards this goal, and we welcome contributions to the library about any topic in mathematics.

The library is built in Agda 2.6.2. It can be compiled by running `make check` from the main folder of the repository.

## Joining the project

Great, you want to contribute something! The best way to start is to find us in our chat channels on the [agda-unimath discord](https://discord.gg/Zp2e8hYsuX). We have a vibing community there, and you're more than welcome to join us just to hang out.

Once you've decided what you want to contribute, the best way to proceed is to make your own fork of the library. Within your fork, make a separate branch in which you will be making your contributions. Now you're ready to start your project! When you've completed your formalization you can proceed by making a pull request. Then we will review your contributions, and merge it when it is ready for the `agda-unimath` library.

## Statement of inclusion

There are many reasons to contribute something to a library of formalized mathematics. Some do it just for fun, some do it for their research, some do it to learn something. Whatever your reason is, we welcome your contributions! To keep the experience of contributing something to our library enjoyable for everyone, we strive for an inclusive community of contributors. You can expect from us that we are kind and respectful in discussions, that we will be mindful of your pronouns and use [inclusive language](https://www.apa.org/about/apa/equity-diversity-inclusion/language-guidelines), and that we value your input regardless of your level of experience or status in the community. We're commited to providing a safe and welcoming environment to people of any gender identity, sexual orientation, race, colour, age, ability, ethnicity, background, or fluency in English -- here on github, in online communication channels, and in person. Homotopy type theory is difficult enough without all the barriers that many of us have to face, so we hope to bring some of those down a bit.

:rainbow: Happy contributing!

Elisabeth Bonnevier  
Jonathan Prieto-Cubides  
Egbert Rijke

<pre class="Agda"><a id="2967" class="Symbol">{-#</a> <a id="2971" class="Keyword">OPTIONS</a> <a id="2979" class="Pragma">--without-K</a> <a id="2991" class="Pragma">--exact-split</a> <a id="3005" class="Pragma">--guardedness</a> <a id="3019" class="Symbol">#-}</a>
</pre>
## Category theory

<pre class="Agda"><a id="3056" class="Keyword">open</a> <a id="3061" class="Keyword">import</a> <a id="3068" href="category-theory.html" class="Module">category-theory</a>
<a id="3084" class="Keyword">open</a> <a id="3089" class="Keyword">import</a> <a id="3096" href="category-theory.adjunctions-large-precategories.html" class="Module">category-theory.adjunctions-large-precategories</a>
<a id="3144" class="Keyword">open</a> <a id="3149" class="Keyword">import</a> <a id="3156" href="category-theory.anafunctors.html" class="Module">category-theory.anafunctors</a>
<a id="3184" class="Keyword">open</a> <a id="3189" class="Keyword">import</a> <a id="3196" href="category-theory.categories.html" class="Module">category-theory.categories</a>
<a id="3223" class="Keyword">open</a> <a id="3228" class="Keyword">import</a> <a id="3235" href="category-theory.equivalences-categories.html" class="Module">category-theory.equivalences-categories</a>
<a id="3275" class="Keyword">open</a> <a id="3280" class="Keyword">import</a> <a id="3287" href="category-theory.equivalences-large-precategories.html" class="Module">category-theory.equivalences-large-precategories</a>
<a id="3336" class="Keyword">open</a> <a id="3341" class="Keyword">import</a> <a id="3348" href="category-theory.equivalences-precategories.html" class="Module">category-theory.equivalences-precategories</a>
<a id="3391" class="Keyword">open</a> <a id="3396" class="Keyword">import</a> <a id="3403" href="category-theory.functors-categories.html" class="Module">category-theory.functors-categories</a>
<a id="3439" class="Keyword">open</a> <a id="3444" class="Keyword">import</a> <a id="3451" href="category-theory.functors-large-precategories.html" class="Module">category-theory.functors-large-precategories</a>
<a id="3496" class="Keyword">open</a> <a id="3501" class="Keyword">import</a> <a id="3508" href="category-theory.functors-precategories.html" class="Module">category-theory.functors-precategories</a>
<a id="3547" class="Keyword">open</a> <a id="3552" class="Keyword">import</a> <a id="3559" href="category-theory.homotopies-natural-transformations-large-precategories.html" class="Module">category-theory.homotopies-natural-transformations-large-precategories</a>
<a id="3630" class="Keyword">open</a> <a id="3635" class="Keyword">import</a> <a id="3642" href="category-theory.initial-objects-precategories.html" class="Module">category-theory.initial-objects-precategories</a>
<a id="3688" class="Keyword">open</a> <a id="3693" class="Keyword">import</a> <a id="3700" href="category-theory.isomorphisms-categories.html" class="Module">category-theory.isomorphisms-categories</a>
<a id="3740" class="Keyword">open</a> <a id="3745" class="Keyword">import</a> <a id="3752" href="category-theory.isomorphisms-large-precategories.html" class="Module">category-theory.isomorphisms-large-precategories</a>
<a id="3801" class="Keyword">open</a> <a id="3806" class="Keyword">import</a> <a id="3813" href="category-theory.isomorphisms-precategories.html" class="Module">category-theory.isomorphisms-precategories</a>
<a id="3856" class="Keyword">open</a> <a id="3861" class="Keyword">import</a> <a id="3868" href="category-theory.large-categories.html" class="Module">category-theory.large-categories</a>
<a id="3901" class="Keyword">open</a> <a id="3906" class="Keyword">import</a> <a id="3913" href="category-theory.large-precategories.html" class="Module">category-theory.large-precategories</a>
<a id="3949" class="Keyword">open</a> <a id="3954" class="Keyword">import</a> <a id="3961" href="category-theory.monomorphisms-large-precategories.html" class="Module">category-theory.monomorphisms-large-precategories</a>
<a id="4011" class="Keyword">open</a> <a id="4016" class="Keyword">import</a> <a id="4023" href="category-theory.natural-isomorphisms-categories.html" class="Module">category-theory.natural-isomorphisms-categories</a>
<a id="4071" class="Keyword">open</a> <a id="4076" class="Keyword">import</a> <a id="4083" href="category-theory.natural-isomorphisms-large-precategories.html" class="Module">category-theory.natural-isomorphisms-large-precategories</a>
<a id="4140" class="Keyword">open</a> <a id="4145" class="Keyword">import</a> <a id="4152" href="category-theory.natural-isomorphisms-precategories.html" class="Module">category-theory.natural-isomorphisms-precategories</a>
<a id="4203" class="Keyword">open</a> <a id="4208" class="Keyword">import</a> <a id="4215" href="category-theory.natural-transformations-categories.html" class="Module">category-theory.natural-transformations-categories</a>
<a id="4266" class="Keyword">open</a> <a id="4271" class="Keyword">import</a> <a id="4278" href="category-theory.natural-transformations-large-precategories.html" class="Module">category-theory.natural-transformations-large-precategories</a>
<a id="4338" class="Keyword">open</a> <a id="4343" class="Keyword">import</a> <a id="4350" href="category-theory.natural-transformations-precategories.html" class="Module">category-theory.natural-transformations-precategories</a>
<a id="4404" class="Keyword">open</a> <a id="4409" class="Keyword">import</a> <a id="4416" href="category-theory.precategories.html" class="Module">category-theory.precategories</a>
<a id="4446" class="Keyword">open</a> <a id="4451" class="Keyword">import</a> <a id="4458" href="category-theory.slice-precategories.html" class="Module">category-theory.slice-precategories</a>
<a id="4494" class="Keyword">open</a> <a id="4499" class="Keyword">import</a> <a id="4506" href="category-theory.terminal-objects-precategories.html" class="Module">category-theory.terminal-objects-precategories</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="4595" class="Keyword">open</a> <a id="4600" class="Keyword">import</a> <a id="4607" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="4632" class="Keyword">open</a> <a id="4637" class="Keyword">import</a> <a id="4644" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="4693" class="Keyword">open</a> <a id="4698" class="Keyword">import</a> <a id="4705" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="4748" class="Keyword">open</a> <a id="4753" class="Keyword">import</a> <a id="4760" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="4810" class="Keyword">open</a> <a id="4815" class="Keyword">import</a> <a id="4822" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="4868" class="Keyword">open</a> <a id="4873" class="Keyword">import</a> <a id="4880" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="4927" class="Keyword">open</a> <a id="4932" class="Keyword">import</a> <a id="4939" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="4998" class="Keyword">open</a> <a id="5003" class="Keyword">import</a> <a id="5010" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="5051" class="Keyword">open</a> <a id="5056" class="Keyword">import</a> <a id="5063" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="5106" class="Keyword">open</a> <a id="5111" class="Keyword">import</a> <a id="5118" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="5162" class="Keyword">open</a> <a id="5167" class="Keyword">import</a> <a id="5174" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="5219" class="Keyword">open</a> <a id="5224" class="Keyword">import</a> <a id="5231" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="5283" class="Keyword">open</a> <a id="5288" class="Keyword">import</a> <a id="5295" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="5355" class="Keyword">open</a> <a id="5360" class="Keyword">import</a> <a id="5367" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="5408" class="Keyword">open</a> <a id="5413" class="Keyword">import</a> <a id="5420" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="5465" class="Keyword">open</a> <a id="5470" class="Keyword">import</a> <a id="5477" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="5524" class="Keyword">open</a> <a id="5529" class="Keyword">import</a> <a id="5536" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="5579" class="Keyword">open</a> <a id="5584" class="Keyword">import</a> <a id="5591" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="5641" class="Keyword">open</a> <a id="5646" class="Keyword">import</a> <a id="5653" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="5700" class="Keyword">open</a> <a id="5705" class="Keyword">import</a> <a id="5712" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="5769" class="Keyword">open</a> <a id="5774" class="Keyword">import</a> <a id="5781" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="5835" class="Keyword">open</a> <a id="5840" class="Keyword">import</a> <a id="5847" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="5907" class="Keyword">open</a> <a id="5912" class="Keyword">import</a> <a id="5919" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="5962" class="Keyword">open</a> <a id="5967" class="Keyword">import</a> <a id="5974" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="6024" class="Keyword">open</a> <a id="6029" class="Keyword">import</a> <a id="6036" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="6096" class="Keyword">open</a> <a id="6101" class="Keyword">import</a> <a id="6108" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="6157" class="Keyword">open</a> <a id="6162" class="Keyword">import</a> <a id="6169" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="6225" class="Keyword">open</a> <a id="6230" class="Keyword">import</a> <a id="6237" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="6273" class="Keyword">open</a> <a id="6278" class="Keyword">import</a> <a id="6285" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="6329" class="Keyword">open</a> <a id="6334" class="Keyword">import</a> <a id="6341" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="6385" class="Keyword">open</a> <a id="6390" class="Keyword">import</a> <a id="6397" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="6447" class="Keyword">open</a> <a id="6452" class="Keyword">import</a> <a id="6459" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="6505" class="Keyword">open</a> <a id="6510" class="Keyword">import</a> <a id="6517" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="6552" class="Keyword">open</a> <a id="6557" class="Keyword">import</a> <a id="6564" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="6609" class="Keyword">open</a> <a id="6614" class="Keyword">import</a> <a id="6621" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="6679" class="Keyword">open</a> <a id="6684" class="Keyword">import</a> <a id="6691" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="6756" class="Keyword">open</a> <a id="6761" class="Keyword">import</a> <a id="6768" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="6811" class="Keyword">open</a> <a id="6816" class="Keyword">import</a> <a id="6823" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="6877" class="Keyword">open</a> <a id="6882" class="Keyword">import</a> <a id="6889" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="6934" class="Keyword">open</a> <a id="6939" class="Keyword">import</a> <a id="6946" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="6998" class="Keyword">open</a> <a id="7003" class="Keyword">import</a> <a id="7010" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="7068" class="Keyword">open</a> <a id="7073" class="Keyword">import</a> <a id="7080" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="7126" class="Keyword">open</a> <a id="7131" class="Keyword">import</a> <a id="7138" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="7172" class="Keyword">open</a> <a id="7177" class="Keyword">import</a> <a id="7184" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="7229" class="Keyword">open</a> <a id="7234" class="Keyword">import</a> <a id="7241" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="7295" class="Keyword">open</a> <a id="7300" class="Keyword">import</a> <a id="7307" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="7356" class="Keyword">open</a> <a id="7361" class="Keyword">import</a> <a id="7368" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="7409" class="Keyword">open</a> <a id="7414" class="Keyword">import</a> <a id="7421" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="7470" class="Keyword">open</a> <a id="7475" class="Keyword">import</a> <a id="7482" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="7548" class="Keyword">open</a> <a id="7553" class="Keyword">import</a> <a id="7560" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="7604" class="Keyword">open</a> <a id="7609" class="Keyword">import</a> <a id="7616" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="7665" class="Keyword">open</a> <a id="7670" class="Keyword">import</a> <a id="7677" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="7733" class="Keyword">open</a> <a id="7738" class="Keyword">import</a> <a id="7745" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="7786" class="Keyword">open</a> <a id="7791" class="Keyword">import</a> <a id="7798" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="7847" class="Keyword">open</a> <a id="7852" class="Keyword">import</a> <a id="7859" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="7918" class="Keyword">open</a> <a id="7923" class="Keyword">import</a> <a id="7930" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="7969" class="Keyword">open</a> <a id="7974" class="Keyword">import</a> <a id="7981" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="8034" class="Keyword">open</a> <a id="8039" class="Keyword">import</a> <a id="8046" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="8103" class="Keyword">open</a> <a id="8108" class="Keyword">import</a> <a id="8115" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="8157" class="Keyword">open</a> <a id="8162" class="Keyword">import</a> <a id="8169" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="8220" class="Keyword">open</a> <a id="8225" class="Keyword">import</a> <a id="8232" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="8290" class="Keyword">open</a> <a id="8295" class="Keyword">import</a> <a id="8302" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="8366" class="Keyword">open</a> <a id="8371" class="Keyword">import</a> <a id="8378" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="8431" class="Keyword">open</a> <a id="8436" class="Keyword">import</a> <a id="8443" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="8496" class="Keyword">open</a> <a id="8501" class="Keyword">import</a> <a id="8508" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="8569" class="Keyword">open</a> <a id="8574" class="Keyword">import</a> <a id="8581" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="8639" class="Keyword">open</a> <a id="8644" class="Keyword">import</a> <a id="8651" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="8700" class="Keyword">open</a> <a id="8705" class="Keyword">import</a> <a id="8712" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="8756" class="Keyword">open</a> <a id="8761" class="Keyword">import</a> <a id="8768" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="8811" class="Keyword">open</a> <a id="8816" class="Keyword">import</a> <a id="8823" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="8870" class="Keyword">open</a> <a id="8875" class="Keyword">import</a> <a id="8882" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="8943" class="Keyword">open</a> <a id="8948" class="Keyword">import</a> <a id="8955" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="9018" class="Keyword">open</a> <a id="9023" class="Keyword">import</a> <a id="9030" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="9090" class="Keyword">open</a> <a id="9095" class="Keyword">import</a> <a id="9102" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="9156" class="Keyword">open</a> <a id="9161" class="Keyword">import</a> <a id="9168" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="9233" class="Keyword">open</a> <a id="9238" class="Keyword">import</a> <a id="9245" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="9353" class="Keyword">open</a> <a id="9358" class="Keyword">import</a> <a id="9365" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="9385" class="Keyword">open</a> <a id="9390" class="Keyword">import</a> <a id="9397" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="9443" class="Keyword">open</a> <a id="9448" class="Keyword">import</a> <a id="9455" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="9501" class="Keyword">open</a> <a id="9506" class="Keyword">import</a> <a id="9513" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="9547" class="Keyword">open</a> <a id="9552" class="Keyword">import</a> <a id="9559" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="9594" class="Keyword">open</a> <a id="9599" class="Keyword">import</a> <a id="9606" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="9644" class="Keyword">open</a> <a id="9649" class="Keyword">import</a> <a id="9656" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="9694" class="Keyword">open</a> <a id="9699" class="Keyword">import</a> <a id="9706" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="9746" class="Keyword">open</a> <a id="9751" class="Keyword">import</a> <a id="9758" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="9791" class="Keyword">open</a> <a id="9796" class="Keyword">import</a> <a id="9803" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="9841" class="Keyword">open</a> <a id="9846" class="Keyword">import</a> <a id="9853" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="9916" class="Keyword">open</a> <a id="9921" class="Keyword">import</a> <a id="9928" href="foundation.html" class="Module">foundation</a>
<a id="9939" class="Keyword">open</a> <a id="9944" class="Keyword">import</a> <a id="9951" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="9969" class="Keyword">open</a> <a id="9974" class="Keyword">import</a> <a id="9981" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="10000" class="Keyword">open</a> <a id="10005" class="Keyword">import</a> <a id="10012" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="10031" class="Keyword">open</a> <a id="10036" class="Keyword">import</a> <a id="10043" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="10087" class="Keyword">open</a> <a id="10092" class="Keyword">import</a> <a id="10099" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="10124" class="Keyword">open</a> <a id="10129" class="Keyword">import</a> <a id="10136" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="10163" class="Keyword">open</a> <a id="10168" class="Keyword">import</a> <a id="10175" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="10204" class="Keyword">open</a> <a id="10209" class="Keyword">import</a> <a id="10216" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="10247" class="Keyword">open</a> <a id="10252" class="Keyword">import</a> <a id="10259" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="10287" class="Keyword">open</a> <a id="10292" class="Keyword">import</a> <a id="10299" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="10329" class="Keyword">open</a> <a id="10334" class="Keyword">import</a> <a id="10341" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="10361" class="Keyword">open</a> <a id="10366" class="Keyword">import</a> <a id="10373" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="10410" class="Keyword">open</a> <a id="10415" class="Keyword">import</a> <a id="10422" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="10457" class="Keyword">open</a> <a id="10462" class="Keyword">import</a> <a id="10469" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="10527" class="Keyword">open</a> <a id="10532" class="Keyword">import</a> <a id="10539" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="10577" class="Keyword">open</a> <a id="10582" class="Keyword">import</a> <a id="10589" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="10618" class="Keyword">open</a> <a id="10623" class="Keyword">import</a> <a id="10630" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="10653" class="Keyword">open</a> <a id="10658" class="Keyword">import</a> <a id="10665" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="10688" class="Keyword">open</a> <a id="10693" class="Keyword">import</a> <a id="10700" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="10742" class="Keyword">open</a> <a id="10747" class="Keyword">import</a> <a id="10754" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="10786" class="Keyword">open</a> <a id="10791" class="Keyword">import</a> <a id="10798" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="10825" class="Keyword">open</a> <a id="10830" class="Keyword">import</a> <a id="10837" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="10862" class="Keyword">open</a> <a id="10867" class="Keyword">import</a> <a id="10874" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="10903" class="Keyword">open</a> <a id="10908" class="Keyword">import</a> <a id="10915" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="10945" class="Keyword">open</a> <a id="10950" class="Keyword">import</a> <a id="10957" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="10984" class="Keyword">open</a> <a id="10989" class="Keyword">import</a> <a id="10996" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="11015" class="Keyword">open</a> <a id="11020" class="Keyword">import</a> <a id="11027" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="11073" class="Keyword">open</a> <a id="11078" class="Keyword">import</a> <a id="11085" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="11127" class="Keyword">open</a> <a id="11132" class="Keyword">import</a> <a id="11139" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="11171" class="Keyword">open</a> <a id="11176" class="Keyword">import</a> <a id="11183" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="11213" class="Keyword">open</a> <a id="11218" class="Keyword">import</a> <a id="11225" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="11251" class="Keyword">open</a> <a id="11256" class="Keyword">import</a> <a id="11263" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="11297" class="Keyword">open</a> <a id="11302" class="Keyword">import</a> <a id="11309" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="11339" class="Keyword">open</a> <a id="11344" class="Keyword">import</a> <a id="11351" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="11378" class="Keyword">open</a> <a id="11383" class="Keyword">import</a> <a id="11390" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="11422" class="Keyword">open</a> <a id="11427" class="Keyword">import</a> <a id="11434" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="11468" class="Keyword">open</a> <a id="11473" class="Keyword">import</a> <a id="11480" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="11503" class="Keyword">open</a> <a id="11508" class="Keyword">import</a> <a id="11515" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="11585" class="Keyword">open</a> <a id="11590" class="Keyword">import</a> <a id="11597" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="11667" class="Keyword">open</a> <a id="11672" class="Keyword">import</a> <a id="11679" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="11706" class="Keyword">open</a> <a id="11711" class="Keyword">import</a> <a id="11718" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="11755" class="Keyword">open</a> <a id="11760" class="Keyword">import</a> <a id="11767" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="11815" class="Keyword">open</a> <a id="11820" class="Keyword">import</a> <a id="11827" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="11867" class="Keyword">open</a> <a id="11872" class="Keyword">import</a> <a id="11879" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="11901" class="Keyword">open</a> <a id="11906" class="Keyword">import</a> <a id="11913" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="11936" class="Keyword">open</a> <a id="11941" class="Keyword">import</a> <a id="11948" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="11993" class="Keyword">open</a> <a id="11998" class="Keyword">import</a> <a id="12005" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="12049" class="Keyword">open</a> <a id="12054" class="Keyword">import</a> <a id="12061" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="12097" class="Keyword">open</a> <a id="12102" class="Keyword">import</a> <a id="12109" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="12154" class="Keyword">open</a> <a id="12159" class="Keyword">import</a> <a id="12166" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="12207" class="Keyword">open</a> <a id="12212" class="Keyword">import</a> <a id="12219" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="12254" class="Keyword">open</a> <a id="12259" class="Keyword">import</a> <a id="12266" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="12297" class="Keyword">open</a> <a id="12302" class="Keyword">import</a> <a id="12309" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="12342" class="Keyword">open</a> <a id="12347" class="Keyword">import</a> <a id="12354" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="12387" class="Keyword">open</a> <a id="12392" class="Keyword">import</a> <a id="12399" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="12429" class="Keyword">open</a> <a id="12434" class="Keyword">import</a> <a id="12441" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="12465" class="Keyword">open</a> <a id="12470" class="Keyword">import</a> <a id="12477" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="12515" class="Keyword">open</a> <a id="12520" class="Keyword">import</a> <a id="12527" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="12558" class="Keyword">open</a> <a id="12563" class="Keyword">import</a> <a id="12570" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="12595" class="Keyword">open</a> <a id="12600" class="Keyword">import</a> <a id="12607" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="12635" class="Keyword">open</a> <a id="12640" class="Keyword">import</a> <a id="12647" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="12671" class="Keyword">open</a> <a id="12676" class="Keyword">import</a> <a id="12683" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="12709" class="Keyword">open</a> <a id="12714" class="Keyword">import</a> <a id="12721" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="12756" class="Keyword">open</a> <a id="12761" class="Keyword">import</a> <a id="12768" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="12789" class="Keyword">open</a> <a id="12794" class="Keyword">import</a> <a id="12801" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="12850" class="Keyword">open</a> <a id="12855" class="Keyword">import</a> <a id="12862" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="12903" class="Keyword">open</a> <a id="12908" class="Keyword">import</a> <a id="12915" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="12965" class="Keyword">open</a> <a id="12970" class="Keyword">import</a> <a id="12977" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="13023" class="Keyword">open</a> <a id="13028" class="Keyword">import</a> <a id="13035" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="13075" class="Keyword">open</a> <a id="13080" class="Keyword">import</a> <a id="13087" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="13137" class="Keyword">open</a> <a id="13142" class="Keyword">import</a> <a id="13149" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="13188" class="Keyword">open</a> <a id="13193" class="Keyword">import</a> <a id="13200" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="13240" class="Keyword">open</a> <a id="13245" class="Keyword">import</a> <a id="13252" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="13285" class="Keyword">open</a> <a id="13290" class="Keyword">import</a> <a id="13297" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="13346" class="Keyword">open</a> <a id="13351" class="Keyword">import</a> <a id="13358" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="13383" class="Keyword">open</a> <a id="13388" class="Keyword">import</a> <a id="13395" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="13433" class="Keyword">open</a> <a id="13438" class="Keyword">import</a> <a id="13445" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="13467" class="Keyword">open</a> <a id="13472" class="Keyword">import</a> <a id="13479" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="13507" class="Keyword">open</a> <a id="13512" class="Keyword">import</a> <a id="13519" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="13545" class="Keyword">open</a> <a id="13550" class="Keyword">import</a> <a id="13557" href="foundation.images.html" class="Module">foundation.images</a>
<a id="13575" class="Keyword">open</a> <a id="13580" class="Keyword">import</a> <a id="13587" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="13622" class="Keyword">open</a> <a id="13627" class="Keyword">import</a> <a id="13634" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="13661" class="Keyword">open</a> <a id="13666" class="Keyword">import</a> <a id="13673" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="13729" class="Keyword">open</a> <a id="13734" class="Keyword">import</a> <a id="13741" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="13770" class="Keyword">open</a> <a id="13775" class="Keyword">import</a> <a id="13782" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="13812" class="Keyword">open</a> <a id="13817" class="Keyword">import</a> <a id="13824" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="13850" class="Keyword">open</a> <a id="13855" class="Keyword">import</a> <a id="13862" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="13889" class="Keyword">open</a> <a id="13894" class="Keyword">import</a> <a id="13901" href="foundation.intersection.html" class="Module">foundation.intersection</a>
<a id="13925" class="Keyword">open</a> <a id="13930" class="Keyword">import</a> <a id="13937" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="13960" class="Keyword">open</a> <a id="13965" class="Keyword">import</a> <a id="13972" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="13999" class="Keyword">open</a> <a id="14004" class="Keyword">import</a> <a id="14011" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="14043" class="Keyword">open</a> <a id="14048" class="Keyword">import</a> <a id="14055" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="14089" class="Keyword">open</a> <a id="14094" class="Keyword">import</a> <a id="14101" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="14141" class="Keyword">open</a> <a id="14146" class="Keyword">import</a> <a id="14153" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="14184" class="Keyword">open</a> <a id="14189" class="Keyword">import</a> <a id="14196" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="14228" class="Keyword">open</a> <a id="14233" class="Keyword">import</a> <a id="14240" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="14271" class="Keyword">open</a> <a id="14276" class="Keyword">import</a> <a id="14283" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="14300" class="Keyword">open</a> <a id="14305" class="Keyword">import</a> <a id="14312" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="14337" class="Keyword">open</a> <a id="14342" class="Keyword">import</a> <a id="14349" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="14378" class="Keyword">open</a> <a id="14383" class="Keyword">import</a> <a id="14390" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="14415" class="Keyword">open</a> <a id="14420" class="Keyword">import</a> <a id="14427" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="14448" class="Keyword">open</a> <a id="14453" class="Keyword">import</a> <a id="14460" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="14480" class="Keyword">open</a> <a id="14485" class="Keyword">import</a> <a id="14492" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="14526" class="Keyword">open</a> <a id="14531" class="Keyword">import</a> <a id="14538" href="foundation.pairs-of-distinct-elements.html" class="Module">foundation.pairs-of-distinct-elements</a>
<a id="14576" class="Keyword">open</a> <a id="14581" class="Keyword">import</a> <a id="14588" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="14612" class="Keyword">open</a> <a id="14617" class="Keyword">import</a> <a id="14624" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="14651" class="Keyword">open</a> <a id="14656" class="Keyword">import</a> <a id="14663" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="14698" class="Keyword">open</a> <a id="14703" class="Keyword">import</a> <a id="14710" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="14746" class="Keyword">open</a> <a id="14751" class="Keyword">import</a> <a id="14758" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="14798" class="Keyword">open</a> <a id="14803" class="Keyword">import</a> <a id="14810" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="14840" class="Keyword">open</a> <a id="14845" class="Keyword">import</a> <a id="14852" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="14889" class="Keyword">open</a> <a id="14894" class="Keyword">import</a> <a id="14901" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="14925" class="Keyword">open</a> <a id="14930" class="Keyword">import</a> <a id="14937" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="14958" class="Keyword">open</a> <a id="14963" class="Keyword">import</a> <a id="14970" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="15005" class="Keyword">open</a> <a id="15010" class="Keyword">import</a> <a id="15017" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="15054" class="Keyword">open</a> <a id="15059" class="Keyword">import</a> <a id="15066" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="15115" class="Keyword">open</a> <a id="15120" class="Keyword">import</a> <a id="15127" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="15150" class="Keyword">open</a> <a id="15155" class="Keyword">import</a> <a id="15162" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="15185" class="Keyword">open</a> <a id="15190" class="Keyword">import</a> <a id="15197" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="15225" class="Keyword">open</a> <a id="15230" class="Keyword">import</a> <a id="15237" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="15257" class="Keyword">open</a> <a id="15262" class="Keyword">import</a> <a id="15269" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="15300" class="Keyword">open</a> <a id="15305" class="Keyword">import</a> <a id="15312" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="15339" class="Keyword">open</a> <a id="15344" class="Keyword">import</a> <a id="15351" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="15367" class="Keyword">open</a> <a id="15372" class="Keyword">import</a> <a id="15379" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="15410" class="Keyword">open</a> <a id="15415" class="Keyword">import</a> <a id="15422" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="15439" class="Keyword">open</a> <a id="15444" class="Keyword">import</a> <a id="15451" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="15473" class="Keyword">open</a> <a id="15478" class="Keyword">import</a> <a id="15485" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="15512" class="Keyword">open</a> <a id="15517" class="Keyword">import</a> <a id="15524" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="15547" class="Keyword">open</a> <a id="15552" class="Keyword">import</a> <a id="15559" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="15586" class="Keyword">open</a> <a id="15591" class="Keyword">import</a> <a id="15598" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="15631" class="Keyword">open</a> <a id="15636" class="Keyword">import</a> <a id="15643" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="15683" class="Keyword">open</a> <a id="15688" class="Keyword">import</a> <a id="15695" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="15716" class="Keyword">open</a> <a id="15721" class="Keyword">import</a> <a id="15728" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="15757" class="Keyword">open</a> <a id="15762" class="Keyword">import</a> <a id="15769" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="15807" class="Keyword">open</a> <a id="15812" class="Keyword">import</a> <a id="15819" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="15839" class="Keyword">open</a> <a id="15844" class="Keyword">import</a> <a id="15851" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="15875" class="Keyword">open</a> <a id="15880" class="Keyword">import</a> <a id="15887" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="15914" class="Keyword">open</a> <a id="15919" class="Keyword">import</a> <a id="15926" href="foundation.symmetric-difference.html" class="Module">foundation.symmetric-difference</a>
<a id="15958" class="Keyword">open</a> <a id="15963" class="Keyword">import</a> <a id="15970" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="16000" class="Keyword">open</a> <a id="16005" class="Keyword">import</a> <a id="16012" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="16038" class="Keyword">open</a> <a id="16043" class="Keyword">import</a> <a id="16050" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="16077" class="Keyword">open</a> <a id="16082" class="Keyword">import</a> <a id="16089" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="16118" class="Keyword">open</a> <a id="16123" class="Keyword">import</a> <a id="16130" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="16153" class="Keyword">open</a> <a id="16158" class="Keyword">import</a> <a id="16165" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="16216" class="Keyword">open</a> <a id="16221" class="Keyword">import</a> <a id="16228" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="16271" class="Keyword">open</a> <a id="16276" class="Keyword">import</a> <a id="16283" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="16331" class="Keyword">open</a> <a id="16336" class="Keyword">import</a> <a id="16343" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="16381" class="Keyword">open</a> <a id="16386" class="Keyword">import</a> <a id="16393" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="16430" class="Keyword">open</a> <a id="16435" class="Keyword">import</a> <a id="16442" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="16470" class="Keyword">open</a> <a id="16475" class="Keyword">import</a> <a id="16482" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="16518" class="Keyword">open</a> <a id="16523" class="Keyword">import</a> <a id="16530" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="16568" class="Keyword">open</a> <a id="16573" class="Keyword">import</a> <a id="16580" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="16613" class="Keyword">open</a> <a id="16618" class="Keyword">import</a> <a id="16625" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="16646" class="Keyword">open</a> <a id="16651" class="Keyword">import</a> <a id="16658" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="16712" class="Keyword">open</a> <a id="16717" class="Keyword">import</a> <a id="16724" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="16746" class="Keyword">open</a> <a id="16751" class="Keyword">import</a> <a id="16758" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="16793" class="Keyword">open</a> <a id="16798" class="Keyword">import</a> <a id="16805" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="16835" class="Keyword">open</a> <a id="16840" class="Keyword">import</a> <a id="16847" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="16886" class="Keyword">open</a> <a id="16891" class="Keyword">import</a> <a id="16898" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="16952" class="Keyword">open</a> <a id="16957" class="Keyword">import</a> <a id="16964" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="17010" class="Keyword">open</a> <a id="17015" class="Keyword">import</a> <a id="17022" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="17073" class="Keyword">open</a> <a id="17078" class="Keyword">import</a> <a id="17085" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="17126" class="Keyword">open</a> <a id="17131" class="Keyword">import</a> <a id="17138" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="17183" class="Keyword">open</a> <a id="17188" class="Keyword">import</a> <a id="17195" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="17240" class="Keyword">open</a> <a id="17245" class="Keyword">import</a> <a id="17252" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="17288" class="Keyword">open</a> <a id="17293" class="Keyword">import</a> <a id="17300" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="17336" class="Keyword">open</a> <a id="17341" class="Keyword">import</a> <a id="17348" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="17413" class="Keyword">open</a> <a id="17418" class="Keyword">import</a> <a id="17425" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="17480" class="Keyword">open</a> <a id="17485" class="Keyword">import</a> <a id="17492" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="17532" class="Keyword">open</a> <a id="17537" class="Keyword">import</a> <a id="17544" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="17588" class="Keyword">open</a> <a id="17593" class="Keyword">import</a> <a id="17600" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="17645" class="Keyword">open</a> <a id="17650" class="Keyword">import</a> <a id="17657" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="17698" class="Keyword">open</a> <a id="17703" class="Keyword">import</a> <a id="17710" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="17750" class="Keyword">open</a> <a id="17755" class="Keyword">import</a> <a id="17762" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="17789" class="Keyword">open</a> <a id="17794" class="Keyword">import</a> <a id="17801" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="17828" class="Keyword">open</a> <a id="17833" class="Keyword">import</a> <a id="17840" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="17859" class="Keyword">open</a> <a id="17864" class="Keyword">import</a> <a id="17871" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="17911" class="Keyword">open</a> <a id="17916" class="Keyword">import</a> <a id="17923" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
<a id="17955" class="Keyword">open</a> <a id="17960" class="Keyword">import</a> <a id="17967" href="foundation.xor.html" class="Module">foundation.xor</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="18015" class="Keyword">open</a> <a id="18020" class="Keyword">import</a> <a id="18027" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="18050" class="Keyword">open</a> <a id="18055" class="Keyword">import</a> <a id="18062" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="18086" class="Keyword">open</a> <a id="18091" class="Keyword">import</a> <a id="18098" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="18138" class="Keyword">open</a> <a id="18143" class="Keyword">import</a> <a id="18150" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="18193" class="Keyword">open</a> <a id="18198" class="Keyword">import</a> <a id="18205" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="18239" class="Keyword">open</a> <a id="18244" class="Keyword">import</a> <a id="18251" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="18281" class="Keyword">open</a> <a id="18286" class="Keyword">import</a> <a id="18293" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="18327" class="Keyword">open</a> <a id="18332" class="Keyword">import</a> <a id="18339" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="18374" class="Keyword">open</a> <a id="18379" class="Keyword">import</a> <a id="18386" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="18423" class="Keyword">open</a> <a id="18428" class="Keyword">import</a> <a id="18435" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="18462" class="Keyword">open</a> <a id="18467" class="Keyword">import</a> <a id="18474" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="18502" class="Keyword">open</a> <a id="18507" class="Keyword">import</a> <a id="18514" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="18563" class="Keyword">open</a> <a id="18568" class="Keyword">import</a> <a id="18575" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="18621" class="Keyword">open</a> <a id="18626" class="Keyword">import</a> <a id="18633" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="18673" class="Keyword">open</a> <a id="18678" class="Keyword">import</a> <a id="18685" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="18723" class="Keyword">open</a> <a id="18728" class="Keyword">import</a> <a id="18735" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="18764" class="Keyword">open</a> <a id="18769" class="Keyword">import</a> <a id="18776" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="18806" class="Keyword">open</a> <a id="18811" class="Keyword">import</a> <a id="18818" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="18849" class="Keyword">open</a> <a id="18854" class="Keyword">import</a> <a id="18861" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="18887" class="Keyword">open</a> <a id="18892" class="Keyword">import</a> <a id="18899" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="18950" class="Keyword">open</a> <a id="18955" class="Keyword">import</a> <a id="18962" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="19016" class="Keyword">open</a> <a id="19021" class="Keyword">import</a> <a id="19028" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="19055" class="Keyword">open</a> <a id="19060" class="Keyword">import</a> <a id="19067" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="19100" class="Keyword">open</a> <a id="19105" class="Keyword">import</a> <a id="19112" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="19143" class="Keyword">open</a> <a id="19148" class="Keyword">import</a> <a id="19155" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="19192" class="Keyword">open</a> <a id="19197" class="Keyword">import</a> <a id="19204" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="19229" class="Keyword">open</a> <a id="19234" class="Keyword">import</a> <a id="19241" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="19273" class="Keyword">open</a> <a id="19278" class="Keyword">import</a> <a id="19285" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="19320" class="Keyword">open</a> <a id="19325" class="Keyword">import</a> <a id="19332" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="19361" class="Keyword">open</a> <a id="19366" class="Keyword">import</a> <a id="19373" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="19401" class="Keyword">open</a> <a id="19406" class="Keyword">import</a> <a id="19413" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="19438" class="Keyword">open</a> <a id="19443" class="Keyword">import</a> <a id="19450" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="19471" class="Keyword">open</a> <a id="19476" class="Keyword">import</a> <a id="19483" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="19519" class="Keyword">open</a> <a id="19524" class="Keyword">import</a> <a id="19531" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="19574" class="Keyword">open</a> <a id="19579" class="Keyword">import</a> <a id="19586" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="19611" class="Keyword">open</a> <a id="19616" class="Keyword">import</a> <a id="19623" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="19654" class="Keyword">open</a> <a id="19659" class="Keyword">import</a> <a id="19666" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="19698" class="Keyword">open</a> <a id="19703" class="Keyword">import</a> <a id="19710" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="19744" class="Keyword">open</a> <a id="19749" class="Keyword">import</a> <a id="19756" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="19812" class="Keyword">open</a> <a id="19817" class="Keyword">import</a> <a id="19824" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="19877" class="Keyword">open</a> <a id="19882" class="Keyword">import</a> <a id="19889" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="19916" class="Keyword">open</a> <a id="19921" class="Keyword">import</a> <a id="19928" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="19990" class="Keyword">open</a> <a id="19995" class="Keyword">import</a> <a id="20002" href="graph-theory.html" class="Module">graph-theory</a>
<a id="20015" class="Keyword">open</a> <a id="20020" class="Keyword">import</a> <a id="20027" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="20068" class="Keyword">open</a> <a id="20073" class="Keyword">import</a> <a id="20080" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="20109" class="Keyword">open</a> <a id="20114" class="Keyword">import</a> <a id="20121" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="20166" class="Keyword">open</a> <a id="20171" class="Keyword">import</a> <a id="20178" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="20222" class="Keyword">open</a> <a id="20227" class="Keyword">import</a> <a id="20234" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="20261" class="Keyword">open</a> <a id="20266" class="Keyword">import</a> <a id="20273" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="20314" class="Keyword">open</a> <a id="20319" class="Keyword">import</a> <a id="20326" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="20349" class="Keyword">open</a> <a id="20354" class="Keyword">import</a> <a id="20361" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="20410" class="Keyword">open</a> <a id="20415" class="Keyword">import</a> <a id="20422" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="20461" class="Keyword">open</a> <a id="20466" class="Keyword">import</a> <a id="20473" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="20514" class="Keyword">open</a> <a id="20519" class="Keyword">import</a> <a id="20526" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="20570" class="Keyword">open</a> <a id="20575" class="Keyword">import</a> <a id="20582" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="20619" class="Keyword">open</a> <a id="20624" class="Keyword">import</a> <a id="20631" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="20653" class="Keyword">open</a> <a id="20658" class="Keyword">import</a> <a id="20665" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="20695" class="Keyword">open</a> <a id="20700" class="Keyword">import</a> <a id="20707" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="20746" class="Keyword">open</a> <a id="20751" class="Keyword">import</a> <a id="20758" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="20796" class="Keyword">open</a> <a id="20801" class="Keyword">import</a> <a id="20808" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="20839" class="Keyword">open</a> <a id="20844" class="Keyword">import</a> <a id="20851" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="20909" class="Keyword">open</a> <a id="20914" class="Keyword">import</a> <a id="20921" href="group-theory.html" class="Module">group-theory</a>
<a id="20934" class="Keyword">open</a> <a id="20939" class="Keyword">import</a> <a id="20946" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="20974" class="Keyword">open</a> <a id="20979" class="Keyword">import</a> <a id="20986" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="21017" class="Keyword">open</a> <a id="21022" class="Keyword">import</a> <a id="21029" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="21065" class="Keyword">open</a> <a id="21070" class="Keyword">import</a> <a id="21077" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="21128" class="Keyword">open</a> <a id="21133" class="Keyword">import</a> <a id="21140" href="group-theory.automorphism-groups.html" class="Module">group-theory.automorphism-groups</a>
<a id="21173" class="Keyword">open</a> <a id="21178" class="Keyword">import</a> <a id="21185" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="21217" class="Keyword">open</a> <a id="21222" class="Keyword">import</a> <a id="21229" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="21265" class="Keyword">open</a> <a id="21270" class="Keyword">import</a> <a id="21277" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="21306" class="Keyword">open</a> <a id="21311" class="Keyword">import</a> <a id="21318" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="21354" class="Keyword">open</a> <a id="21359" class="Keyword">import</a> <a id="21366" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="21395" class="Keyword">open</a> <a id="21400" class="Keyword">import</a> <a id="21407" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="21439" class="Keyword">open</a> <a id="21444" class="Keyword">import</a> <a id="21451" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="21476" class="Keyword">open</a> <a id="21481" class="Keyword">import</a> <a id="21488" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="21519" class="Keyword">open</a> <a id="21524" class="Keyword">import</a> <a id="21531" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="21578" class="Keyword">open</a> <a id="21583" class="Keyword">import</a> <a id="21590" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="21630" class="Keyword">open</a> <a id="21635" class="Keyword">import</a> <a id="21642" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="21679" class="Keyword">open</a> <a id="21684" class="Keyword">import</a> <a id="21691" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="21727" class="Keyword">open</a> <a id="21732" class="Keyword">import</a> <a id="21739" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="21771" class="Keyword">open</a> <a id="21776" class="Keyword">import</a> <a id="21783" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="21810" class="Keyword">open</a> <a id="21815" class="Keyword">import</a> <a id="21822" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="21842" class="Keyword">open</a> <a id="21847" class="Keyword">import</a> <a id="21854" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="21881" class="Keyword">open</a> <a id="21886" class="Keyword">import</a> <a id="21893" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="21935" class="Keyword">open</a> <a id="21940" class="Keyword">import</a> <a id="21947" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="21988" class="Keyword">open</a> <a id="21993" class="Keyword">import</a> <a id="22000" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="22034" class="Keyword">open</a> <a id="22039" class="Keyword">import</a> <a id="22046" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="22081" class="Keyword">open</a> <a id="22086" class="Keyword">import</a> <a id="22093" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="22131" class="Keyword">open</a> <a id="22136" class="Keyword">import</a> <a id="22143" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="22175" class="Keyword">open</a> <a id="22180" class="Keyword">import</a> <a id="22187" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="22228" class="Keyword">open</a> <a id="22233" class="Keyword">import</a> <a id="22240" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="22281" class="Keyword">open</a> <a id="22286" class="Keyword">import</a> <a id="22293" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="22333" class="Keyword">open</a> <a id="22338" class="Keyword">import</a> <a id="22345" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="22378" class="Keyword">open</a> <a id="22383" class="Keyword">import</a> <a id="22390" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="22427" class="Keyword">open</a> <a id="22432" class="Keyword">import</a> <a id="22439" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="22484" class="Keyword">open</a> <a id="22489" class="Keyword">import</a> <a id="22496" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="22517" class="Keyword">open</a> <a id="22522" class="Keyword">import</a> <a id="22529" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="22563" class="Keyword">open</a> <a id="22568" class="Keyword">import</a> <a id="22575" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="22617" class="Keyword">open</a> <a id="22622" class="Keyword">import</a> <a id="22629" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="22664" class="Keyword">open</a> <a id="22669" class="Keyword">import</a> <a id="22676" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="22715" class="Keyword">open</a> <a id="22720" class="Keyword">import</a> <a id="22727" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="22764" class="Keyword">open</a> <a id="22769" class="Keyword">import</a> <a id="22776" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="22800" class="Keyword">open</a> <a id="22805" class="Keyword">import</a> <a id="22812" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="22837" class="Keyword">open</a> <a id="22842" class="Keyword">import</a> <a id="22849" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="22880" class="Keyword">open</a> <a id="22885" class="Keyword">import</a> <a id="22892" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="22915" class="Keyword">open</a> <a id="22920" class="Keyword">import</a> <a id="22927" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="22975" class="Keyword">open</a> <a id="22980" class="Keyword">import</a> <a id="22987" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="23017" class="Keyword">open</a> <a id="23022" class="Keyword">import</a> <a id="23029" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="23099" class="Keyword">open</a> <a id="23104" class="Keyword">import</a> <a id="23111" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="23126" class="Keyword">open</a> <a id="23131" class="Keyword">import</a> <a id="23138" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="23171" class="Keyword">open</a> <a id="23176" class="Keyword">import</a> <a id="23183" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="23215" class="Keyword">open</a> <a id="23220" class="Keyword">import</a> <a id="23227" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="23269" class="Keyword">open</a> <a id="23274" class="Keyword">import</a> <a id="23281" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="23319" class="Keyword">open</a> <a id="23324" class="Keyword">import</a> <a id="23331" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="23368" class="Keyword">open</a> <a id="23373" class="Keyword">import</a> <a id="23380" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="23413" class="Keyword">open</a> <a id="23418" class="Keyword">import</a> <a id="23425" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="23449" class="Keyword">open</a> <a id="23454" class="Keyword">import</a> <a id="23461" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="23500" class="Keyword">open</a> <a id="23505" class="Keyword">import</a> <a id="23512" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="23558" class="Keyword">open</a> <a id="23563" class="Keyword">import</a> <a id="23570" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="23615" class="Keyword">open</a> <a id="23620" class="Keyword">import</a> <a id="23627" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="23665" class="Keyword">open</a> <a id="23670" class="Keyword">import</a> <a id="23677" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="23709" class="Keyword">open</a> <a id="23714" class="Keyword">import</a> <a id="23721" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="23774" class="Keyword">open</a> <a id="23779" class="Keyword">import</a> <a id="23786" href="order-theory.html" class="Module">order-theory</a>
<a id="23799" class="Keyword">open</a> <a id="23804" class="Keyword">import</a> <a id="23811" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="23838" class="Keyword">open</a> <a id="23843" class="Keyword">import</a> <a id="23850" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="23880" class="Keyword">open</a> <a id="23885" class="Keyword">import</a> <a id="23892" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="23925" class="Keyword">open</a> <a id="23930" class="Keyword">import</a> <a id="23937" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="23973" class="Keyword">open</a> <a id="23978" class="Keyword">import</a> <a id="23985" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="24012" class="Keyword">open</a> <a id="24017" class="Keyword">import</a> <a id="24024" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="24054" class="Keyword">open</a> <a id="24059" class="Keyword">import</a> <a id="24066" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="24102" class="Keyword">open</a> <a id="24107" class="Keyword">import</a> <a id="24114" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="24156" class="Keyword">open</a> <a id="24161" class="Keyword">import</a> <a id="24168" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="24200" class="Keyword">open</a> <a id="24205" class="Keyword">import</a> <a id="24212" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="24249" class="Keyword">open</a> <a id="24254" class="Keyword">import</a> <a id="24261" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="24301" class="Keyword">open</a> <a id="24306" class="Keyword">import</a> <a id="24313" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="24348" class="Keyword">open</a> <a id="24353" class="Keyword">import</a> <a id="24360" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="24398" class="Keyword">open</a> <a id="24403" class="Keyword">import</a> <a id="24410" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="24445" class="Keyword">open</a> <a id="24450" class="Keyword">import</a> <a id="24457" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="24492" class="Keyword">open</a> <a id="24497" class="Keyword">import</a> <a id="24504" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="24542" class="Keyword">open</a> <a id="24547" class="Keyword">import</a> <a id="24554" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="24585" class="Keyword">open</a> <a id="24590" class="Keyword">import</a> <a id="24597" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="24630" class="Keyword">open</a> <a id="24635" class="Keyword">import</a> <a id="24642" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="24662" class="Keyword">open</a> <a id="24667" class="Keyword">import</a> <a id="24674" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="24697" class="Keyword">open</a> <a id="24702" class="Keyword">import</a> <a id="24709" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="24732" class="Keyword">open</a> <a id="24737" class="Keyword">import</a> <a id="24744" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="24770" class="Keyword">open</a> <a id="24775" class="Keyword">import</a> <a id="24782" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="24808" class="Keyword">open</a> <a id="24813" class="Keyword">import</a> <a id="24820" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="24876" class="Keyword">open</a> <a id="24881" class="Keyword">import</a> <a id="24888" href="polytopes.html" class="Module">polytopes</a>
<a id="24898" class="Keyword">open</a> <a id="24903" class="Keyword">import</a> <a id="24910" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="24968" class="Keyword">open</a> <a id="24973" class="Keyword">import</a> <a id="24980" href="ring-theory.html" class="Module">ring-theory</a>
<a id="24992" class="Keyword">open</a> <a id="24997" class="Keyword">import</a> <a id="25004" href="ring-theory.commutative-rings.html" class="Module">ring-theory.commutative-rings</a>
<a id="25034" class="Keyword">open</a> <a id="25039" class="Keyword">import</a> <a id="25046" href="ring-theory.discrete-fields.html" class="Module">ring-theory.discrete-fields</a>
<a id="25074" class="Keyword">open</a> <a id="25079" class="Keyword">import</a> <a id="25086" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="25113" class="Keyword">open</a> <a id="25118" class="Keyword">import</a> <a id="25125" href="ring-theory.eisenstein-integers.html" class="Module">ring-theory.eisenstein-integers</a>
<a id="25157" class="Keyword">open</a> <a id="25162" class="Keyword">import</a> <a id="25169" href="ring-theory.gaussian-integers.html" class="Module">ring-theory.gaussian-integers</a>
<a id="25199" class="Keyword">open</a> <a id="25204" class="Keyword">import</a> <a id="25211" href="ring-theory.homomorphisms-commutative-rings.html" class="Module">ring-theory.homomorphisms-commutative-rings</a>
<a id="25255" class="Keyword">open</a> <a id="25260" class="Keyword">import</a> <a id="25267" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="25299" class="Keyword">open</a> <a id="25304" class="Keyword">import</a> <a id="25311" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="25357" class="Keyword">open</a> <a id="25362" class="Keyword">import</a> <a id="25369" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="25394" class="Keyword">open</a> <a id="25399" class="Keyword">import</a> <a id="25406" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="25444" class="Keyword">open</a> <a id="25449" class="Keyword">import</a> <a id="25456" href="ring-theory.isomorphisms-commutative-rings.html" class="Module">ring-theory.isomorphisms-commutative-rings</a>
<a id="25499" class="Keyword">open</a> <a id="25504" class="Keyword">import</a> <a id="25511" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="25542" class="Keyword">open</a> <a id="25547" class="Keyword">import</a> <a id="25554" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="25586" class="Keyword">open</a> <a id="25591" class="Keyword">import</a> <a id="25598" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="25627" class="Keyword">open</a> <a id="25632" class="Keyword">import</a> <a id="25639" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="25700" class="Keyword">open</a> <a id="25705" class="Keyword">import</a> <a id="25712" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="25738" class="Keyword">open</a> <a id="25743" class="Keyword">import</a> <a id="25750" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="25789" class="Keyword">open</a> <a id="25794" class="Keyword">import</a> <a id="25801" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="25839" class="Keyword">open</a> <a id="25844" class="Keyword">import</a> <a id="25851" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="25897" class="Keyword">open</a> <a id="25902" class="Keyword">import</a> <a id="25909" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="25946" class="Keyword">open</a> <a id="25951" class="Keyword">import</a> <a id="25958" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="25998" class="Keyword">open</a> <a id="26003" class="Keyword">import</a> <a id="26010" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="26049" class="Keyword">open</a> <a id="26054" class="Keyword">import</a> <a id="26061" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="26094" class="Keyword">open</a> <a id="26099" class="Keyword">import</a> <a id="26106" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="26155" class="Keyword">open</a> <a id="26160" class="Keyword">import</a> <a id="26167" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="26206" class="Keyword">open</a> <a id="26211" class="Keyword">import</a> <a id="26218" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="26263" class="Keyword">open</a> <a id="26268" class="Keyword">import</a> <a id="26275" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="26327" class="Keyword">open</a> <a id="26332" class="Keyword">import</a> <a id="26339" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="26392" class="Keyword">open</a> <a id="26397" class="Keyword">import</a> <a id="26404" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="26452" class="Keyword">open</a> <a id="26457" class="Keyword">import</a> <a id="26464" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="26504" class="Keyword">open</a> <a id="26509" class="Keyword">import</a> <a id="26516" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="26563" class="Keyword">open</a> <a id="26568" class="Keyword">import</a> <a id="26575" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="26613" class="Keyword">open</a> <a id="26618" class="Keyword">import</a> <a id="26625" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="26679" class="Keyword">open</a> <a id="26684" class="Keyword">import</a> <a id="26691" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="26738" class="Keyword">open</a> <a id="26743" class="Keyword">import</a> <a id="26750" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="26802" class="Keyword">open</a> <a id="26807" class="Keyword">import</a> <a id="26814" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="26859" class="Keyword">open</a> <a id="26864" class="Keyword">import</a> <a id="26871" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="26910" class="Keyword">open</a> <a id="26915" class="Keyword">import</a> <a id="26922" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="26962" class="Keyword">open</a> <a id="26967" class="Keyword">import</a> <a id="26974" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="27007" class="Keyword">open</a> <a id="27012" class="Keyword">import</a> <a id="27019" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="27064" class="Keyword">open</a> <a id="27069" class="Keyword">import</a> <a id="27076" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="27152" class="Keyword">open</a> <a id="27157" class="Keyword">import</a> <a id="27164" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Type theories

<pre class="Agda"><a id="27216" class="Keyword">open</a> <a id="27221" class="Keyword">import</a> <a id="27228" href="type-theories.html" class="Module">type-theories</a>
<a id="27242" class="Keyword">open</a> <a id="27247" class="Keyword">import</a> <a id="27254" href="type-theories.comprehension-type-theories.html" class="Module">type-theories.comprehension-type-theories</a>
<a id="27296" class="Keyword">open</a> <a id="27301" class="Keyword">import</a> <a id="27308" href="type-theories.dependent-type-theories.html" class="Module">type-theories.dependent-type-theories</a>
<a id="27346" class="Keyword">open</a> <a id="27351" class="Keyword">import</a> <a id="27358" href="type-theories.fibered-dependent-type-theories.html" class="Module">type-theories.fibered-dependent-type-theories</a>
<a id="27404" class="Keyword">open</a> <a id="27409" class="Keyword">import</a> <a id="27416" href="type-theories.sections-dependent-type-theories.html" class="Module">type-theories.sections-dependent-type-theories</a>
<a id="27463" class="Keyword">open</a> <a id="27468" class="Keyword">import</a> <a id="27475" href="type-theories.simple-type-theories.html" class="Module">type-theories.simple-type-theories</a>
<a id="27510" class="Keyword">open</a> <a id="27515" class="Keyword">import</a> <a id="27522" href="type-theories.unityped-type-theories.html" class="Module">type-theories.unityped-type-theories</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="27600" class="Keyword">open</a> <a id="27605" class="Keyword">import</a> <a id="27612" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="27636" class="Keyword">open</a> <a id="27641" class="Keyword">import</a> <a id="27648" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="27701" class="Keyword">open</a> <a id="27706" class="Keyword">import</a> <a id="27713" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="27756" class="Keyword">open</a> <a id="27761" class="Keyword">import</a> <a id="27768" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="27808" class="Keyword">open</a> <a id="27813" class="Keyword">import</a> <a id="27820" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="27859" class="Keyword">open</a> <a id="27864" class="Keyword">import</a> <a id="27871" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="27919" class="Keyword">open</a> <a id="27924" class="Keyword">import</a> <a id="27931" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="27978" class="Keyword">open</a> <a id="27983" class="Keyword">import</a> <a id="27990" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="28042" class="Keyword">open</a> <a id="28047" class="Keyword">import</a> <a id="28054" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="28094" class="Keyword">open</a> <a id="28099" class="Keyword">import</a> <a id="28106" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="28158" class="Keyword">open</a> <a id="28163" class="Keyword">import</a> <a id="28170" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="28224" class="Keyword">open</a> <a id="28229" class="Keyword">import</a> <a id="28236" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="28275" class="Keyword">open</a> <a id="28280" class="Keyword">import</a> <a id="28287" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="28320" class="Keyword">open</a> <a id="28325" class="Keyword">import</a> <a id="28332" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="28362" class="Keyword">open</a> <a id="28367" class="Keyword">import</a> <a id="28374" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="28433" class="Keyword">open</a> <a id="28438" class="Keyword">import</a> <a id="28445" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="28500" class="Keyword">open</a> <a id="28505" class="Keyword">import</a> <a id="28512" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="28555" class="Keyword">open</a> <a id="28560" class="Keyword">import</a> <a id="28567" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="28616" class="Keyword">open</a> <a id="28621" class="Keyword">import</a> <a id="28628" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="28673" class="Keyword">open</a> <a id="28678" class="Keyword">import</a> <a id="28685" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="28736" class="Keyword">open</a> <a id="28741" class="Keyword">import</a> <a id="28748" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="28826" class="Keyword">open</a> <a id="28831" class="Keyword">import</a> <a id="28838" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="28878" class="Keyword">open</a> <a id="28883" class="Keyword">import</a> <a id="28890" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="28947" class="Keyword">open</a> <a id="28952" class="Keyword">import</a> <a id="28959" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="28994" class="Keyword">open</a> <a id="28999" class="Keyword">import</a> <a id="29006" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="29052" class="Keyword">open</a> <a id="29057" class="Keyword">import</a> <a id="29064" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="29119" class="Keyword">open</a> <a id="29124" class="Keyword">import</a> <a id="29131" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="29174" class="Keyword">open</a> <a id="29179" class="Keyword">import</a> <a id="29186" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="29245" class="Keyword">open</a> <a id="29250" class="Keyword">import</a> <a id="29257" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="29294" class="Keyword">open</a> <a id="29299" class="Keyword">import</a> <a id="29306" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="29345" class="Keyword">open</a> <a id="29350" class="Keyword">import</a> <a id="29357" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="29395" class="Keyword">open</a> <a id="29400" class="Keyword">import</a> <a id="29407" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="29459" class="Keyword">open</a> <a id="29464" class="Keyword">import</a> <a id="29471" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="29516" class="Keyword">open</a> <a id="29521" class="Keyword">import</a> <a id="29528" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="29565" class="Keyword">open</a> <a id="29570" class="Keyword">import</a> <a id="29577" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="29626" class="Keyword">open</a> <a id="29631" class="Keyword">import</a> <a id="29638" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="29677" class="Keyword">open</a> <a id="29682" class="Keyword">import</a> <a id="29689" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="29727" class="Keyword">open</a> <a id="29732" class="Keyword">import</a> <a id="29739" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="29794" class="Keyword">open</a> <a id="29799" class="Keyword">import</a> <a id="29806" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="29845" class="Keyword">open</a> <a id="29850" class="Keyword">import</a> <a id="29857" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="29904" class="Keyword">open</a> <a id="29909" class="Keyword">import</a> <a id="29916" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="29946" class="Keyword">open</a> <a id="29951" class="Keyword">import</a> <a id="29958" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="29988" class="Keyword">open</a> <a id="29993" class="Keyword">import</a> <a id="30000" href="univalent-combinatorics.orientations-complete-undirected-graph.html" class="Module">univalent-combinatorics.orientations-complete-undirected-graph</a>
<a id="30063" class="Keyword">open</a> <a id="30068" class="Keyword">import</a> <a id="30075" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="30118" class="Keyword">open</a> <a id="30123" class="Keyword">import</a> <a id="30130" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="30165" class="Keyword">open</a> <a id="30170" class="Keyword">import</a> <a id="30177" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="30217" class="Keyword">open</a> <a id="30222" class="Keyword">import</a> <a id="30229" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="30274" class="Keyword">open</a> <a id="30279" class="Keyword">import</a> <a id="30286" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="30336" class="Keyword">open</a> <a id="30341" class="Keyword">import</a> <a id="30348" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="30386" class="Keyword">open</a> <a id="30391" class="Keyword">import</a> <a id="30398" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="30447" class="Keyword">open</a> <a id="30452" class="Keyword">import</a> <a id="30459" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="30522" class="Keyword">open</a> <a id="30527" class="Keyword">import</a> <a id="30534" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="30566" class="Keyword">open</a> <a id="30571" class="Keyword">import</a> <a id="30578" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="30631" class="Keyword">open</a> <a id="30636" class="Keyword">import</a> <a id="30643" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="30689" class="Keyword">open</a> <a id="30694" class="Keyword">import</a> <a id="30701" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="30747" class="Keyword">open</a> <a id="30752" class="Keyword">import</a> <a id="30759" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="30807" class="Keyword">open</a> <a id="30812" class="Keyword">import</a> <a id="30819" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
<a id="30859" class="Keyword">open</a> <a id="30864" class="Keyword">import</a> <a id="30871" href="univalent-combinatorics.symmetric-difference.html" class="Module">univalent-combinatorics.symmetric-difference</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="30946" class="Keyword">open</a> <a id="30951" class="Keyword">import</a> <a id="30958" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="30971" class="Keyword">open</a> <a id="30976" class="Keyword">import</a> <a id="30983" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="31003" class="Keyword">open</a> <a id="31008" class="Keyword">import</a> <a id="31015" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="31045" class="Keyword">open</a> <a id="31050" class="Keyword">import</a> <a id="31057" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="31099" class="Keyword">open</a> <a id="31104" class="Keyword">import</a> <a id="31111" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="31162" class="Keyword">open</a> <a id="31167" class="Keyword">import</a> <a id="31174" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="31199" class="Keyword">open</a> <a id="31204" class="Keyword">import</a> <a id="31211" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="31235" class="Keyword">open</a> <a id="31240" class="Keyword">import</a> <a id="31247" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="31273" class="Keyword">open</a> <a id="31278" class="Keyword">import</a> <a id="31285" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="31315" class="Keyword">open</a> <a id="31320" class="Keyword">import</a> <a id="31327" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="31356" class="Keyword">open</a> <a id="31361" class="Keyword">import</a> <a id="31368" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

