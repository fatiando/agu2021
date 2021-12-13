<!--
This file defines the contents of each slide.
The reveal.js configuration can be found in index.html
-->

<!-- .slide: class="slide-title" data-background-color="#060629" data-background-size="contain" -->

<!-- Place the content at the bottom of the slide -->
<div class="r-stretch">
</div>

<!-- Main title page -->
<div class="lefted">

<h1 id="talk-title">
Design useful tools that do one thing well and work together:
<br>
<span style="font-size: 3.5rem;">
Rediscovering the UNIX philosophy while building the Fatiando a Terra project
</span>
</h1>

<p id="talk-authors">
<strong>Leonardo Uieda</strong>,
Lu Li,
Santiago Soler,
Agustina Pesce
</p>

<!-- Place location and date side-by-side with affiliation logos -->
<div class="container talk-info">
<div class="col-large">

AGU 2021
<span style="margin: 0 20px">•</span>
13 December 2021

<!-- Permission to reuse and CC-BY license logo -->
<p><a href="https://creativecommons.org/licenses/by/4.0/">
<i class="fab fa-creative-commons"></i><i class="fab fa-creative-commons-by" style="margin: 0 10px 0 2px"></i>
CC-BY 4.0 License
</a></p>

<i class="fa fa-camera" style="margin: 0 10px 0 0"></i>
Feel free to screenshot/share/reuse/remix this presentation

</div>
<div class="col-small">

<!-- Add logos here. Need these wrappers to align them to the bottom right -->
<div class="talk-logos-container">
<div class="talk-logos">
    <img src="assets/university-of-liverpool-white.png">
    <img src="assets/compgeolab-banner-light.svg">
    <img src="assets/conicet.png">
    <img src="assets/universidad-nacional-de-san-juan.png">
    <img src="assets/uwacrest-white.svg">
</div>
</div>

</div>
</div>

</div>

---

<!-- .slide: data-background-image="assets/fatiando-a-terra-front-page.svg" data-background-size="contain" data-background-repeat="no-repeat" data-background-color="#000000" -->

<div class="r-stretch bottom-right">

[Fatiando a Terra](https://www.fatiando.org)
is a collection of open-source Python tools for geoscience.
**Fun fact:** the name is Portuguese for **"Slicing the Earth"**

</div>

---

<!-- .slide: data-background-image="assets/fatiando-first-commit.svg" data-background-size="contain" data-background-repeat="no-repeat" data-background-color="#000000" -->

<div class="r-stretch bottom-right">

First released as the `fatiando` Python 2.7 package on April 2010
(commit: [928515b](https://github.com/fatiando/fatiando/commit/928515b0fcfdccecbc4f661ed2469390ef43ec1d))
<br>
Last version is **v0.5** (2016), archived at [legacy.fatiando.org](https://legacy.fatiando.org)

</div>

---

<div class="container">
<div class="col" style="padding-right: 5%">

<h1 style="color: #0000dd;">
<i class="far fa-thumbs-up" style="margin-right: 20px;"></i>
The good parts
</h1>

<hr>

<ul class="fa-ul">

<li>
<span class="fa-li"> <i class="fa fa-lightbulb fa-fw"></i> </span>
State-of-the-art algorithms
</li>

<li>
<span class="fa-li"> <i class="fa fa-file-alt fa-fw"></i> </span>
Used in several thesis & papers (>70 citations)
</li>

<li>
<span class="fa-li"> <i class="fa fa-users fa-fw"></i> </span>
2-3 active contributors
</li>

</ul>

</div>
<div class="col fragment" style="padding-left: 5%">

<h1 style="color: #dd0000;">
<i class="far fa-thumbs-down" style="margin-right: 20px;"></i>
The bad parts
</h1>

<hr>

<ul class="fa-ul">

<li>
<span class="fa-li"> <i class="fa fa-gamepad fa-fw"></i> </span>
Too many toy problems and experimental code
</li>

<li>
<span class="fa-li"> <i class="fa fa-tools fa-fw"></i> </span>
Difficult to maintain
</li>

<li>
<span class="fa-li"> <i class="fa fa-leaf fa-fw"></i> </span>
Lack of integration with larger ecosystem
</li>

</ul>
</div>

---

# New directions 🚀

<hr>

<div class="huge">

Multiple tools with narrow scope

Focus on real use cases

Documentation-driven development

Lower barriers to entry

</div>

<div class="r-stretch bottom-right">

We decided to start from scratch in 2018.
See [this blog post](https://www.leouieda.com/blog/future-of-fatiando.html).

</div>

---

<div class="container small">
<div class="col">

## Verde

ML-based spatial data processing and **gridding**

<i class="fab fa-github" title="GitHub repository"></i>
<a href="https://github.com/fatiando/verde">fatiando/verde</a>

<i class="fa fa-check" style="color: green" title="Project status"></i>
Stable

</div>
<div class="col fragment">

## Pooch

The easiest way to **download and cache** data

<i class="fab fa-github" title="GitHub repository"></i>
<a href="https://github.com/fatiando/pooch">fatiando/pooch</a>

<i class="fa fa-check" style="color: green" title="Project status"></i>
Stable


</div>
</div>
<div class="container small">
<div class="col fragment">

## Harmonica

Processing and modeling <b>gravity & magnetic</b> data

<i class="fab fa-github" title="GitHub repository"></i>
<a href="https://github.com/fatiando/harmonica">fatiando/harmonica</a>

<i class="fa fa-sync-alt" style="color: orange" title="Project status"></i>
Still changing

</div>
<div class="col fragment">

## Boule

Reference <b>ellipsoids</b> and <b>normal gravity</b> for the Earth and other planets

<i class="fab fa-github" title="GitHub repository"></i>
<a href="https://github.com/fatiando/boule">fatiando/boule</a>

<i class="fa fa-sync-alt" style="color: orange" title="Project status"></i>
Still changing

</div>
</div>

---

# Current developments

* FFT-based processing and 3D visualization in Harmonica
* Redesign of Boule ellipsoid classes
* Less memory-intensive gridding in Verde
* New shared sample data repository: [fatiando/data](https://github.com/fatiando/data)
* Planned new sample data package **Ensaio**

---

<div class="centered">

<div>

# Get involved

<div class="container">
<div class="col">

<ul class="fa-ul">

<li>
<span class="fa-li"><i class="fa fa-home"></i></span>
Learn more at <a href="https://www.fatiando.org">fatiando.org</a>
</li>

<li>
<span class="fa-li"><i class="fab fa-slack"></i></span>
Come say "Hi" on <a href="https://www.fatiando.org/contact">Slack</a>
</li>

<li>
<span class="fa-li"><i class="fa fa-microphone-alt"></i></span>
Join our weekly
<a href="https://github.com/fatiando/community">video calls</a>
</li>

</ul>

</div>
<div class="col">
<img src="assets/fatiando-community-call.jpg">
</div>
</div>

</div>
</div>

---

<!-- .slide: class="slide-license" -->

<div class="centered">
<div>

<p class="license-icons">
<i class="fab fa-creative-commons"></i><i class="fab fa-creative-commons-by"></i>
</p>

Unless otherwise noted,
the contents of this presentation are
licensed under the
<br>
[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

</div>
</div>
