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
## Commutative algebra

<pre class="Agda"><a id="4590" class="Keyword">open</a> <a id="4595" class="Keyword">import</a> <a id="4602" href="commutative-algebra.html" class="Module">commutative-algebra</a>
<a id="4622" class="Keyword">open</a> <a id="4627" class="Keyword">import</a> <a id="4634" href="commutative-algebra.commutative-rings.html" class="Module">commutative-algebra.commutative-rings</a>
<a id="4672" class="Keyword">open</a> <a id="4677" class="Keyword">import</a> <a id="4684" href="commutative-algebra.discrete-fields.html" class="Module">commutative-algebra.discrete-fields</a>
<a id="4720" class="Keyword">open</a> <a id="4725" class="Keyword">import</a> <a id="4732" href="commutative-algebra.eisenstein-integers.html" class="Module">commutative-algebra.eisenstein-integers</a>
<a id="4772" class="Keyword">open</a> <a id="4777" class="Keyword">import</a> <a id="4784" href="commutative-algebra.gaussian-integers.html" class="Module">commutative-algebra.gaussian-integers</a>
<a id="4822" class="Keyword">open</a> <a id="4827" class="Keyword">import</a> <a id="4834" href="commutative-algebra.homomorphisms-commutative-rings.html" class="Module">commutative-algebra.homomorphisms-commutative-rings</a>
<a id="4886" class="Keyword">open</a> <a id="4891" class="Keyword">import</a> <a id="4898" href="commutative-algebra.ideals-commutative-rings.html" class="Module">commutative-algebra.ideals-commutative-rings</a>
<a id="4943" class="Keyword">open</a> <a id="4948" class="Keyword">import</a> <a id="4955" href="commutative-algebra.isomorphisms-commutative-rings.html" class="Module">commutative-algebra.isomorphisms-commutative-rings</a>
</pre>
## Elementary number theory

<pre class="Agda"><a id="5048" class="Keyword">open</a> <a id="5053" class="Keyword">import</a> <a id="5060" href="elementary-number-theory.html" class="Module">elementary-number-theory</a>
<a id="5085" class="Keyword">open</a> <a id="5090" class="Keyword">import</a> <a id="5097" href="elementary-number-theory.absolute-value-integers.html" class="Module">elementary-number-theory.absolute-value-integers</a>
<a id="5146" class="Keyword">open</a> <a id="5151" class="Keyword">import</a> <a id="5158" href="elementary-number-theory.addition-integers.html" class="Module">elementary-number-theory.addition-integers</a>
<a id="5201" class="Keyword">open</a> <a id="5206" class="Keyword">import</a> <a id="5213" href="elementary-number-theory.addition-natural-numbers.html" class="Module">elementary-number-theory.addition-natural-numbers</a>
<a id="5263" class="Keyword">open</a> <a id="5268" class="Keyword">import</a> <a id="5275" href="elementary-number-theory.arithmetic-functions.html" class="Module">elementary-number-theory.arithmetic-functions</a>
<a id="5321" class="Keyword">open</a> <a id="5326" class="Keyword">import</a> <a id="5333" href="elementary-number-theory.binomial-coefficients.html" class="Module">elementary-number-theory.binomial-coefficients</a>
<a id="5380" class="Keyword">open</a> <a id="5385" class="Keyword">import</a> <a id="5392" href="elementary-number-theory.bounded-sums-arithmetic-functions.html" class="Module">elementary-number-theory.bounded-sums-arithmetic-functions</a>
<a id="5451" class="Keyword">open</a> <a id="5456" class="Keyword">import</a> <a id="5463" href="elementary-number-theory.catalan-numbers.html" class="Module">elementary-number-theory.catalan-numbers</a>
<a id="5504" class="Keyword">open</a> <a id="5509" class="Keyword">import</a> <a id="5516" href="elementary-number-theory.collatz-bijection.html" class="Module">elementary-number-theory.collatz-bijection</a>
<a id="5559" class="Keyword">open</a> <a id="5564" class="Keyword">import</a> <a id="5571" href="elementary-number-theory.collatz-conjecture.html" class="Module">elementary-number-theory.collatz-conjecture</a>
<a id="5615" class="Keyword">open</a> <a id="5620" class="Keyword">import</a> <a id="5627" href="elementary-number-theory.congruence-integers.html" class="Module">elementary-number-theory.congruence-integers</a>
<a id="5672" class="Keyword">open</a> <a id="5677" class="Keyword">import</a> <a id="5684" href="elementary-number-theory.congruence-natural-numbers.html" class="Module">elementary-number-theory.congruence-natural-numbers</a>
<a id="5736" class="Keyword">open</a> <a id="5741" class="Keyword">import</a> <a id="5748" href="elementary-number-theory.decidable-dependent-function-types.html" class="Module">elementary-number-theory.decidable-dependent-function-types</a>
<a id="5808" class="Keyword">open</a> <a id="5813" class="Keyword">import</a> <a id="5820" href="elementary-number-theory.decidable-types.html" class="Module">elementary-number-theory.decidable-types</a>
<a id="5861" class="Keyword">open</a> <a id="5866" class="Keyword">import</a> <a id="5873" href="elementary-number-theory.difference-integers.html" class="Module">elementary-number-theory.difference-integers</a>
<a id="5918" class="Keyword">open</a> <a id="5923" class="Keyword">import</a> <a id="5930" href="elementary-number-theory.dirichlet-convolution.html" class="Module">elementary-number-theory.dirichlet-convolution</a>
<a id="5977" class="Keyword">open</a> <a id="5982" class="Keyword">import</a> <a id="5989" href="elementary-number-theory.distance-integers.html" class="Module">elementary-number-theory.distance-integers</a>
<a id="6032" class="Keyword">open</a> <a id="6037" class="Keyword">import</a> <a id="6044" href="elementary-number-theory.distance-natural-numbers.html" class="Module">elementary-number-theory.distance-natural-numbers</a>
<a id="6094" class="Keyword">open</a> <a id="6099" class="Keyword">import</a> <a id="6106" href="elementary-number-theory.divisibility-integers.html" class="Module">elementary-number-theory.divisibility-integers</a>
<a id="6153" class="Keyword">open</a> <a id="6158" class="Keyword">import</a> <a id="6165" href="elementary-number-theory.divisibility-modular-arithmetic.html" class="Module">elementary-number-theory.divisibility-modular-arithmetic</a>
<a id="6222" class="Keyword">open</a> <a id="6227" class="Keyword">import</a> <a id="6234" href="elementary-number-theory.divisibility-natural-numbers.html" class="Module">elementary-number-theory.divisibility-natural-numbers</a>
<a id="6288" class="Keyword">open</a> <a id="6293" class="Keyword">import</a> <a id="6300" href="elementary-number-theory.divisibility-standard-finite-types.html" class="Module">elementary-number-theory.divisibility-standard-finite-types</a>
<a id="6360" class="Keyword">open</a> <a id="6365" class="Keyword">import</a> <a id="6372" href="elementary-number-theory.equality-integers.html" class="Module">elementary-number-theory.equality-integers</a>
<a id="6415" class="Keyword">open</a> <a id="6420" class="Keyword">import</a> <a id="6427" href="elementary-number-theory.equality-natural-numbers.html" class="Module">elementary-number-theory.equality-natural-numbers</a>
<a id="6477" class="Keyword">open</a> <a id="6482" class="Keyword">import</a> <a id="6489" href="elementary-number-theory.euclidean-division-natural-numbers.html" class="Module">elementary-number-theory.euclidean-division-natural-numbers</a>
<a id="6549" class="Keyword">open</a> <a id="6554" class="Keyword">import</a> <a id="6561" href="elementary-number-theory.eulers-totient-function.html" class="Module">elementary-number-theory.eulers-totient-function</a>
<a id="6610" class="Keyword">open</a> <a id="6615" class="Keyword">import</a> <a id="6622" href="elementary-number-theory.exponentiation-natural-numbers.html" class="Module">elementary-number-theory.exponentiation-natural-numbers</a>
<a id="6678" class="Keyword">open</a> <a id="6683" class="Keyword">import</a> <a id="6690" href="elementary-number-theory.factorials.html" class="Module">elementary-number-theory.factorials</a>
<a id="6726" class="Keyword">open</a> <a id="6731" class="Keyword">import</a> <a id="6738" href="elementary-number-theory.falling-factorials.html" class="Module">elementary-number-theory.falling-factorials</a>
<a id="6782" class="Keyword">open</a> <a id="6787" class="Keyword">import</a> <a id="6794" href="elementary-number-theory.fibonacci-sequence.html" class="Module">elementary-number-theory.fibonacci-sequence</a>
<a id="6838" class="Keyword">open</a> <a id="6843" class="Keyword">import</a> <a id="6850" href="elementary-number-theory.finitary-natural-numbers.html" class="Module">elementary-number-theory.finitary-natural-numbers</a>
<a id="6900" class="Keyword">open</a> <a id="6905" class="Keyword">import</a> <a id="6912" href="elementary-number-theory.finitely-cyclic-maps.html" class="Module">elementary-number-theory.finitely-cyclic-maps</a>
<a id="6958" class="Keyword">open</a> <a id="6963" class="Keyword">import</a> <a id="6970" href="elementary-number-theory.fractions.html" class="Module">elementary-number-theory.fractions</a>
<a id="7005" class="Keyword">open</a> <a id="7010" class="Keyword">import</a> <a id="7017" href="elementary-number-theory.goldbach-conjecture.html" class="Module">elementary-number-theory.goldbach-conjecture</a>
<a id="7062" class="Keyword">open</a> <a id="7067" class="Keyword">import</a> <a id="7074" href="elementary-number-theory.greatest-common-divisor-integers.html" class="Module">elementary-number-theory.greatest-common-divisor-integers</a>
<a id="7132" class="Keyword">open</a> <a id="7137" class="Keyword">import</a> <a id="7144" href="elementary-number-theory.greatest-common-divisor-natural-numbers.html" class="Module">elementary-number-theory.greatest-common-divisor-natural-numbers</a>
<a id="7209" class="Keyword">open</a> <a id="7214" class="Keyword">import</a> <a id="7221" href="elementary-number-theory.group-of-integers.html" class="Module">elementary-number-theory.group-of-integers</a>
<a id="7264" class="Keyword">open</a> <a id="7269" class="Keyword">import</a> <a id="7276" href="elementary-number-theory.groups-of-modular-arithmetic.html" class="Module">elementary-number-theory.groups-of-modular-arithmetic</a>
<a id="7330" class="Keyword">open</a> <a id="7335" class="Keyword">import</a> <a id="7342" href="elementary-number-theory.inequality-integers.html" class="Module">elementary-number-theory.inequality-integers</a>
<a id="7387" class="Keyword">open</a> <a id="7392" class="Keyword">import</a> <a id="7399" href="elementary-number-theory.inequality-natural-numbers.html" class="Module">elementary-number-theory.inequality-natural-numbers</a>
<a id="7451" class="Keyword">open</a> <a id="7456" class="Keyword">import</a> <a id="7463" href="elementary-number-theory.inequality-standard-finite-types.html" class="Module">elementary-number-theory.inequality-standard-finite-types</a>
<a id="7521" class="Keyword">open</a> <a id="7526" class="Keyword">import</a> <a id="7533" href="elementary-number-theory.infinitude-of-primes.html" class="Module">elementary-number-theory.infinitude-of-primes</a>
<a id="7579" class="Keyword">open</a> <a id="7584" class="Keyword">import</a> <a id="7591" href="elementary-number-theory.integers.html" class="Module">elementary-number-theory.integers</a>
<a id="7625" class="Keyword">open</a> <a id="7630" class="Keyword">import</a> <a id="7637" href="elementary-number-theory.iterating-functions.html" class="Module">elementary-number-theory.iterating-functions</a>
<a id="7682" class="Keyword">open</a> <a id="7687" class="Keyword">import</a> <a id="7694" href="elementary-number-theory.lower-bounds-natural-numbers.html" class="Module">elementary-number-theory.lower-bounds-natural-numbers</a>
<a id="7748" class="Keyword">open</a> <a id="7753" class="Keyword">import</a> <a id="7760" href="elementary-number-theory.maximum-natural-numbers.html" class="Module">elementary-number-theory.maximum-natural-numbers</a>
<a id="7809" class="Keyword">open</a> <a id="7814" class="Keyword">import</a> <a id="7821" href="elementary-number-theory.mersenne-primes.html" class="Module">elementary-number-theory.mersenne-primes</a>
<a id="7862" class="Keyword">open</a> <a id="7867" class="Keyword">import</a> <a id="7874" href="elementary-number-theory.minimum-natural-numbers.html" class="Module">elementary-number-theory.minimum-natural-numbers</a>
<a id="7923" class="Keyword">open</a> <a id="7928" class="Keyword">import</a> <a id="7935" href="elementary-number-theory.modular-arithmetic-standard-finite-types.html" class="Module">elementary-number-theory.modular-arithmetic-standard-finite-types</a>
<a id="8001" class="Keyword">open</a> <a id="8006" class="Keyword">import</a> <a id="8013" href="elementary-number-theory.modular-arithmetic.html" class="Module">elementary-number-theory.modular-arithmetic</a>
<a id="8057" class="Keyword">open</a> <a id="8062" class="Keyword">import</a> <a id="8069" href="elementary-number-theory.multiplication-integers.html" class="Module">elementary-number-theory.multiplication-integers</a>
<a id="8118" class="Keyword">open</a> <a id="8123" class="Keyword">import</a> <a id="8130" href="elementary-number-theory.multiplication-natural-numbers.html" class="Module">elementary-number-theory.multiplication-natural-numbers</a>
<a id="8186" class="Keyword">open</a> <a id="8191" class="Keyword">import</a> <a id="8198" href="elementary-number-theory.natural-numbers.html" class="Module">elementary-number-theory.natural-numbers</a>
<a id="8239" class="Keyword">open</a> <a id="8244" class="Keyword">import</a> <a id="8251" href="elementary-number-theory.nonzero-natural-numbers.html" class="Module">elementary-number-theory.nonzero-natural-numbers</a>
<a id="8300" class="Keyword">open</a> <a id="8305" class="Keyword">import</a> <a id="8312" href="elementary-number-theory.ordinal-induction-natural-numbers.html" class="Module">elementary-number-theory.ordinal-induction-natural-numbers</a>
<a id="8371" class="Keyword">open</a> <a id="8376" class="Keyword">import</a> <a id="8383" href="elementary-number-theory.prime-numbers.html" class="Module">elementary-number-theory.prime-numbers</a>
<a id="8422" class="Keyword">open</a> <a id="8427" class="Keyword">import</a> <a id="8434" href="elementary-number-theory.products-of-natural-numbers.html" class="Module">elementary-number-theory.products-of-natural-numbers</a>
<a id="8487" class="Keyword">open</a> <a id="8492" class="Keyword">import</a> <a id="8499" href="elementary-number-theory.proper-divisors-natural-numbers.html" class="Module">elementary-number-theory.proper-divisors-natural-numbers</a>
<a id="8556" class="Keyword">open</a> <a id="8561" class="Keyword">import</a> <a id="8568" href="elementary-number-theory.rational-numbers.html" class="Module">elementary-number-theory.rational-numbers</a>
<a id="8610" class="Keyword">open</a> <a id="8615" class="Keyword">import</a> <a id="8622" href="elementary-number-theory.relatively-prime-integers.html" class="Module">elementary-number-theory.relatively-prime-integers</a>
<a id="8673" class="Keyword">open</a> <a id="8678" class="Keyword">import</a> <a id="8685" href="elementary-number-theory.relatively-prime-natural-numbers.html" class="Module">elementary-number-theory.relatively-prime-natural-numbers</a>
<a id="8743" class="Keyword">open</a> <a id="8748" class="Keyword">import</a> <a id="8755" href="elementary-number-theory.repeating-element-standard-finite-type.html" class="Module">elementary-number-theory.repeating-element-standard-finite-type</a>
<a id="8819" class="Keyword">open</a> <a id="8824" class="Keyword">import</a> <a id="8831" href="elementary-number-theory.retracts-of-natural-numbers.html" class="Module">elementary-number-theory.retracts-of-natural-numbers</a>
<a id="8884" class="Keyword">open</a> <a id="8889" class="Keyword">import</a> <a id="8896" href="elementary-number-theory.square-free-natural-numbers.html" class="Module">elementary-number-theory.square-free-natural-numbers</a>
<a id="8949" class="Keyword">open</a> <a id="8954" class="Keyword">import</a> <a id="8961" href="elementary-number-theory.stirling-numbers-of-the-second-kind.html" class="Module">elementary-number-theory.stirling-numbers-of-the-second-kind</a>
<a id="9022" class="Keyword">open</a> <a id="9027" class="Keyword">import</a> <a id="9034" href="elementary-number-theory.strong-induction-natural-numbers.html" class="Module">elementary-number-theory.strong-induction-natural-numbers</a>
<a id="9092" class="Keyword">open</a> <a id="9097" class="Keyword">import</a> <a id="9104" href="elementary-number-theory.sums-of-natural-numbers.html" class="Module">elementary-number-theory.sums-of-natural-numbers</a>
<a id="9153" class="Keyword">open</a> <a id="9158" class="Keyword">import</a> <a id="9165" href="elementary-number-theory.triangular-numbers.html" class="Module">elementary-number-theory.triangular-numbers</a>
<a id="9209" class="Keyword">open</a> <a id="9214" class="Keyword">import</a> <a id="9221" href="elementary-number-theory.telephone-numbers.html" class="Module">elementary-number-theory.telephone-numbers</a>
<a id="9264" class="Keyword">open</a> <a id="9269" class="Keyword">import</a> <a id="9276" href="elementary-number-theory.twin-prime-conjecture.html" class="Module">elementary-number-theory.twin-prime-conjecture</a>
<a id="9323" class="Keyword">open</a> <a id="9328" class="Keyword">import</a> <a id="9335" href="elementary-number-theory.unit-elements-standard-finite-types.html" class="Module">elementary-number-theory.unit-elements-standard-finite-types</a>
<a id="9396" class="Keyword">open</a> <a id="9401" class="Keyword">import</a> <a id="9408" href="elementary-number-theory.unit-similarity-standard-finite-types.html" class="Module">elementary-number-theory.unit-similarity-standard-finite-types</a>
<a id="9471" class="Keyword">open</a> <a id="9476" class="Keyword">import</a> <a id="9483" href="elementary-number-theory.universal-property-natural-numbers.html" class="Module">elementary-number-theory.universal-property-natural-numbers</a>
<a id="9543" class="Keyword">open</a> <a id="9548" class="Keyword">import</a> <a id="9555" href="elementary-number-theory.upper-bounds-natural-numbers.html" class="Module">elementary-number-theory.upper-bounds-natural-numbers</a>
<a id="9609" class="Keyword">open</a> <a id="9614" class="Keyword">import</a> <a id="9621" href="elementary-number-theory.well-ordering-principle-natural-numbers.html" class="Module">elementary-number-theory.well-ordering-principle-natural-numbers</a>
<a id="9686" class="Keyword">open</a> <a id="9691" class="Keyword">import</a> <a id="9698" href="elementary-number-theory.well-ordering-principle-standard-finite-types.html" class="Module">elementary-number-theory.well-ordering-principle-standard-finite-types</a>
</pre>
## Finite group theory

<pre class="Agda"><a id="9806" class="Keyword">open</a> <a id="9811" class="Keyword">import</a> <a id="9818" href="finite-group-theory.html" class="Module">finite-group-theory</a>
<a id="9838" class="Keyword">open</a> <a id="9843" class="Keyword">import</a> <a id="9850" href="finite-group-theory.abstract-quaternion-group.html" class="Module">finite-group-theory.abstract-quaternion-group</a>
<a id="9896" class="Keyword">open</a> <a id="9901" class="Keyword">import</a> <a id="9908" href="finite-group-theory.concrete-quaternion-group.html" class="Module">finite-group-theory.concrete-quaternion-group</a>
<a id="9954" class="Keyword">open</a> <a id="9959" class="Keyword">import</a> <a id="9966" href="finite-group-theory.finite-groups.html" class="Module">finite-group-theory.finite-groups</a>
<a id="10000" class="Keyword">open</a> <a id="10005" class="Keyword">import</a> <a id="10012" href="finite-group-theory.finite-monoids.html" class="Module">finite-group-theory.finite-monoids</a>
<a id="10047" class="Keyword">open</a> <a id="10052" class="Keyword">import</a> <a id="10059" href="finite-group-theory.finite-semigroups.html" class="Module">finite-group-theory.finite-semigroups</a>
<a id="10097" class="Keyword">open</a> <a id="10102" class="Keyword">import</a> <a id="10109" href="finite-group-theory.groups-of-order-2.html" class="Module">finite-group-theory.groups-of-order-2</a>
<a id="10147" class="Keyword">open</a> <a id="10152" class="Keyword">import</a> <a id="10159" href="finite-group-theory.orbits-permutations.html" class="Module">finite-group-theory.orbits-permutations</a>
<a id="10199" class="Keyword">open</a> <a id="10204" class="Keyword">import</a> <a id="10211" href="finite-group-theory.permutations.html" class="Module">finite-group-theory.permutations</a>
<a id="10244" class="Keyword">open</a> <a id="10249" class="Keyword">import</a> <a id="10256" href="finite-group-theory.sign-homomorphism.html" class="Module">finite-group-theory.sign-homomorphism</a>
<a id="10294" class="Keyword">open</a> <a id="10299" class="Keyword">import</a> <a id="10306" href="finite-group-theory.transpositions.html" class="Module">finite-group-theory.transpositions</a>
</pre>
## Foundation

<pre class="Agda"><a id="10369" class="Keyword">open</a> <a id="10374" class="Keyword">import</a> <a id="10381" href="foundation.html" class="Module">foundation</a>
<a id="10392" class="Keyword">open</a> <a id="10397" class="Keyword">import</a> <a id="10404" href="foundation.0-maps.html" class="Module">foundation.0-maps</a>
<a id="10422" class="Keyword">open</a> <a id="10427" class="Keyword">import</a> <a id="10434" href="foundation.1-types.html" class="Module">foundation.1-types</a>
<a id="10453" class="Keyword">open</a> <a id="10458" class="Keyword">import</a> <a id="10465" href="foundation.2-types.html" class="Module">foundation.2-types</a>
<a id="10484" class="Keyword">open</a> <a id="10489" class="Keyword">import</a> <a id="10496" href="foundation.algebras-polynomial-endofunctors.html" class="Module">foundation.algebras-polynomial-endofunctors</a>
<a id="10540" class="Keyword">open</a> <a id="10545" class="Keyword">import</a> <a id="10552" href="foundation.automorphisms.html" class="Module">foundation.automorphisms</a>
<a id="10577" class="Keyword">open</a> <a id="10582" class="Keyword">import</a> <a id="10589" href="foundation.axiom-of-choice.html" class="Module">foundation.axiom-of-choice</a>
<a id="10616" class="Keyword">open</a> <a id="10621" class="Keyword">import</a> <a id="10628" href="foundation.binary-embeddings.html" class="Module">foundation.binary-embeddings</a>
<a id="10657" class="Keyword">open</a> <a id="10662" class="Keyword">import</a> <a id="10669" href="foundation.binary-equivalences.html" class="Module">foundation.binary-equivalences</a>
<a id="10700" class="Keyword">open</a> <a id="10705" class="Keyword">import</a> <a id="10712" href="foundation.binary-relations.html" class="Module">foundation.binary-relations</a>
<a id="10740" class="Keyword">open</a> <a id="10745" class="Keyword">import</a> <a id="10752" href="foundation.boolean-reflection.html" class="Module">foundation.boolean-reflection</a>
<a id="10782" class="Keyword">open</a> <a id="10787" class="Keyword">import</a> <a id="10794" href="foundation.booleans.html" class="Module">foundation.booleans</a>
<a id="10814" class="Keyword">open</a> <a id="10819" class="Keyword">import</a> <a id="10826" href="foundation.cantors-diagonal-argument.html" class="Module">foundation.cantors-diagonal-argument</a>
<a id="10863" class="Keyword">open</a> <a id="10868" class="Keyword">import</a> <a id="10875" href="foundation.cartesian-product-types.html" class="Module">foundation.cartesian-product-types</a>
<a id="10910" class="Keyword">open</a> <a id="10915" class="Keyword">import</a> <a id="10922" href="foundation.choice-of-representatives-equivalence-relation.html" class="Module">foundation.choice-of-representatives-equivalence-relation</a>
<a id="10980" class="Keyword">open</a> <a id="10985" class="Keyword">import</a> <a id="10992" href="foundation.coherently-invertible-maps.html" class="Module">foundation.coherently-invertible-maps</a>
<a id="11030" class="Keyword">open</a> <a id="11035" class="Keyword">import</a> <a id="11042" href="foundation.commuting-squares.html" class="Module">foundation.commuting-squares</a>
<a id="11071" class="Keyword">open</a> <a id="11076" class="Keyword">import</a> <a id="11083" href="foundation.complements.html" class="Module">foundation.complements</a>
<a id="11106" class="Keyword">open</a> <a id="11111" class="Keyword">import</a> <a id="11118" href="foundation.conjunction.html" class="Module">foundation.conjunction</a>
<a id="11141" class="Keyword">open</a> <a id="11146" class="Keyword">import</a> <a id="11153" href="foundation.connected-components-universes.html" class="Module">foundation.connected-components-universes</a>
<a id="11195" class="Keyword">open</a> <a id="11200" class="Keyword">import</a> <a id="11207" href="foundation.connected-components.html" class="Module">foundation.connected-components</a>
<a id="11239" class="Keyword">open</a> <a id="11244" class="Keyword">import</a> <a id="11251" href="foundation.connected-types.html" class="Module">foundation.connected-types</a>
<a id="11278" class="Keyword">open</a> <a id="11283" class="Keyword">import</a> <a id="11290" href="foundation.constant-maps.html" class="Module">foundation.constant-maps</a>
<a id="11315" class="Keyword">open</a> <a id="11320" class="Keyword">import</a> <a id="11327" href="foundation.contractible-maps.html" class="Module">foundation.contractible-maps</a>
<a id="11356" class="Keyword">open</a> <a id="11361" class="Keyword">import</a> <a id="11368" href="foundation.contractible-types.html" class="Module">foundation.contractible-types</a>
<a id="11398" class="Keyword">open</a> <a id="11403" class="Keyword">import</a> <a id="11410" href="foundation.coproduct-types.html" class="Module">foundation.coproduct-types</a>
<a id="11437" class="Keyword">open</a> <a id="11442" class="Keyword">import</a> <a id="11449" href="foundation.coslice.html" class="Module">foundation.coslice</a>
<a id="11468" class="Keyword">open</a> <a id="11473" class="Keyword">import</a> <a id="11480" href="foundation.decidable-dependent-function-types.html" class="Module">foundation.decidable-dependent-function-types</a>
<a id="11526" class="Keyword">open</a> <a id="11531" class="Keyword">import</a> <a id="11538" href="foundation.decidable-dependent-pair-types.html" class="Module">foundation.decidable-dependent-pair-types</a>
<a id="11580" class="Keyword">open</a> <a id="11585" class="Keyword">import</a> <a id="11592" href="foundation.decidable-embeddings.html" class="Module">foundation.decidable-embeddings</a>
<a id="11624" class="Keyword">open</a> <a id="11629" class="Keyword">import</a> <a id="11636" href="foundation.decidable-equality.html" class="Module">foundation.decidable-equality</a>
<a id="11666" class="Keyword">open</a> <a id="11671" class="Keyword">import</a> <a id="11678" href="foundation.decidable-maps.html" class="Module">foundation.decidable-maps</a>
<a id="11704" class="Keyword">open</a> <a id="11709" class="Keyword">import</a> <a id="11716" href="foundation.decidable-propositions.html" class="Module">foundation.decidable-propositions</a>
<a id="11750" class="Keyword">open</a> <a id="11755" class="Keyword">import</a> <a id="11762" href="foundation.decidable-subtypes.html" class="Module">foundation.decidable-subtypes</a>
<a id="11792" class="Keyword">open</a> <a id="11797" class="Keyword">import</a> <a id="11804" href="foundation.decidable-types.html" class="Module">foundation.decidable-types</a>
<a id="11831" class="Keyword">open</a> <a id="11836" class="Keyword">import</a> <a id="11843" href="foundation.dependent-pair-types.html" class="Module">foundation.dependent-pair-types</a>
<a id="11875" class="Keyword">open</a> <a id="11880" class="Keyword">import</a> <a id="11887" href="foundation.diagonal-maps-of-types.html" class="Module">foundation.diagonal-maps-of-types</a>
<a id="11921" class="Keyword">open</a> <a id="11926" class="Keyword">import</a> <a id="11933" href="foundation.disjunction.html" class="Module">foundation.disjunction</a>
<a id="11956" class="Keyword">open</a> <a id="11961" class="Keyword">import</a> <a id="11968" href="foundation.distributivity-of-dependent-functions-over-coproduct-types.html" class="Module">foundation.distributivity-of-dependent-functions-over-coproduct-types</a>
<a id="12038" class="Keyword">open</a> <a id="12043" class="Keyword">import</a> <a id="12050" href="foundation.distributivity-of-dependent-functions-over-dependent-pairs.html" class="Module">foundation.distributivity-of-dependent-functions-over-dependent-pairs</a>
<a id="12120" class="Keyword">open</a> <a id="12125" class="Keyword">import</a> <a id="12132" href="foundation.double-negation.html" class="Module">foundation.double-negation</a>
<a id="12159" class="Keyword">open</a> <a id="12164" class="Keyword">import</a> <a id="12171" href="foundation.double-powersets.html" class="Module">foundation.double-powersets</a>
<a id="12199" class="Keyword">open</a> <a id="12204" class="Keyword">import</a> <a id="12211" href="foundation.dubuc-penon-compact-types.html" class="Module">foundation.dubuc-penon-compact-types</a>
<a id="12248" class="Keyword">open</a> <a id="12253" class="Keyword">import</a> <a id="12260" href="foundation.effective-maps-equivalence-relations.html" class="Module">foundation.effective-maps-equivalence-relations</a>
<a id="12308" class="Keyword">open</a> <a id="12313" class="Keyword">import</a> <a id="12320" href="foundation.elementhood-relation-w-types.html" class="Module">foundation.elementhood-relation-w-types</a>
<a id="12360" class="Keyword">open</a> <a id="12365" class="Keyword">import</a> <a id="12372" href="foundation.embeddings.html" class="Module">foundation.embeddings</a>
<a id="12394" class="Keyword">open</a> <a id="12399" class="Keyword">import</a> <a id="12406" href="foundation.empty-types.html" class="Module">foundation.empty-types</a>
<a id="12429" class="Keyword">open</a> <a id="12434" class="Keyword">import</a> <a id="12441" href="foundation.epimorphisms-with-respect-to-sets.html" class="Module">foundation.epimorphisms-with-respect-to-sets</a>
<a id="12486" class="Keyword">open</a> <a id="12491" class="Keyword">import</a> <a id="12498" href="foundation.equality-cartesian-product-types.html" class="Module">foundation.equality-cartesian-product-types</a>
<a id="12542" class="Keyword">open</a> <a id="12547" class="Keyword">import</a> <a id="12554" href="foundation.equality-coproduct-types.html" class="Module">foundation.equality-coproduct-types</a>
<a id="12590" class="Keyword">open</a> <a id="12595" class="Keyword">import</a> <a id="12602" href="foundation.equality-dependent-function-types.html" class="Module">foundation.equality-dependent-function-types</a>
<a id="12647" class="Keyword">open</a> <a id="12652" class="Keyword">import</a> <a id="12659" href="foundation.equality-dependent-pair-types.html" class="Module">foundation.equality-dependent-pair-types</a>
<a id="12700" class="Keyword">open</a> <a id="12705" class="Keyword">import</a> <a id="12712" href="foundation.equality-fibers-of-maps.html" class="Module">foundation.equality-fibers-of-maps</a>
<a id="12747" class="Keyword">open</a> <a id="12752" class="Keyword">import</a> <a id="12759" href="foundation.equivalence-classes.html" class="Module">foundation.equivalence-classes</a>
<a id="12790" class="Keyword">open</a> <a id="12795" class="Keyword">import</a> <a id="12802" href="foundation.equivalence-induction.html" class="Module">foundation.equivalence-induction</a>
<a id="12835" class="Keyword">open</a> <a id="12840" class="Keyword">import</a> <a id="12847" href="foundation.equivalence-relations.html" class="Module">foundation.equivalence-relations</a>
<a id="12880" class="Keyword">open</a> <a id="12885" class="Keyword">import</a> <a id="12892" href="foundation.equivalences-maybe.html" class="Module">foundation.equivalences-maybe</a>
<a id="12922" class="Keyword">open</a> <a id="12927" class="Keyword">import</a> <a id="12934" href="foundation.equivalences.html" class="Module">foundation.equivalences</a>
<a id="12958" class="Keyword">open</a> <a id="12963" class="Keyword">import</a> <a id="12970" href="foundation.existential-quantification.html" class="Module">foundation.existential-quantification</a>
<a id="13008" class="Keyword">open</a> <a id="13013" class="Keyword">import</a> <a id="13020" href="foundation.extensional-w-types.html" class="Module">foundation.extensional-w-types</a>
<a id="13051" class="Keyword">open</a> <a id="13056" class="Keyword">import</a> <a id="13063" href="foundation.faithful-maps.html" class="Module">foundation.faithful-maps</a>
<a id="13088" class="Keyword">open</a> <a id="13093" class="Keyword">import</a> <a id="13100" href="foundation.fiber-inclusions.html" class="Module">foundation.fiber-inclusions</a>
<a id="13128" class="Keyword">open</a> <a id="13133" class="Keyword">import</a> <a id="13140" href="foundation.fibered-maps.html" class="Module">foundation.fibered-maps</a>
<a id="13164" class="Keyword">open</a> <a id="13169" class="Keyword">import</a> <a id="13176" href="foundation.fibers-of-maps.html" class="Module">foundation.fibers-of-maps</a>
<a id="13202" class="Keyword">open</a> <a id="13207" class="Keyword">import</a> <a id="13214" href="foundation.function-extensionality.html" class="Module">foundation.function-extensionality</a>
<a id="13249" class="Keyword">open</a> <a id="13254" class="Keyword">import</a> <a id="13261" href="foundation.functions.html" class="Module">foundation.functions</a>
<a id="13282" class="Keyword">open</a> <a id="13287" class="Keyword">import</a> <a id="13294" href="foundation.functoriality-cartesian-product-types.html" class="Module">foundation.functoriality-cartesian-product-types</a>
<a id="13343" class="Keyword">open</a> <a id="13348" class="Keyword">import</a> <a id="13355" href="foundation.functoriality-coproduct-types.html" class="Module">foundation.functoriality-coproduct-types</a>
<a id="13396" class="Keyword">open</a> <a id="13401" class="Keyword">import</a> <a id="13408" href="foundation.functoriality-dependent-function-types.html" class="Module">foundation.functoriality-dependent-function-types</a>
<a id="13458" class="Keyword">open</a> <a id="13463" class="Keyword">import</a> <a id="13470" href="foundation.functoriality-dependent-pair-types.html" class="Module">foundation.functoriality-dependent-pair-types</a>
<a id="13516" class="Keyword">open</a> <a id="13521" class="Keyword">import</a> <a id="13528" href="foundation.functoriality-function-types.html" class="Module">foundation.functoriality-function-types</a>
<a id="13568" class="Keyword">open</a> <a id="13573" class="Keyword">import</a> <a id="13580" href="foundation.functoriality-propositional-truncation.html" class="Module">foundation.functoriality-propositional-truncation</a>
<a id="13630" class="Keyword">open</a> <a id="13635" class="Keyword">import</a> <a id="13642" href="foundation.functoriality-set-quotients.html" class="Module">foundation.functoriality-set-quotients</a>
<a id="13681" class="Keyword">open</a> <a id="13686" class="Keyword">import</a> <a id="13693" href="foundation.functoriality-set-truncation.html" class="Module">foundation.functoriality-set-truncation</a>
<a id="13733" class="Keyword">open</a> <a id="13738" class="Keyword">import</a> <a id="13745" href="foundation.functoriality-w-types.html" class="Module">foundation.functoriality-w-types</a>
<a id="13778" class="Keyword">open</a> <a id="13783" class="Keyword">import</a> <a id="13790" href="foundation.fundamental-theorem-of-identity-types.html" class="Module">foundation.fundamental-theorem-of-identity-types</a>
<a id="13839" class="Keyword">open</a> <a id="13844" class="Keyword">import</a> <a id="13851" href="foundation.global-choice.html" class="Module">foundation.global-choice</a>
<a id="13876" class="Keyword">open</a> <a id="13881" class="Keyword">import</a> <a id="13888" href="foundation.hilberts-epsilon-operators.html" class="Module">foundation.hilberts-epsilon-operators</a>
<a id="13926" class="Keyword">open</a> <a id="13931" class="Keyword">import</a> <a id="13938" href="foundation.homotopies.html" class="Module">foundation.homotopies</a>
<a id="13960" class="Keyword">open</a> <a id="13965" class="Keyword">import</a> <a id="13972" href="foundation.identity-systems.html" class="Module">foundation.identity-systems</a>
<a id="14000" class="Keyword">open</a> <a id="14005" class="Keyword">import</a> <a id="14012" href="foundation.identity-types.html" class="Module">foundation.identity-types</a>
<a id="14038" class="Keyword">open</a> <a id="14043" class="Keyword">import</a> <a id="14050" href="foundation.images.html" class="Module">foundation.images</a>
<a id="14068" class="Keyword">open</a> <a id="14073" class="Keyword">import</a> <a id="14080" href="foundation.impredicative-encodings.html" class="Module">foundation.impredicative-encodings</a>
<a id="14115" class="Keyword">open</a> <a id="14120" class="Keyword">import</a> <a id="14127" href="foundation.indexed-w-types.html" class="Module">foundation.indexed-w-types</a>
<a id="14154" class="Keyword">open</a> <a id="14159" class="Keyword">import</a> <a id="14166" href="foundation.induction-principle-propositional-truncation.html" class="Module">foundation.induction-principle-propositional-truncation</a>
<a id="14222" class="Keyword">open</a> <a id="14227" class="Keyword">import</a> <a id="14234" href="foundation.induction-w-types.html" class="Module">foundation.induction-w-types</a>
<a id="14263" class="Keyword">open</a> <a id="14268" class="Keyword">import</a> <a id="14275" href="foundation.inequality-w-types.html" class="Module">foundation.inequality-w-types</a>
<a id="14305" class="Keyword">open</a> <a id="14310" class="Keyword">import</a> <a id="14317" href="foundation.injective-maps.html" class="Module">foundation.injective-maps</a>
<a id="14343" class="Keyword">open</a> <a id="14348" class="Keyword">import</a> <a id="14355" href="foundation.interchange-law.html" class="Module">foundation.interchange-law</a>
<a id="14382" class="Keyword">open</a> <a id="14387" class="Keyword">import</a> <a id="14394" href="foundation.intersection.html" class="Module">foundation.intersection</a>
<a id="14418" class="Keyword">open</a> <a id="14423" class="Keyword">import</a> <a id="14430" href="foundation.involutions.html" class="Module">foundation.involutions</a>
<a id="14453" class="Keyword">open</a> <a id="14458" class="Keyword">import</a> <a id="14465" href="foundation.isolated-points.html" class="Module">foundation.isolated-points</a>
<a id="14492" class="Keyword">open</a> <a id="14497" class="Keyword">import</a> <a id="14504" href="foundation.isomorphisms-of-sets.html" class="Module">foundation.isomorphisms-of-sets</a>
<a id="14536" class="Keyword">open</a> <a id="14541" class="Keyword">import</a> <a id="14548" href="foundation.law-of-excluded-middle.html" class="Module">foundation.law-of-excluded-middle</a>
<a id="14582" class="Keyword">open</a> <a id="14587" class="Keyword">import</a> <a id="14594" href="foundation.lawveres-fixed-point-theorem.html" class="Module">foundation.lawveres-fixed-point-theorem</a>
<a id="14634" class="Keyword">open</a> <a id="14639" class="Keyword">import</a> <a id="14646" href="foundation.locally-small-types.html" class="Module">foundation.locally-small-types</a>
<a id="14677" class="Keyword">open</a> <a id="14682" class="Keyword">import</a> <a id="14689" href="foundation.logical-equivalences.html" class="Module">foundation.logical-equivalences</a>
<a id="14721" class="Keyword">open</a> <a id="14726" class="Keyword">import</a> <a id="14733" href="foundation.lower-types-w-types.html" class="Module">foundation.lower-types-w-types</a>
<a id="14764" class="Keyword">open</a> <a id="14769" class="Keyword">import</a> <a id="14776" href="foundation.maybe.html" class="Module">foundation.maybe</a>
<a id="14793" class="Keyword">open</a> <a id="14798" class="Keyword">import</a> <a id="14805" href="foundation.mere-equality.html" class="Module">foundation.mere-equality</a>
<a id="14830" class="Keyword">open</a> <a id="14835" class="Keyword">import</a> <a id="14842" href="foundation.mere-equivalences.html" class="Module">foundation.mere-equivalences</a>
<a id="14871" class="Keyword">open</a> <a id="14876" class="Keyword">import</a> <a id="14883" href="foundation.monomorphisms.html" class="Module">foundation.monomorphisms</a>
<a id="14908" class="Keyword">open</a> <a id="14913" class="Keyword">import</a> <a id="14920" href="foundation.multisets.html" class="Module">foundation.multisets</a>
<a id="14941" class="Keyword">open</a> <a id="14946" class="Keyword">import</a> <a id="14953" href="foundation.negation.html" class="Module">foundation.negation</a>
<a id="14973" class="Keyword">open</a> <a id="14978" class="Keyword">import</a> <a id="14985" href="foundation.non-contractible-types.html" class="Module">foundation.non-contractible-types</a>
<a id="15019" class="Keyword">open</a> <a id="15024" class="Keyword">import</a> <a id="15031" href="foundation.pairs-of-distinct-elements.html" class="Module">foundation.pairs-of-distinct-elements</a>
<a id="15069" class="Keyword">open</a> <a id="15074" class="Keyword">import</a> <a id="15081" href="foundation.path-algebra.html" class="Module">foundation.path-algebra</a>
<a id="15105" class="Keyword">open</a> <a id="15110" class="Keyword">import</a> <a id="15117" href="foundation.path-split-maps.html" class="Module">foundation.path-split-maps</a>
<a id="15144" class="Keyword">open</a> <a id="15149" class="Keyword">import</a> <a id="15156" href="foundation.polynomial-endofunctors.html" class="Module">foundation.polynomial-endofunctors</a>
<a id="15191" class="Keyword">open</a> <a id="15196" class="Keyword">import</a> <a id="15203" href="foundation.powersets.html" class="Module">foundation.powersets</a>
<a id="15224" class="Keyword">open</a> <a id="15229" class="Keyword">import</a> <a id="15236" href="foundation.principle-of-omniscience.html" class="Module">foundation.principle-of-omniscience</a>
<a id="15272" class="Keyword">open</a> <a id="15277" class="Keyword">import</a> <a id="15284" href="foundation.propositional-extensionality.html" class="Module">foundation.propositional-extensionality</a>
<a id="15324" class="Keyword">open</a> <a id="15329" class="Keyword">import</a> <a id="15336" href="foundation.propositional-maps.html" class="Module">foundation.propositional-maps</a>
<a id="15366" class="Keyword">open</a> <a id="15371" class="Keyword">import</a> <a id="15378" href="foundation.propositional-truncations.html" class="Module">foundation.propositional-truncations</a>
<a id="15415" class="Keyword">open</a> <a id="15420" class="Keyword">import</a> <a id="15427" href="foundation.propositions.html" class="Module">foundation.propositions</a>
<a id="15451" class="Keyword">open</a> <a id="15456" class="Keyword">import</a> <a id="15463" href="foundation.pullbacks.html" class="Module">foundation.pullbacks</a>
<a id="15484" class="Keyword">open</a> <a id="15489" class="Keyword">import</a> <a id="15496" href="foundation.raising-universe-levels.html" class="Module">foundation.raising-universe-levels</a>
<a id="15531" class="Keyword">open</a> <a id="15536" class="Keyword">import</a> <a id="15543" href="foundation.ranks-of-elements-w-types.html" class="Module">foundation.ranks-of-elements-w-types</a>
<a id="15580" class="Keyword">open</a> <a id="15585" class="Keyword">import</a> <a id="15592" href="foundation.reflecting-maps-equivalence-relations.html" class="Module">foundation.reflecting-maps-equivalence-relations</a>
<a id="15641" class="Keyword">open</a> <a id="15646" class="Keyword">import</a> <a id="15653" href="foundation.replacement.html" class="Module">foundation.replacement</a>
<a id="15676" class="Keyword">open</a> <a id="15681" class="Keyword">import</a> <a id="15688" href="foundation.retractions.html" class="Module">foundation.retractions</a>
<a id="15711" class="Keyword">open</a> <a id="15716" class="Keyword">import</a> <a id="15723" href="foundation.russells-paradox.html" class="Module">foundation.russells-paradox</a>
<a id="15751" class="Keyword">open</a> <a id="15756" class="Keyword">import</a> <a id="15763" href="foundation.sections.html" class="Module">foundation.sections</a>
<a id="15783" class="Keyword">open</a> <a id="15788" class="Keyword">import</a> <a id="15795" href="foundation.set-presented-types.html" class="Module">foundation.set-presented-types</a>
<a id="15826" class="Keyword">open</a> <a id="15831" class="Keyword">import</a> <a id="15838" href="foundation.set-truncations.html" class="Module">foundation.set-truncations</a>
<a id="15865" class="Keyword">open</a> <a id="15870" class="Keyword">import</a> <a id="15877" href="foundation.sets.html" class="Module">foundation.sets</a>
<a id="15893" class="Keyword">open</a> <a id="15898" class="Keyword">import</a> <a id="15905" href="foundation.singleton-induction.html" class="Module">foundation.singleton-induction</a>
<a id="15936" class="Keyword">open</a> <a id="15941" class="Keyword">import</a> <a id="15948" href="foundation.slice.html" class="Module">foundation.slice</a>
<a id="15965" class="Keyword">open</a> <a id="15970" class="Keyword">import</a> <a id="15977" href="foundation.small-maps.html" class="Module">foundation.small-maps</a>
<a id="15999" class="Keyword">open</a> <a id="16004" class="Keyword">import</a> <a id="16011" href="foundation.small-multisets.html" class="Module">foundation.small-multisets</a>
<a id="16038" class="Keyword">open</a> <a id="16043" class="Keyword">import</a> <a id="16050" href="foundation.small-types.html" class="Module">foundation.small-types</a>
<a id="16073" class="Keyword">open</a> <a id="16078" class="Keyword">import</a> <a id="16085" href="foundation.small-universes.html" class="Module">foundation.small-universes</a>
<a id="16112" class="Keyword">open</a> <a id="16117" class="Keyword">import</a> <a id="16124" href="foundation.split-surjective-maps.html" class="Module">foundation.split-surjective-maps</a>
<a id="16157" class="Keyword">open</a> <a id="16162" class="Keyword">import</a> <a id="16169" href="foundation.structure-identity-principle.html" class="Module">foundation.structure-identity-principle</a>
<a id="16209" class="Keyword">open</a> <a id="16214" class="Keyword">import</a> <a id="16221" href="foundation.structure.html" class="Module">foundation.structure</a>
<a id="16242" class="Keyword">open</a> <a id="16247" class="Keyword">import</a> <a id="16254" href="foundation.subterminal-types.html" class="Module">foundation.subterminal-types</a>
<a id="16283" class="Keyword">open</a> <a id="16288" class="Keyword">import</a> <a id="16295" href="foundation.subtype-identity-principle.html" class="Module">foundation.subtype-identity-principle</a>
<a id="16333" class="Keyword">open</a> <a id="16338" class="Keyword">import</a> <a id="16345" href="foundation.subtypes.html" class="Module">foundation.subtypes</a>
<a id="16365" class="Keyword">open</a> <a id="16370" class="Keyword">import</a> <a id="16377" href="foundation.subuniverses.html" class="Module">foundation.subuniverses</a>
<a id="16401" class="Keyword">open</a> <a id="16406" class="Keyword">import</a> <a id="16413" href="foundation.surjective-maps.html" class="Module">foundation.surjective-maps</a>
<a id="16440" class="Keyword">open</a> <a id="16445" class="Keyword">import</a> <a id="16452" href="foundation.symmetric-difference.html" class="Module">foundation.symmetric-difference</a>
<a id="16484" class="Keyword">open</a> <a id="16489" class="Keyword">import</a> <a id="16496" href="foundation.truncated-equality.html" class="Module">foundation.truncated-equality</a>
<a id="16526" class="Keyword">open</a> <a id="16531" class="Keyword">import</a> <a id="16538" href="foundation.truncated-maps.html" class="Module">foundation.truncated-maps</a>
<a id="16564" class="Keyword">open</a> <a id="16569" class="Keyword">import</a> <a id="16576" href="foundation.truncated-types.html" class="Module">foundation.truncated-types</a>
<a id="16603" class="Keyword">open</a> <a id="16608" class="Keyword">import</a> <a id="16615" href="foundation.truncation-levels.html" class="Module">foundation.truncation-levels</a>
<a id="16644" class="Keyword">open</a> <a id="16649" class="Keyword">import</a> <a id="16656" href="foundation.truncations.html" class="Module">foundation.truncations</a>
<a id="16679" class="Keyword">open</a> <a id="16684" class="Keyword">import</a> <a id="16691" href="foundation.type-arithmetic-cartesian-product-types.html" class="Module">foundation.type-arithmetic-cartesian-product-types</a>
<a id="16742" class="Keyword">open</a> <a id="16747" class="Keyword">import</a> <a id="16754" href="foundation.type-arithmetic-coproduct-types.html" class="Module">foundation.type-arithmetic-coproduct-types</a>
<a id="16797" class="Keyword">open</a> <a id="16802" class="Keyword">import</a> <a id="16809" href="foundation.type-arithmetic-dependent-pair-types.html" class="Module">foundation.type-arithmetic-dependent-pair-types</a>
<a id="16857" class="Keyword">open</a> <a id="16862" class="Keyword">import</a> <a id="16869" href="foundation.type-arithmetic-empty-type.html" class="Module">foundation.type-arithmetic-empty-type</a>
<a id="16907" class="Keyword">open</a> <a id="16912" class="Keyword">import</a> <a id="16919" href="foundation.type-arithmetic-unit-type.html" class="Module">foundation.type-arithmetic-unit-type</a>
<a id="16956" class="Keyword">open</a> <a id="16961" class="Keyword">import</a> <a id="16968" href="foundation.uniqueness-image.html" class="Module">foundation.uniqueness-image</a>
<a id="16996" class="Keyword">open</a> <a id="17001" class="Keyword">import</a> <a id="17008" href="foundation.uniqueness-set-quotients.html" class="Module">foundation.uniqueness-set-quotients</a>
<a id="17044" class="Keyword">open</a> <a id="17049" class="Keyword">import</a> <a id="17056" href="foundation.uniqueness-set-truncations.html" class="Module">foundation.uniqueness-set-truncations</a>
<a id="17094" class="Keyword">open</a> <a id="17099" class="Keyword">import</a> <a id="17106" href="foundation.uniqueness-truncation.html" class="Module">foundation.uniqueness-truncation</a>
<a id="17139" class="Keyword">open</a> <a id="17144" class="Keyword">import</a> <a id="17151" href="foundation.unit-type.html" class="Module">foundation.unit-type</a>
<a id="17172" class="Keyword">open</a> <a id="17177" class="Keyword">import</a> <a id="17184" href="foundation.univalence-implies-function-extensionality.html" class="Module">foundation.univalence-implies-function-extensionality</a>
<a id="17238" class="Keyword">open</a> <a id="17243" class="Keyword">import</a> <a id="17250" href="foundation.univalence.html" class="Module">foundation.univalence</a>
<a id="17272" class="Keyword">open</a> <a id="17277" class="Keyword">import</a> <a id="17284" href="foundation.univalent-type-families.html" class="Module">foundation.univalent-type-families</a>
<a id="17319" class="Keyword">open</a> <a id="17324" class="Keyword">import</a> <a id="17331" href="foundation.universal-multiset.html" class="Module">foundation.universal-multiset</a>
<a id="17361" class="Keyword">open</a> <a id="17366" class="Keyword">import</a> <a id="17373" href="foundation.universal-property-booleans.html" class="Module">foundation.universal-property-booleans</a>
<a id="17412" class="Keyword">open</a> <a id="17417" class="Keyword">import</a> <a id="17424" href="foundation.universal-property-cartesian-product-types.html" class="Module">foundation.universal-property-cartesian-product-types</a>
<a id="17478" class="Keyword">open</a> <a id="17483" class="Keyword">import</a> <a id="17490" href="foundation.universal-property-coproduct-types.html" class="Module">foundation.universal-property-coproduct-types</a>
<a id="17536" class="Keyword">open</a> <a id="17541" class="Keyword">import</a> <a id="17548" href="foundation.universal-property-dependent-pair-types.html" class="Module">foundation.universal-property-dependent-pair-types</a>
<a id="17599" class="Keyword">open</a> <a id="17604" class="Keyword">import</a> <a id="17611" href="foundation.universal-property-empty-type.html" class="Module">foundation.universal-property-empty-type</a>
<a id="17652" class="Keyword">open</a> <a id="17657" class="Keyword">import</a> <a id="17664" href="foundation.universal-property-fiber-products.html" class="Module">foundation.universal-property-fiber-products</a>
<a id="17709" class="Keyword">open</a> <a id="17714" class="Keyword">import</a> <a id="17721" href="foundation.universal-property-identity-types.html" class="Module">foundation.universal-property-identity-types</a>
<a id="17766" class="Keyword">open</a> <a id="17771" class="Keyword">import</a> <a id="17778" href="foundation.universal-property-image.html" class="Module">foundation.universal-property-image</a>
<a id="17814" class="Keyword">open</a> <a id="17819" class="Keyword">import</a> <a id="17826" href="foundation.universal-property-maybe.html" class="Module">foundation.universal-property-maybe</a>
<a id="17862" class="Keyword">open</a> <a id="17867" class="Keyword">import</a> <a id="17874" href="foundation.universal-property-propositional-truncation-into-sets.html" class="Module">foundation.universal-property-propositional-truncation-into-sets</a>
<a id="17939" class="Keyword">open</a> <a id="17944" class="Keyword">import</a> <a id="17951" href="foundation.universal-property-propositional-truncation.html" class="Module">foundation.universal-property-propositional-truncation</a>
<a id="18006" class="Keyword">open</a> <a id="18011" class="Keyword">import</a> <a id="18018" href="foundation.universal-property-pullbacks.html" class="Module">foundation.universal-property-pullbacks</a>
<a id="18058" class="Keyword">open</a> <a id="18063" class="Keyword">import</a> <a id="18070" href="foundation.universal-property-set-quotients.html" class="Module">foundation.universal-property-set-quotients</a>
<a id="18114" class="Keyword">open</a> <a id="18119" class="Keyword">import</a> <a id="18126" href="foundation.universal-property-set-truncation.html" class="Module">foundation.universal-property-set-truncation</a>
<a id="18171" class="Keyword">open</a> <a id="18176" class="Keyword">import</a> <a id="18183" href="foundation.universal-property-truncation.html" class="Module">foundation.universal-property-truncation</a>
<a id="18224" class="Keyword">open</a> <a id="18229" class="Keyword">import</a> <a id="18236" href="foundation.universal-property-unit-type.html" class="Module">foundation.universal-property-unit-type</a>
<a id="18276" class="Keyword">open</a> <a id="18281" class="Keyword">import</a> <a id="18288" href="foundation.universe-levels.html" class="Module">foundation.universe-levels</a>
<a id="18315" class="Keyword">open</a> <a id="18320" class="Keyword">import</a> <a id="18327" href="foundation.unordered-pairs.html" class="Module">foundation.unordered-pairs</a>
<a id="18354" class="Keyword">open</a> <a id="18359" class="Keyword">import</a> <a id="18366" href="foundation.w-types.html" class="Module">foundation.w-types</a>
<a id="18385" class="Keyword">open</a> <a id="18390" class="Keyword">import</a> <a id="18397" href="foundation.weak-function-extensionality.html" class="Module">foundation.weak-function-extensionality</a>
<a id="18437" class="Keyword">open</a> <a id="18442" class="Keyword">import</a> <a id="18449" href="foundation.weakly-constant-maps.html" class="Module">foundation.weakly-constant-maps</a>
<a id="18481" class="Keyword">open</a> <a id="18486" class="Keyword">import</a> <a id="18493" href="foundation.xor.html" class="Module">foundation.xor</a>
</pre>
## Foundation Core

<pre class="Agda"><a id="18541" class="Keyword">open</a> <a id="18546" class="Keyword">import</a> <a id="18553" href="foundation-core.0-maps.html" class="Module">foundation-core.0-maps</a>
<a id="18576" class="Keyword">open</a> <a id="18581" class="Keyword">import</a> <a id="18588" href="foundation-core.1-types.html" class="Module">foundation-core.1-types</a>
<a id="18612" class="Keyword">open</a> <a id="18617" class="Keyword">import</a> <a id="18624" href="foundation-core.cartesian-product-types.html" class="Module">foundation-core.cartesian-product-types</a>
<a id="18664" class="Keyword">open</a> <a id="18669" class="Keyword">import</a> <a id="18676" href="foundation-core.coherently-invertible-maps.html" class="Module">foundation-core.coherently-invertible-maps</a>
<a id="18719" class="Keyword">open</a> <a id="18724" class="Keyword">import</a> <a id="18731" href="foundation-core.commuting-squares.html" class="Module">foundation-core.commuting-squares</a>
<a id="18765" class="Keyword">open</a> <a id="18770" class="Keyword">import</a> <a id="18777" href="foundation-core.constant-maps.html" class="Module">foundation-core.constant-maps</a>
<a id="18807" class="Keyword">open</a> <a id="18812" class="Keyword">import</a> <a id="18819" href="foundation-core.contractible-maps.html" class="Module">foundation-core.contractible-maps</a>
<a id="18853" class="Keyword">open</a> <a id="18858" class="Keyword">import</a> <a id="18865" href="foundation-core.contractible-types.html" class="Module">foundation-core.contractible-types</a>
<a id="18900" class="Keyword">open</a> <a id="18905" class="Keyword">import</a> <a id="18912" href="foundation-core.dependent-pair-types.html" class="Module">foundation-core.dependent-pair-types</a>
<a id="18949" class="Keyword">open</a> <a id="18954" class="Keyword">import</a> <a id="18961" href="foundation-core.embeddings.html" class="Module">foundation-core.embeddings</a>
<a id="18988" class="Keyword">open</a> <a id="18993" class="Keyword">import</a> <a id="19000" href="foundation-core.empty-types.html" class="Module">foundation-core.empty-types</a>
<a id="19028" class="Keyword">open</a> <a id="19033" class="Keyword">import</a> <a id="19040" href="foundation-core.equality-cartesian-product-types.html" class="Module">foundation-core.equality-cartesian-product-types</a>
<a id="19089" class="Keyword">open</a> <a id="19094" class="Keyword">import</a> <a id="19101" href="foundation-core.equality-dependent-pair-types.html" class="Module">foundation-core.equality-dependent-pair-types</a>
<a id="19147" class="Keyword">open</a> <a id="19152" class="Keyword">import</a> <a id="19159" href="foundation-core.equality-fibers-of-maps.html" class="Module">foundation-core.equality-fibers-of-maps</a>
<a id="19199" class="Keyword">open</a> <a id="19204" class="Keyword">import</a> <a id="19211" href="foundation-core.equivalence-induction.html" class="Module">foundation-core.equivalence-induction</a>
<a id="19249" class="Keyword">open</a> <a id="19254" class="Keyword">import</a> <a id="19261" href="foundation-core.equivalences.html" class="Module">foundation-core.equivalences</a>
<a id="19290" class="Keyword">open</a> <a id="19295" class="Keyword">import</a> <a id="19302" href="foundation-core.faithful-maps.html" class="Module">foundation-core.faithful-maps</a>
<a id="19332" class="Keyword">open</a> <a id="19337" class="Keyword">import</a> <a id="19344" href="foundation-core.fibers-of-maps.html" class="Module">foundation-core.fibers-of-maps</a>
<a id="19375" class="Keyword">open</a> <a id="19380" class="Keyword">import</a> <a id="19387" href="foundation-core.functions.html" class="Module">foundation-core.functions</a>
<a id="19413" class="Keyword">open</a> <a id="19418" class="Keyword">import</a> <a id="19425" href="foundation-core.functoriality-dependent-pair-types.html" class="Module">foundation-core.functoriality-dependent-pair-types</a>
<a id="19476" class="Keyword">open</a> <a id="19481" class="Keyword">import</a> <a id="19488" href="foundation-core.fundamental-theorem-of-identity-types.html" class="Module">foundation-core.fundamental-theorem-of-identity-types</a>
<a id="19542" class="Keyword">open</a> <a id="19547" class="Keyword">import</a> <a id="19554" href="foundation-core.homotopies.html" class="Module">foundation-core.homotopies</a>
<a id="19581" class="Keyword">open</a> <a id="19586" class="Keyword">import</a> <a id="19593" href="foundation-core.identity-systems.html" class="Module">foundation-core.identity-systems</a>
<a id="19626" class="Keyword">open</a> <a id="19631" class="Keyword">import</a> <a id="19638" href="foundation-core.identity-types.html" class="Module">foundation-core.identity-types</a>
<a id="19669" class="Keyword">open</a> <a id="19674" class="Keyword">import</a> <a id="19681" href="foundation-core.logical-equivalences.html" class="Module">foundation-core.logical-equivalences</a>
<a id="19718" class="Keyword">open</a> <a id="19723" class="Keyword">import</a> <a id="19730" href="foundation-core.negation.html" class="Module">foundation-core.negation</a>
<a id="19755" class="Keyword">open</a> <a id="19760" class="Keyword">import</a> <a id="19767" href="foundation-core.path-split-maps.html" class="Module">foundation-core.path-split-maps</a>
<a id="19799" class="Keyword">open</a> <a id="19804" class="Keyword">import</a> <a id="19811" href="foundation-core.propositional-maps.html" class="Module">foundation-core.propositional-maps</a>
<a id="19846" class="Keyword">open</a> <a id="19851" class="Keyword">import</a> <a id="19858" href="foundation-core.propositions.html" class="Module">foundation-core.propositions</a>
<a id="19887" class="Keyword">open</a> <a id="19892" class="Keyword">import</a> <a id="19899" href="foundation-core.retractions.html" class="Module">foundation-core.retractions</a>
<a id="19927" class="Keyword">open</a> <a id="19932" class="Keyword">import</a> <a id="19939" href="foundation-core.sections.html" class="Module">foundation-core.sections</a>
<a id="19964" class="Keyword">open</a> <a id="19969" class="Keyword">import</a> <a id="19976" href="foundation-core.sets.html" class="Module">foundation-core.sets</a>
<a id="19997" class="Keyword">open</a> <a id="20002" class="Keyword">import</a> <a id="20009" href="foundation-core.singleton-induction.html" class="Module">foundation-core.singleton-induction</a>
<a id="20045" class="Keyword">open</a> <a id="20050" class="Keyword">import</a> <a id="20057" href="foundation-core.subtype-identity-principle.html" class="Module">foundation-core.subtype-identity-principle</a>
<a id="20100" class="Keyword">open</a> <a id="20105" class="Keyword">import</a> <a id="20112" href="foundation-core.subtypes.html" class="Module">foundation-core.subtypes</a>
<a id="20137" class="Keyword">open</a> <a id="20142" class="Keyword">import</a> <a id="20149" href="foundation-core.truncated-maps.html" class="Module">foundation-core.truncated-maps</a>
<a id="20180" class="Keyword">open</a> <a id="20185" class="Keyword">import</a> <a id="20192" href="foundation-core.truncated-types.html" class="Module">foundation-core.truncated-types</a>
<a id="20224" class="Keyword">open</a> <a id="20229" class="Keyword">import</a> <a id="20236" href="foundation-core.truncation-levels.html" class="Module">foundation-core.truncation-levels</a>
<a id="20270" class="Keyword">open</a> <a id="20275" class="Keyword">import</a> <a id="20282" href="foundation-core.type-arithmetic-cartesian-product-types.html" class="Module">foundation-core.type-arithmetic-cartesian-product-types</a>
<a id="20338" class="Keyword">open</a> <a id="20343" class="Keyword">import</a> <a id="20350" href="foundation-core.type-arithmetic-dependent-pair-types.html" class="Module">foundation-core.type-arithmetic-dependent-pair-types</a>
<a id="20403" class="Keyword">open</a> <a id="20408" class="Keyword">import</a> <a id="20415" href="foundation-core.univalence.html" class="Module">foundation-core.univalence</a>
<a id="20442" class="Keyword">open</a> <a id="20447" class="Keyword">import</a> <a id="20454" href="foundation-core.universe-levels.html" class="Module">foundation-core.universe-levels</a>
</pre>
## Graph theory

<pre class="Agda"><a id="20516" class="Keyword">open</a> <a id="20521" class="Keyword">import</a> <a id="20528" href="graph-theory.html" class="Module">graph-theory</a>
<a id="20541" class="Keyword">open</a> <a id="20546" class="Keyword">import</a> <a id="20553" href="graph-theory.connected-undirected-graphs.html" class="Module">graph-theory.connected-undirected-graphs</a>
<a id="20594" class="Keyword">open</a> <a id="20599" class="Keyword">import</a> <a id="20606" href="graph-theory.directed-graphs.html" class="Module">graph-theory.directed-graphs</a>
<a id="20635" class="Keyword">open</a> <a id="20640" class="Keyword">import</a> <a id="20647" href="graph-theory.edge-coloured-undirected-graphs.html" class="Module">graph-theory.edge-coloured-undirected-graphs</a>
<a id="20692" class="Keyword">open</a> <a id="20697" class="Keyword">import</a> <a id="20704" href="graph-theory.equivalences-undirected-graphs.html" class="Module">graph-theory.equivalences-undirected-graphs</a>
<a id="20748" class="Keyword">open</a> <a id="20753" class="Keyword">import</a> <a id="20760" href="graph-theory.finite-graphs.html" class="Module">graph-theory.finite-graphs</a>
<a id="20787" class="Keyword">open</a> <a id="20792" class="Keyword">import</a> <a id="20799" href="graph-theory.incidence-undirected-graphs.html" class="Module">graph-theory.incidence-undirected-graphs</a>
<a id="20840" class="Keyword">open</a> <a id="20845" class="Keyword">import</a> <a id="20852" href="graph-theory.matchings.html" class="Module">graph-theory.matchings</a>
<a id="20875" class="Keyword">open</a> <a id="20880" class="Keyword">import</a> <a id="20887" href="graph-theory.mere-equivalences-undirected-graphs.html" class="Module">graph-theory.mere-equivalences-undirected-graphs</a>
<a id="20936" class="Keyword">open</a> <a id="20941" class="Keyword">import</a> <a id="20948" href="graph-theory.morphisms-directed-graphs.html" class="Module">graph-theory.morphisms-directed-graphs</a>
<a id="20987" class="Keyword">open</a> <a id="20992" class="Keyword">import</a> <a id="20999" href="graph-theory.morphisms-undirected-graphs.html" class="Module">graph-theory.morphisms-undirected-graphs</a>
<a id="21040" class="Keyword">open</a> <a id="21045" class="Keyword">import</a> <a id="21052" href="graph-theory.orientations-undirected-graphs.html" class="Module">graph-theory.orientations-undirected-graphs</a>
<a id="21096" class="Keyword">open</a> <a id="21101" class="Keyword">import</a> <a id="21108" href="graph-theory.paths-undirected-graphs.html" class="Module">graph-theory.paths-undirected-graphs</a>
<a id="21145" class="Keyword">open</a> <a id="21150" class="Keyword">import</a> <a id="21157" href="graph-theory.polygons.html" class="Module">graph-theory.polygons</a>
<a id="21179" class="Keyword">open</a> <a id="21184" class="Keyword">import</a> <a id="21191" href="graph-theory.reflexive-graphs.html" class="Module">graph-theory.reflexive-graphs</a>
<a id="21221" class="Keyword">open</a> <a id="21226" class="Keyword">import</a> <a id="21233" href="graph-theory.regular-undirected-graphs.html" class="Module">graph-theory.regular-undirected-graphs</a>
<a id="21272" class="Keyword">open</a> <a id="21277" class="Keyword">import</a> <a id="21284" href="graph-theory.simple-undirected-graphs.html" class="Module">graph-theory.simple-undirected-graphs</a>
<a id="21322" class="Keyword">open</a> <a id="21327" class="Keyword">import</a> <a id="21334" href="graph-theory.undirected-graphs.html" class="Module">graph-theory.undirected-graphs</a>
<a id="21365" class="Keyword">open</a> <a id="21370" class="Keyword">import</a> <a id="21377" href="graph-theory.voltage-graphs.html" class="Module">graph-theory.voltage-graphs</a>
</pre>
## Group theory

<pre class="Agda"><a id="21435" class="Keyword">open</a> <a id="21440" class="Keyword">import</a> <a id="21447" href="group-theory.html" class="Module">group-theory</a>
<a id="21460" class="Keyword">open</a> <a id="21465" class="Keyword">import</a> <a id="21472" href="group-theory.abelian-groups.html" class="Module">group-theory.abelian-groups</a>
<a id="21500" class="Keyword">open</a> <a id="21505" class="Keyword">import</a> <a id="21512" href="group-theory.abelian-subgroups.html" class="Module">group-theory.abelian-subgroups</a>
<a id="21543" class="Keyword">open</a> <a id="21548" class="Keyword">import</a> <a id="21555" href="group-theory.abstract-group-torsors.html" class="Module">group-theory.abstract-group-torsors</a>
<a id="21591" class="Keyword">open</a> <a id="21596" class="Keyword">import</a> <a id="21603" href="group-theory.addition-homomorphisms-abelian-groups.html" class="Module">group-theory.addition-homomorphisms-abelian-groups</a>
<a id="21654" class="Keyword">open</a> <a id="21659" class="Keyword">import</a> <a id="21666" href="group-theory.automorphism-groups.html" class="Module">group-theory.automorphism-groups</a>
<a id="21699" class="Keyword">open</a> <a id="21704" class="Keyword">import</a> <a id="21711" href="group-theory.category-of-groups.html" class="Module">group-theory.category-of-groups</a>
<a id="21743" class="Keyword">open</a> <a id="21748" class="Keyword">import</a> <a id="21755" href="group-theory.category-of-semigroups.html" class="Module">group-theory.category-of-semigroups</a>
<a id="21791" class="Keyword">open</a> <a id="21796" class="Keyword">import</a> <a id="21803" href="group-theory.cayleys-theorem.html" class="Module">group-theory.cayleys-theorem</a>
<a id="21832" class="Keyword">open</a> <a id="21837" class="Keyword">import</a> <a id="21844" href="group-theory.concrete-group-actions.html" class="Module">group-theory.concrete-group-actions</a>
<a id="21880" class="Keyword">open</a> <a id="21885" class="Keyword">import</a> <a id="21892" href="group-theory.concrete-groups.html" class="Module">group-theory.concrete-groups</a>
<a id="21921" class="Keyword">open</a> <a id="21926" class="Keyword">import</a> <a id="21933" href="group-theory.concrete-subgroups.html" class="Module">group-theory.concrete-subgroups</a>
<a id="21965" class="Keyword">open</a> <a id="21970" class="Keyword">import</a> <a id="21977" href="group-theory.conjugation.html" class="Module">group-theory.conjugation</a>
<a id="22002" class="Keyword">open</a> <a id="22007" class="Keyword">import</a> <a id="22014" href="group-theory.embeddings-groups.html" class="Module">group-theory.embeddings-groups</a>
<a id="22045" class="Keyword">open</a> <a id="22050" class="Keyword">import</a> <a id="22057" href="group-theory.endomorphism-rings-abelian-groups.html" class="Module">group-theory.endomorphism-rings-abelian-groups</a>
<a id="22104" class="Keyword">open</a> <a id="22109" class="Keyword">import</a> <a id="22116" href="group-theory.equivalences-group-actions.html" class="Module">group-theory.equivalences-group-actions</a>
<a id="22156" class="Keyword">open</a> <a id="22161" class="Keyword">import</a> <a id="22168" href="group-theory.equivalences-semigroups.html" class="Module">group-theory.equivalences-semigroups</a>
<a id="22205" class="Keyword">open</a> <a id="22210" class="Keyword">import</a> <a id="22217" href="group-theory.examples-higher-groups.html" class="Module">group-theory.examples-higher-groups</a>
<a id="22253" class="Keyword">open</a> <a id="22258" class="Keyword">import</a> <a id="22265" href="group-theory.furstenberg-groups.html" class="Module">group-theory.furstenberg-groups</a>
<a id="22297" class="Keyword">open</a> <a id="22302" class="Keyword">import</a> <a id="22309" href="group-theory.group-actions.html" class="Module">group-theory.group-actions</a>
<a id="22336" class="Keyword">open</a> <a id="22341" class="Keyword">import</a> <a id="22348" href="group-theory.groups.html" class="Module">group-theory.groups</a>
<a id="22368" class="Keyword">open</a> <a id="22373" class="Keyword">import</a> <a id="22380" href="group-theory.higher-groups.html" class="Module">group-theory.higher-groups</a>
<a id="22407" class="Keyword">open</a> <a id="22412" class="Keyword">import</a> <a id="22419" href="group-theory.homomorphisms-abelian-groups.html" class="Module">group-theory.homomorphisms-abelian-groups</a>
<a id="22461" class="Keyword">open</a> <a id="22466" class="Keyword">import</a> <a id="22473" href="group-theory.homomorphisms-group-actions.html" class="Module">group-theory.homomorphisms-group-actions</a>
<a id="22514" class="Keyword">open</a> <a id="22519" class="Keyword">import</a> <a id="22526" href="group-theory.homomorphisms-groups.html" class="Module">group-theory.homomorphisms-groups</a>
<a id="22560" class="Keyword">open</a> <a id="22565" class="Keyword">import</a> <a id="22572" href="group-theory.homomorphisms-monoids.html" class="Module">group-theory.homomorphisms-monoids</a>
<a id="22607" class="Keyword">open</a> <a id="22612" class="Keyword">import</a> <a id="22619" href="group-theory.homomorphisms-semigroups.html" class="Module">group-theory.homomorphisms-semigroups</a>
<a id="22657" class="Keyword">open</a> <a id="22662" class="Keyword">import</a> <a id="22669" href="group-theory.inverse-semigroups.html" class="Module">group-theory.inverse-semigroups</a>
<a id="22701" class="Keyword">open</a> <a id="22706" class="Keyword">import</a> <a id="22713" href="group-theory.invertible-elements-monoids.html" class="Module">group-theory.invertible-elements-monoids</a>
<a id="22754" class="Keyword">open</a> <a id="22759" class="Keyword">import</a> <a id="22766" href="group-theory.isomorphisms-abelian-groups.html" class="Module">group-theory.isomorphisms-abelian-groups</a>
<a id="22807" class="Keyword">open</a> <a id="22812" class="Keyword">import</a> <a id="22819" href="group-theory.isomorphisms-group-actions.html" class="Module">group-theory.isomorphisms-group-actions</a>
<a id="22859" class="Keyword">open</a> <a id="22864" class="Keyword">import</a> <a id="22871" href="group-theory.isomorphisms-groups.html" class="Module">group-theory.isomorphisms-groups</a>
<a id="22904" class="Keyword">open</a> <a id="22909" class="Keyword">import</a> <a id="22916" href="group-theory.isomorphisms-semigroups.html" class="Module">group-theory.isomorphisms-semigroups</a>
<a id="22953" class="Keyword">open</a> <a id="22958" class="Keyword">import</a> <a id="22965" href="group-theory.mere-equivalences-group-actions.html" class="Module">group-theory.mere-equivalences-group-actions</a>
<a id="23010" class="Keyword">open</a> <a id="23015" class="Keyword">import</a> <a id="23022" href="group-theory.monoids.html" class="Module">group-theory.monoids</a>
<a id="23043" class="Keyword">open</a> <a id="23048" class="Keyword">import</a> <a id="23055" href="group-theory.orbits-group-actions.html" class="Module">group-theory.orbits-group-actions</a>
<a id="23089" class="Keyword">open</a> <a id="23094" class="Keyword">import</a> <a id="23101" href="group-theory.precategory-of-group-actions.html" class="Module">group-theory.precategory-of-group-actions</a>
<a id="23143" class="Keyword">open</a> <a id="23148" class="Keyword">import</a> <a id="23155" href="group-theory.precategory-of-groups.html" class="Module">group-theory.precategory-of-groups</a>
<a id="23190" class="Keyword">open</a> <a id="23195" class="Keyword">import</a> <a id="23202" href="group-theory.precategory-of-semigroups.html" class="Module">group-theory.precategory-of-semigroups</a>
<a id="23241" class="Keyword">open</a> <a id="23246" class="Keyword">import</a> <a id="23253" href="group-theory.principal-group-actions.html" class="Module">group-theory.principal-group-actions</a>
<a id="23290" class="Keyword">open</a> <a id="23295" class="Keyword">import</a> <a id="23302" href="group-theory.semigroups.html" class="Module">group-theory.semigroups</a>
<a id="23326" class="Keyword">open</a> <a id="23331" class="Keyword">import</a> <a id="23338" href="group-theory.sheargroups.html" class="Module">group-theory.sheargroups</a>
<a id="23363" class="Keyword">open</a> <a id="23368" class="Keyword">import</a> <a id="23375" href="group-theory.stabilizer-groups.html" class="Module">group-theory.stabilizer-groups</a>
<a id="23406" class="Keyword">open</a> <a id="23411" class="Keyword">import</a> <a id="23418" href="group-theory.subgroups.html" class="Module">group-theory.subgroups</a>
<a id="23441" class="Keyword">open</a> <a id="23446" class="Keyword">import</a> <a id="23453" href="group-theory.substitution-functor-group-actions.html" class="Module">group-theory.substitution-functor-group-actions</a>
<a id="23501" class="Keyword">open</a> <a id="23506" class="Keyword">import</a> <a id="23513" href="group-theory.symmetric-groups.html" class="Module">group-theory.symmetric-groups</a>
<a id="23543" class="Keyword">open</a> <a id="23548" class="Keyword">import</a> <a id="23555" href="group-theory.transitive-group-actions.html" class="Module">group-theory.transitive-group-actions</a>
</pre>
## Linear algebra

<pre class="Agda"><a id="23625" class="Keyword">open</a> <a id="23630" class="Keyword">import</a> <a id="23637" href="linear-algebra.html" class="Module">linear-algebra</a>
<a id="23652" class="Keyword">open</a> <a id="23657" class="Keyword">import</a> <a id="23664" href="linear-algebra.constant-matrices.html" class="Module">linear-algebra.constant-matrices</a>
<a id="23697" class="Keyword">open</a> <a id="23702" class="Keyword">import</a> <a id="23709" href="linear-algebra.constant-vectors.html" class="Module">linear-algebra.constant-vectors</a>
<a id="23741" class="Keyword">open</a> <a id="23746" class="Keyword">import</a> <a id="23753" href="linear-algebra.diagonal-matrices-on-rings.html" class="Module">linear-algebra.diagonal-matrices-on-rings</a>
<a id="23795" class="Keyword">open</a> <a id="23800" class="Keyword">import</a> <a id="23807" href="linear-algebra.functoriality-matrices.html" class="Module">linear-algebra.functoriality-matrices</a>
<a id="23845" class="Keyword">open</a> <a id="23850" class="Keyword">import</a> <a id="23857" href="linear-algebra.functoriality-vectors.html" class="Module">linear-algebra.functoriality-vectors</a>
<a id="23894" class="Keyword">open</a> <a id="23899" class="Keyword">import</a> <a id="23906" href="linear-algebra.matrices-on-rings.html" class="Module">linear-algebra.matrices-on-rings</a>
<a id="23939" class="Keyword">open</a> <a id="23944" class="Keyword">import</a> <a id="23951" href="linear-algebra.matrices.html" class="Module">linear-algebra.matrices</a>
<a id="23975" class="Keyword">open</a> <a id="23980" class="Keyword">import</a> <a id="23987" href="linear-algebra.multiplication-matrices.html" class="Module">linear-algebra.multiplication-matrices</a>
<a id="24026" class="Keyword">open</a> <a id="24031" class="Keyword">import</a> <a id="24038" href="linear-algebra.scalar-multiplication-matrices.html" class="Module">linear-algebra.scalar-multiplication-matrices</a>
<a id="24084" class="Keyword">open</a> <a id="24089" class="Keyword">import</a> <a id="24096" href="linear-algebra.scalar-multiplication-vectors.html" class="Module">linear-algebra.scalar-multiplication-vectors</a>
<a id="24141" class="Keyword">open</a> <a id="24146" class="Keyword">import</a> <a id="24153" href="linear-algebra.transposition-matrices.html" class="Module">linear-algebra.transposition-matrices</a>
<a id="24191" class="Keyword">open</a> <a id="24196" class="Keyword">import</a> <a id="24203" href="linear-algebra.vectors-on-rings.html" class="Module">linear-algebra.vectors-on-rings</a>
<a id="24235" class="Keyword">open</a> <a id="24240" class="Keyword">import</a> <a id="24247" href="linear-algebra.vectors.html" class="Module">linear-algebra.vectors</a>
</pre>
## Order theory

<pre class="Agda"><a id="24300" class="Keyword">open</a> <a id="24305" class="Keyword">import</a> <a id="24312" href="order-theory.html" class="Module">order-theory</a>
<a id="24325" class="Keyword">open</a> <a id="24330" class="Keyword">import</a> <a id="24337" href="order-theory.chains-posets.html" class="Module">order-theory.chains-posets</a>
<a id="24364" class="Keyword">open</a> <a id="24369" class="Keyword">import</a> <a id="24376" href="order-theory.chains-preorders.html" class="Module">order-theory.chains-preorders</a>
<a id="24406" class="Keyword">open</a> <a id="24411" class="Keyword">import</a> <a id="24418" href="order-theory.decidable-subposets.html" class="Module">order-theory.decidable-subposets</a>
<a id="24451" class="Keyword">open</a> <a id="24456" class="Keyword">import</a> <a id="24463" href="order-theory.decidable-subpreorders.html" class="Module">order-theory.decidable-subpreorders</a>
<a id="24499" class="Keyword">open</a> <a id="24504" class="Keyword">import</a> <a id="24511" href="order-theory.finite-posets.html" class="Module">order-theory.finite-posets</a>
<a id="24538" class="Keyword">open</a> <a id="24543" class="Keyword">import</a> <a id="24550" href="order-theory.finite-preorders.html" class="Module">order-theory.finite-preorders</a>
<a id="24580" class="Keyword">open</a> <a id="24585" class="Keyword">import</a> <a id="24592" href="order-theory.finitely-graded-posets.html" class="Module">order-theory.finitely-graded-posets</a>
<a id="24628" class="Keyword">open</a> <a id="24633" class="Keyword">import</a> <a id="24640" href="order-theory.greatest-lower-bounds-posets.html" class="Module">order-theory.greatest-lower-bounds-posets</a>
<a id="24682" class="Keyword">open</a> <a id="24687" class="Keyword">import</a> <a id="24694" href="order-theory.interval-subposets.html" class="Module">order-theory.interval-subposets</a>
<a id="24726" class="Keyword">open</a> <a id="24731" class="Keyword">import</a> <a id="24738" href="order-theory.large-posets.html" class="Module">order-theory.large-posets</a>
<a id="24764" class="Keyword">open</a> <a id="24769" class="Keyword">import</a> <a id="24776" href="order-theory.large-preorders.html" class="Module">order-theory.large-preorders</a>
<a id="24805" class="Keyword">open</a> <a id="24810" class="Keyword">import</a> <a id="24817" href="order-theory.largest-elements-posets.html" class="Module">order-theory.largest-elements-posets</a>
<a id="24854" class="Keyword">open</a> <a id="24859" class="Keyword">import</a> <a id="24866" href="order-theory.largest-elements-preorders.html" class="Module">order-theory.largest-elements-preorders</a>
<a id="24906" class="Keyword">open</a> <a id="24911" class="Keyword">import</a> <a id="24918" href="order-theory.least-elements-posets.html" class="Module">order-theory.least-elements-posets</a>
<a id="24953" class="Keyword">open</a> <a id="24958" class="Keyword">import</a> <a id="24965" href="order-theory.least-elements-preorders.html" class="Module">order-theory.least-elements-preorders</a>
<a id="25003" class="Keyword">open</a> <a id="25008" class="Keyword">import</a> <a id="25015" href="order-theory.locally-finite-posets.html" class="Module">order-theory.locally-finite-posets</a>
<a id="25050" class="Keyword">open</a> <a id="25055" class="Keyword">import</a> <a id="25062" href="order-theory.maximal-chains-posets.html" class="Module">order-theory.maximal-chains-posets</a>
<a id="25097" class="Keyword">open</a> <a id="25102" class="Keyword">import</a> <a id="25109" href="order-theory.maximal-chains-preorders.html" class="Module">order-theory.maximal-chains-preorders</a>
<a id="25147" class="Keyword">open</a> <a id="25152" class="Keyword">import</a> <a id="25159" href="order-theory.meet-semilattices.html" class="Module">order-theory.meet-semilattices</a>
<a id="25190" class="Keyword">open</a> <a id="25195" class="Keyword">import</a> <a id="25202" href="order-theory.planar-binary-trees.html" class="Module">order-theory.planar-binary-trees</a>
<a id="25235" class="Keyword">open</a> <a id="25240" class="Keyword">import</a> <a id="25247" href="order-theory.posets.html" class="Module">order-theory.posets</a>
<a id="25267" class="Keyword">open</a> <a id="25272" class="Keyword">import</a> <a id="25279" href="order-theory.preorders.html" class="Module">order-theory.preorders</a>
<a id="25302" class="Keyword">open</a> <a id="25307" class="Keyword">import</a> <a id="25314" href="order-theory.subposets.html" class="Module">order-theory.subposets</a>
<a id="25337" class="Keyword">open</a> <a id="25342" class="Keyword">import</a> <a id="25349" href="order-theory.subpreorders.html" class="Module">order-theory.subpreorders</a>
<a id="25375" class="Keyword">open</a> <a id="25380" class="Keyword">import</a> <a id="25387" href="order-theory.total-posets.html" class="Module">order-theory.total-posets</a>
<a id="25413" class="Keyword">open</a> <a id="25418" class="Keyword">import</a> <a id="25425" href="order-theory.total-preorders.html" class="Module">order-theory.total-preorders</a>
</pre>
## Polytopes

<pre class="Agda"><a id="25481" class="Keyword">open</a> <a id="25486" class="Keyword">import</a> <a id="25493" href="polytopes.html" class="Module">polytopes</a>
<a id="25503" class="Keyword">open</a> <a id="25508" class="Keyword">import</a> <a id="25515" href="polytopes.abstract-polytopes.html" class="Module">polytopes.abstract-polytopes</a>
</pre>
## Ring theory

<pre class="Agda"><a id="25573" class="Keyword">open</a> <a id="25578" class="Keyword">import</a> <a id="25585" href="ring-theory.html" class="Module">ring-theory</a>
<a id="25597" class="Keyword">open</a> <a id="25602" class="Keyword">import</a> <a id="25609" href="ring-theory.division-rings.html" class="Module">ring-theory.division-rings</a>
<a id="25636" class="Keyword">open</a> <a id="25641" class="Keyword">import</a> <a id="25648" href="ring-theory.homomorphisms-rings.html" class="Module">ring-theory.homomorphisms-rings</a>
<a id="25680" class="Keyword">open</a> <a id="25685" class="Keyword">import</a> <a id="25692" href="ring-theory.ideals-generated-by-subsets-rings.html" class="Module">ring-theory.ideals-generated-by-subsets-rings</a>
<a id="25738" class="Keyword">open</a> <a id="25743" class="Keyword">import</a> <a id="25750" href="ring-theory.ideals-rings.html" class="Module">ring-theory.ideals-rings</a>
<a id="25775" class="Keyword">open</a> <a id="25780" class="Keyword">import</a> <a id="25787" href="ring-theory.invertible-elements-rings.html" class="Module">ring-theory.invertible-elements-rings</a>
<a id="25825" class="Keyword">open</a> <a id="25830" class="Keyword">import</a> <a id="25837" href="ring-theory.isomorphisms-rings.html" class="Module">ring-theory.isomorphisms-rings</a>
<a id="25868" class="Keyword">open</a> <a id="25873" class="Keyword">import</a> <a id="25880" href="ring-theory.localizations-rings.html" class="Module">ring-theory.localizations-rings</a>
<a id="25912" class="Keyword">open</a> <a id="25917" class="Keyword">import</a> <a id="25924" href="ring-theory.nontrivial-rings.html" class="Module">ring-theory.nontrivial-rings</a>
<a id="25953" class="Keyword">open</a> <a id="25958" class="Keyword">import</a> <a id="25965" href="ring-theory.rings.html" class="Module">ring-theory.rings</a>
</pre>
## Synthetic homotopy theory

<pre class="Agda"><a id="26026" class="Keyword">open</a> <a id="26031" class="Keyword">import</a> <a id="26038" href="synthetic-homotopy-theory.html" class="Module">synthetic-homotopy-theory</a>
<a id="26064" class="Keyword">open</a> <a id="26069" class="Keyword">import</a> <a id="26076" href="synthetic-homotopy-theory.23-pullbacks.html" class="Module">synthetic-homotopy-theory.23-pullbacks</a>
<a id="26115" class="Keyword">open</a> <a id="26120" class="Keyword">import</a> <a id="26127" href="synthetic-homotopy-theory.24-pushouts.html" class="Module">synthetic-homotopy-theory.24-pushouts</a>
<a id="26165" class="Keyword">open</a> <a id="26170" class="Keyword">import</a> <a id="26177" href="synthetic-homotopy-theory.25-cubical-diagrams.html" class="Module">synthetic-homotopy-theory.25-cubical-diagrams</a>
<a id="26223" class="Keyword">open</a> <a id="26228" class="Keyword">import</a> <a id="26235" href="synthetic-homotopy-theory.26-descent.html" class="Module">synthetic-homotopy-theory.26-descent</a>
<a id="26272" class="Keyword">open</a> <a id="26277" class="Keyword">import</a> <a id="26284" href="synthetic-homotopy-theory.26-id-pushout.html" class="Module">synthetic-homotopy-theory.26-id-pushout</a>
<a id="26324" class="Keyword">open</a> <a id="26329" class="Keyword">import</a> <a id="26336" href="synthetic-homotopy-theory.27-sequences.html" class="Module">synthetic-homotopy-theory.27-sequences</a>
<a id="26375" class="Keyword">open</a> <a id="26380" class="Keyword">import</a> <a id="26387" href="synthetic-homotopy-theory.circle.html" class="Module">synthetic-homotopy-theory.circle</a>
<a id="26420" class="Keyword">open</a> <a id="26425" class="Keyword">import</a> <a id="26432" href="synthetic-homotopy-theory.commutative-operations.html" class="Module">synthetic-homotopy-theory.commutative-operations</a>
<a id="26481" class="Keyword">open</a> <a id="26486" class="Keyword">import</a> <a id="26493" href="synthetic-homotopy-theory.cyclic-types.html" class="Module">synthetic-homotopy-theory.cyclic-types</a>
<a id="26532" class="Keyword">open</a> <a id="26537" class="Keyword">import</a> <a id="26544" href="synthetic-homotopy-theory.double-loop-spaces.html" class="Module">synthetic-homotopy-theory.double-loop-spaces</a>
<a id="26589" class="Keyword">open</a> <a id="26594" class="Keyword">import</a> <a id="26601" href="synthetic-homotopy-theory.functoriality-loop-spaces.html" class="Module">synthetic-homotopy-theory.functoriality-loop-spaces</a>
<a id="26653" class="Keyword">open</a> <a id="26658" class="Keyword">import</a> <a id="26665" href="synthetic-homotopy-theory.groups-of-loops-in-1-types.html" class="Module">synthetic-homotopy-theory.groups-of-loops-in-1-types</a>
<a id="26718" class="Keyword">open</a> <a id="26723" class="Keyword">import</a> <a id="26730" href="synthetic-homotopy-theory.infinite-cyclic-types.html" class="Module">synthetic-homotopy-theory.infinite-cyclic-types</a>
<a id="26778" class="Keyword">open</a> <a id="26783" class="Keyword">import</a> <a id="26790" href="synthetic-homotopy-theory.interval-type.html" class="Module">synthetic-homotopy-theory.interval-type</a>
<a id="26830" class="Keyword">open</a> <a id="26835" class="Keyword">import</a> <a id="26842" href="synthetic-homotopy-theory.iterated-loop-spaces.html" class="Module">synthetic-homotopy-theory.iterated-loop-spaces</a>
<a id="26889" class="Keyword">open</a> <a id="26894" class="Keyword">import</a> <a id="26901" href="synthetic-homotopy-theory.loop-spaces.html" class="Module">synthetic-homotopy-theory.loop-spaces</a>
<a id="26939" class="Keyword">open</a> <a id="26944" class="Keyword">import</a> <a id="26951" href="synthetic-homotopy-theory.pointed-dependent-functions.html" class="Module">synthetic-homotopy-theory.pointed-dependent-functions</a>
<a id="27005" class="Keyword">open</a> <a id="27010" class="Keyword">import</a> <a id="27017" href="synthetic-homotopy-theory.pointed-equivalences.html" class="Module">synthetic-homotopy-theory.pointed-equivalences</a>
<a id="27064" class="Keyword">open</a> <a id="27069" class="Keyword">import</a> <a id="27076" href="synthetic-homotopy-theory.pointed-families-of-types.html" class="Module">synthetic-homotopy-theory.pointed-families-of-types</a>
<a id="27128" class="Keyword">open</a> <a id="27133" class="Keyword">import</a> <a id="27140" href="synthetic-homotopy-theory.pointed-homotopies.html" class="Module">synthetic-homotopy-theory.pointed-homotopies</a>
<a id="27185" class="Keyword">open</a> <a id="27190" class="Keyword">import</a> <a id="27197" href="synthetic-homotopy-theory.pointed-maps.html" class="Module">synthetic-homotopy-theory.pointed-maps</a>
<a id="27236" class="Keyword">open</a> <a id="27241" class="Keyword">import</a> <a id="27248" href="synthetic-homotopy-theory.pointed-types.html" class="Module">synthetic-homotopy-theory.pointed-types</a>
<a id="27288" class="Keyword">open</a> <a id="27293" class="Keyword">import</a> <a id="27300" href="synthetic-homotopy-theory.spaces.html" class="Module">synthetic-homotopy-theory.spaces</a>
<a id="27333" class="Keyword">open</a> <a id="27338" class="Keyword">import</a> <a id="27345" href="synthetic-homotopy-theory.triple-loop-spaces.html" class="Module">synthetic-homotopy-theory.triple-loop-spaces</a>
<a id="27390" class="Keyword">open</a> <a id="27395" class="Keyword">import</a> <a id="27402" href="synthetic-homotopy-theory.universal-cover-circle.html" class="Module">synthetic-homotopy-theory.universal-cover-circle</a>
</pre>
## Tutorials

<pre class="Agda"><a id="27478" class="Keyword">open</a> <a id="27483" class="Keyword">import</a> <a id="27490" href="tutorials.basic-agda.html" class="Module">tutorials.basic-agda</a>
</pre>
## Type theories

<pre class="Agda"><a id="27542" class="Keyword">open</a> <a id="27547" class="Keyword">import</a> <a id="27554" href="type-theories.html" class="Module">type-theories</a>
<a id="27568" class="Keyword">open</a> <a id="27573" class="Keyword">import</a> <a id="27580" href="type-theories.comprehension-type-theories.html" class="Module">type-theories.comprehension-type-theories</a>
<a id="27622" class="Keyword">open</a> <a id="27627" class="Keyword">import</a> <a id="27634" href="type-theories.dependent-type-theories.html" class="Module">type-theories.dependent-type-theories</a>
<a id="27672" class="Keyword">open</a> <a id="27677" class="Keyword">import</a> <a id="27684" href="type-theories.fibered-dependent-type-theories.html" class="Module">type-theories.fibered-dependent-type-theories</a>
<a id="27730" class="Keyword">open</a> <a id="27735" class="Keyword">import</a> <a id="27742" href="type-theories.sections-dependent-type-theories.html" class="Module">type-theories.sections-dependent-type-theories</a>
<a id="27789" class="Keyword">open</a> <a id="27794" class="Keyword">import</a> <a id="27801" href="type-theories.simple-type-theories.html" class="Module">type-theories.simple-type-theories</a>
<a id="27836" class="Keyword">open</a> <a id="27841" class="Keyword">import</a> <a id="27848" href="type-theories.unityped-type-theories.html" class="Module">type-theories.unityped-type-theories</a>
</pre>
## Univalent combinatorics

<pre class="Agda"><a id="27926" class="Keyword">open</a> <a id="27931" class="Keyword">import</a> <a id="27938" href="univalent-combinatorics.html" class="Module">univalent-combinatorics</a>
<a id="27962" class="Keyword">open</a> <a id="27967" class="Keyword">import</a> <a id="27974" href="univalent-combinatorics.2-element-decidable-subtypes.html" class="Module">univalent-combinatorics.2-element-decidable-subtypes</a>
<a id="28027" class="Keyword">open</a> <a id="28032" class="Keyword">import</a> <a id="28039" href="univalent-combinatorics.2-element-subtypes.html" class="Module">univalent-combinatorics.2-element-subtypes</a>
<a id="28082" class="Keyword">open</a> <a id="28087" class="Keyword">import</a> <a id="28094" href="univalent-combinatorics.2-element-types.html" class="Module">univalent-combinatorics.2-element-types</a>
<a id="28134" class="Keyword">open</a> <a id="28139" class="Keyword">import</a> <a id="28146" href="univalent-combinatorics.binomial-types.html" class="Module">univalent-combinatorics.binomial-types</a>
<a id="28185" class="Keyword">open</a> <a id="28190" class="Keyword">import</a> <a id="28197" href="univalent-combinatorics.cartesian-product-types.html" class="Module">univalent-combinatorics.cartesian-product-types</a>
<a id="28245" class="Keyword">open</a> <a id="28250" class="Keyword">import</a> <a id="28257" href="univalent-combinatorics.classical-finite-types.html" class="Module">univalent-combinatorics.classical-finite-types</a>
<a id="28304" class="Keyword">open</a> <a id="28309" class="Keyword">import</a> <a id="28316" href="univalent-combinatorics.complements-isolated-points.html" class="Module">univalent-combinatorics.complements-isolated-points</a>
<a id="28368" class="Keyword">open</a> <a id="28373" class="Keyword">import</a> <a id="28380" href="univalent-combinatorics.coproduct-types.html" class="Module">univalent-combinatorics.coproduct-types</a>
<a id="28420" class="Keyword">open</a> <a id="28425" class="Keyword">import</a> <a id="28432" href="univalent-combinatorics.counting-decidable-subtypes.html" class="Module">univalent-combinatorics.counting-decidable-subtypes</a>
<a id="28484" class="Keyword">open</a> <a id="28489" class="Keyword">import</a> <a id="28496" href="univalent-combinatorics.counting-dependent-pair-types.html" class="Module">univalent-combinatorics.counting-dependent-pair-types</a>
<a id="28550" class="Keyword">open</a> <a id="28555" class="Keyword">import</a> <a id="28562" href="univalent-combinatorics.counting-maybe.html" class="Module">univalent-combinatorics.counting-maybe</a>
<a id="28601" class="Keyword">open</a> <a id="28606" class="Keyword">import</a> <a id="28613" href="univalent-combinatorics.counting.html" class="Module">univalent-combinatorics.counting</a>
<a id="28646" class="Keyword">open</a> <a id="28651" class="Keyword">import</a> <a id="28658" href="univalent-combinatorics.cubes.html" class="Module">univalent-combinatorics.cubes</a>
<a id="28688" class="Keyword">open</a> <a id="28693" class="Keyword">import</a> <a id="28700" href="univalent-combinatorics.decidable-dependent-function-types.html" class="Module">univalent-combinatorics.decidable-dependent-function-types</a>
<a id="28759" class="Keyword">open</a> <a id="28764" class="Keyword">import</a> <a id="28771" href="univalent-combinatorics.decidable-dependent-pair-types.html" class="Module">univalent-combinatorics.decidable-dependent-pair-types</a>
<a id="28826" class="Keyword">open</a> <a id="28831" class="Keyword">import</a> <a id="28838" href="univalent-combinatorics.decidable-subtypes.html" class="Module">univalent-combinatorics.decidable-subtypes</a>
<a id="28881" class="Keyword">open</a> <a id="28886" class="Keyword">import</a> <a id="28893" href="univalent-combinatorics.dependent-function-types.html" class="Module">univalent-combinatorics.dependent-function-types</a>
<a id="28942" class="Keyword">open</a> <a id="28947" class="Keyword">import</a> <a id="28954" href="univalent-combinatorics.dedekind-finite-sets.html" class="Module">univalent-combinatorics.dedekind-finite-sets</a>
<a id="28999" class="Keyword">open</a> <a id="29004" class="Keyword">import</a> <a id="29011" href="univalent-combinatorics.dependent-sum-finite-types.html" class="Module">univalent-combinatorics.dependent-sum-finite-types</a>
<a id="29062" class="Keyword">open</a> <a id="29067" class="Keyword">import</a> <a id="29074" href="univalent-combinatorics.distributivity-of-set-truncation-over-finite-products.html" class="Module">univalent-combinatorics.distributivity-of-set-truncation-over-finite-products</a>
<a id="29152" class="Keyword">open</a> <a id="29157" class="Keyword">import</a> <a id="29164" href="univalent-combinatorics.double-counting.html" class="Module">univalent-combinatorics.double-counting</a>
<a id="29204" class="Keyword">open</a> <a id="29209" class="Keyword">import</a> <a id="29216" href="univalent-combinatorics.embeddings-standard-finite-types.html" class="Module">univalent-combinatorics.embeddings-standard-finite-types</a>
<a id="29273" class="Keyword">open</a> <a id="29278" class="Keyword">import</a> <a id="29285" href="univalent-combinatorics.embeddings.html" class="Module">univalent-combinatorics.embeddings</a>
<a id="29320" class="Keyword">open</a> <a id="29325" class="Keyword">import</a> <a id="29332" href="univalent-combinatorics.equality-finite-types.html" class="Module">univalent-combinatorics.equality-finite-types</a>
<a id="29378" class="Keyword">open</a> <a id="29383" class="Keyword">import</a> <a id="29390" href="univalent-combinatorics.equality-standard-finite-types.html" class="Module">univalent-combinatorics.equality-standard-finite-types</a>
<a id="29445" class="Keyword">open</a> <a id="29450" class="Keyword">import</a> <a id="29457" href="univalent-combinatorics.equivalences-cubes.html" class="Module">univalent-combinatorics.equivalences-cubes</a>
<a id="29500" class="Keyword">open</a> <a id="29505" class="Keyword">import</a> <a id="29512" href="univalent-combinatorics.equivalences-standard-finite-types.html" class="Module">univalent-combinatorics.equivalences-standard-finite-types</a>
<a id="29571" class="Keyword">open</a> <a id="29576" class="Keyword">import</a> <a id="29583" href="univalent-combinatorics.equivalences.html" class="Module">univalent-combinatorics.equivalences</a>
<a id="29620" class="Keyword">open</a> <a id="29625" class="Keyword">import</a> <a id="29632" href="univalent-combinatorics.fibers-of-maps.html" class="Module">univalent-combinatorics.fibers-of-maps</a>
<a id="29671" class="Keyword">open</a> <a id="29676" class="Keyword">import</a> <a id="29683" href="univalent-combinatorics.finite-choice.html" class="Module">univalent-combinatorics.finite-choice</a>
<a id="29721" class="Keyword">open</a> <a id="29726" class="Keyword">import</a> <a id="29733" href="univalent-combinatorics.finite-connected-components.html" class="Module">univalent-combinatorics.finite-connected-components</a>
<a id="29785" class="Keyword">open</a> <a id="29790" class="Keyword">import</a> <a id="29797" href="univalent-combinatorics.finite-presentations.html" class="Module">univalent-combinatorics.finite-presentations</a>
<a id="29842" class="Keyword">open</a> <a id="29847" class="Keyword">import</a> <a id="29854" href="univalent-combinatorics.finite-types.html" class="Module">univalent-combinatorics.finite-types</a>
<a id="29891" class="Keyword">open</a> <a id="29896" class="Keyword">import</a> <a id="29903" href="univalent-combinatorics.finitely-presented-types.html" class="Module">univalent-combinatorics.finitely-presented-types</a>
<a id="29952" class="Keyword">open</a> <a id="29957" class="Keyword">import</a> <a id="29964" href="univalent-combinatorics.function-types.html" class="Module">univalent-combinatorics.function-types</a>
<a id="30003" class="Keyword">open</a> <a id="30008" class="Keyword">import</a> <a id="30015" href="univalent-combinatorics.image-of-maps.html" class="Module">univalent-combinatorics.image-of-maps</a>
<a id="30053" class="Keyword">open</a> <a id="30058" class="Keyword">import</a> <a id="30065" href="univalent-combinatorics.inequality-types-with-counting.html" class="Module">univalent-combinatorics.inequality-types-with-counting</a>
<a id="30120" class="Keyword">open</a> <a id="30125" class="Keyword">import</a> <a id="30132" href="univalent-combinatorics.injective-maps.html" class="Module">univalent-combinatorics.injective-maps</a>
<a id="30171" class="Keyword">open</a> <a id="30176" class="Keyword">import</a> <a id="30183" href="univalent-combinatorics.kuratowsky-finite-sets.html" class="Module">univalent-combinatorics.kuratowsky-finite-sets</a>
<a id="30230" class="Keyword">open</a> <a id="30235" class="Keyword">import</a> <a id="30242" href="univalent-combinatorics.lists.html" class="Module">univalent-combinatorics.lists</a>
<a id="30272" class="Keyword">open</a> <a id="30277" class="Keyword">import</a> <a id="30284" href="univalent-combinatorics.maybe.html" class="Module">univalent-combinatorics.maybe</a>
<a id="30314" class="Keyword">open</a> <a id="30319" class="Keyword">import</a> <a id="30326" href="univalent-combinatorics.orientations-complete-undirected-graph.html" class="Module">univalent-combinatorics.orientations-complete-undirected-graph</a>
<a id="30389" class="Keyword">open</a> <a id="30394" class="Keyword">import</a> <a id="30401" href="univalent-combinatorics.orientations-cubes.html" class="Module">univalent-combinatorics.orientations-cubes</a>
<a id="30444" class="Keyword">open</a> <a id="30449" class="Keyword">import</a> <a id="30456" href="univalent-combinatorics.petri-nets.html" class="Module">univalent-combinatorics.petri-nets</a>
<a id="30491" class="Keyword">open</a> <a id="30496" class="Keyword">import</a> <a id="30503" href="univalent-combinatorics.pi-finite-types.html" class="Module">univalent-combinatorics.pi-finite-types</a>
<a id="30543" class="Keyword">open</a> <a id="30548" class="Keyword">import</a> <a id="30555" href="univalent-combinatorics.pigeonhole-principle.html" class="Module">univalent-combinatorics.pigeonhole-principle</a>
<a id="30600" class="Keyword">open</a> <a id="30605" class="Keyword">import</a> <a id="30612" href="univalent-combinatorics.presented-pi-finite-types.html" class="Module">univalent-combinatorics.presented-pi-finite-types</a>
<a id="30662" class="Keyword">open</a> <a id="30667" class="Keyword">import</a> <a id="30674" href="univalent-combinatorics.ramsey-theory.html" class="Module">univalent-combinatorics.ramsey-theory</a>
<a id="30712" class="Keyword">open</a> <a id="30717" class="Keyword">import</a> <a id="30724" href="univalent-combinatorics.retracts-of-finite-types.html" class="Module">univalent-combinatorics.retracts-of-finite-types</a>
<a id="30773" class="Keyword">open</a> <a id="30778" class="Keyword">import</a> <a id="30785" href="univalent-combinatorics.skipping-element-standard-finite-types.html" class="Module">univalent-combinatorics.skipping-element-standard-finite-types</a>
<a id="30848" class="Keyword">open</a> <a id="30853" class="Keyword">import</a> <a id="30860" href="univalent-combinatorics.species.html" class="Module">univalent-combinatorics.species</a>
<a id="30892" class="Keyword">open</a> <a id="30897" class="Keyword">import</a> <a id="30904" href="univalent-combinatorics.standard-finite-pruned-trees.html" class="Module">univalent-combinatorics.standard-finite-pruned-trees</a>
<a id="30957" class="Keyword">open</a> <a id="30962" class="Keyword">import</a> <a id="30969" href="univalent-combinatorics.standard-finite-trees.html" class="Module">univalent-combinatorics.standard-finite-trees</a>
<a id="31015" class="Keyword">open</a> <a id="31020" class="Keyword">import</a> <a id="31027" href="univalent-combinatorics.standard-finite-types.html" class="Module">univalent-combinatorics.standard-finite-types</a>
<a id="31073" class="Keyword">open</a> <a id="31078" class="Keyword">import</a> <a id="31085" href="univalent-combinatorics.sums-of-natural-numbers.html" class="Module">univalent-combinatorics.sums-of-natural-numbers</a>
<a id="31133" class="Keyword">open</a> <a id="31138" class="Keyword">import</a> <a id="31145" href="univalent-combinatorics.surjective-maps.html" class="Module">univalent-combinatorics.surjective-maps</a>
<a id="31185" class="Keyword">open</a> <a id="31190" class="Keyword">import</a> <a id="31197" href="univalent-combinatorics.symmetric-difference.html" class="Module">univalent-combinatorics.symmetric-difference</a>
</pre>
## Wild algebra

<pre class="Agda"><a id="31272" class="Keyword">open</a> <a id="31277" class="Keyword">import</a> <a id="31284" href="wild-algebra.html" class="Module">wild-algebra</a>
<a id="31297" class="Keyword">open</a> <a id="31302" class="Keyword">import</a> <a id="31309" href="wild-algebra.magmas.html" class="Module">wild-algebra.magmas</a>
<a id="31329" class="Keyword">open</a> <a id="31334" class="Keyword">import</a> <a id="31341" href="wild-algebra.morphisms-magmas.html" class="Module">wild-algebra.morphisms-magmas</a>
<a id="31371" class="Keyword">open</a> <a id="31376" class="Keyword">import</a> <a id="31383" href="wild-algebra.morphisms-wild-unital-magmas.html" class="Module">wild-algebra.morphisms-wild-unital-magmas</a>
<a id="31425" class="Keyword">open</a> <a id="31430" class="Keyword">import</a> <a id="31437" href="wild-algebra.universal-property-lists-wild-monoids.html" class="Module">wild-algebra.universal-property-lists-wild-monoids</a>
<a id="31488" class="Keyword">open</a> <a id="31493" class="Keyword">import</a> <a id="31500" href="wild-algebra.wild-groups.html" class="Module">wild-algebra.wild-groups</a>
<a id="31525" class="Keyword">open</a> <a id="31530" class="Keyword">import</a> <a id="31537" href="wild-algebra.wild-loops.html" class="Module">wild-algebra.wild-loops</a>
<a id="31561" class="Keyword">open</a> <a id="31566" class="Keyword">import</a> <a id="31573" href="wild-algebra.wild-monoids.html" class="Module">wild-algebra.wild-monoids</a>
<a id="31599" class="Keyword">open</a> <a id="31604" class="Keyword">import</a> <a id="31611" href="wild-algebra.wild-quasigroups.html" class="Module">wild-algebra.wild-quasigroups</a>
<a id="31641" class="Keyword">open</a> <a id="31646" class="Keyword">import</a> <a id="31653" href="wild-algebra.wild-semigroups.html" class="Module">wild-algebra.wild-semigroups</a>
<a id="31682" class="Keyword">open</a> <a id="31687" class="Keyword">import</a> <a id="31694" href="wild-algebra.wild-unital-magmas.html" class="Module">wild-algebra.wild-unital-magmas</a>
</pre>
## Everything

See the list of all Agda modules [here](everything.html).

