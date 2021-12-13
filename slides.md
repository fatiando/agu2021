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

<!-- .slide: class="slide-transition" data-background-color="#060629" -->

<div class="centered">
<div style="width: 70%;">

# A bit of history

<img src="assets/logo-evolution.svg" style="margin-top: 5%;">

</div>
</div>

---

<!-- .slide: data-background-image="assets/fatiando-first-commit.svg" data-background-size="contain" data-background-repeat="no-repeat" data-background-color="#000000" -->

<div class="r-stretch bottom-right">

First released as the `fatiando` Python 2.7 package on April 2010
(commit: [928515b](https://github.com/fatiando/fatiando/commit/928515b0fcfdccecbc4f661ed2469390ef43ec1d))

</div>

---

<!-- .slide: data-background-image="assets/fatiando-first-commit-vcs.svg" data-background-size="contain" data-background-repeat="no-repeat" data-background-color="#000000" -->

<div class="r-stretch bottom-right">

We **learned a lot** about software development:
version control (went through 3),
<br>
tests, packaging, documentation, and more.

</div>

---

<!-- .slide: data-background-image="assets/fatiando-docs-v0.5.jpg" data-background-size="contain" data-background-repeat="no-repeat" data-background-color="#000000" -->

<div class="r-stretch bottom-left bottom-dark">

We made several releases until **v0.5** (2016). doi:[10.5281/zenodo.157746](https://doi.org/10.5281/zenodo.157746)
<br>
Now archived at [legacy.fatiando.org](https://legacy.fatiando.org)

</div>

---

<div class="container">
<div class="col-left" style="padding-right: 5%">

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

<li>
<span class="fa-li"> <i class="fa fa-chalkboard-teacher fa-fw"></i> </span>
Enabled teaching through simulation
</li>

</ul>

</div>
<div class="col-right fragment" style="padding-left: 5%">

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
<span class="fa-li"> <i class="fas fa-vial fa-fw"></i> </span>
Not designed for testability
</li>

<li>
<span class="fa-li"> <i class="fa fa-tools fa-fw"></i> </span>
Difficult to maintain
</li>

<li>
<span class="fa-li"> <i class="fa fa-landmark fa-fw"></i> </span>
Unstable foundations for growth
</li>

</ul>
</div>

---

<div class="container small">
<div class="col">

### ✨ New Fatiando ✨

Split into libraries

Better coding practices

Use modern tools

Supplement the ecosystem

</div>
<div class="col fragment">

<a href="http://www.fatiando.org/pooch">
<img class="project-logo center-block" src="assets/pooch-logo.svg">
</a>

Data <b>download & caching</b> (used by other libraries)

<ul class="fa-ul project-icons">
<li><i class="fa-li fab fa-github fa-fw" title="Github repository"></i>
   <a href="https://github.com/fatiando/pooch">fatiando/pooch</a>
</li>
<li><i class="fa-li fas fa-bookmark fa-fw" title="Publication"></i>
   doi: <a href="https://doi.org/10.21105/joss.01943">10.21105/joss.01943</a>
</li>
<li><i class="fa-li fa fa-check fa-fw" style="color: green" title="Project status"></i>
   Stable and ready for use
</li>
</ul>

</div>
<div class="col fragment">

<a href="http://www.fatiando.org/verde">
<img class="project-logo center-block" src="assets/verde-logo.svg">
</a>

ML-based point data processing and <b>gridding</b>

<ul class="fa-ul project-icons">
<li><i class="fa-li fab fa-github fa-fw" title="Github repository"></i>
   <a href="https://github.com/fatiando/verde">fatiando/verde</a>
</li>
<li><i class="fa-li fas fa-bookmark fa-fw" title="Publication"></i>
   doi: <a href="https://doi.org/10.21105/joss.00957">10.21105/joss.00957</a>
</li>
<li><i class="fa-li fa fa-check fa-fw" style="color: green" title="Project status"></i>
   Stable and ready for use
</li>
</ul>

</div>
</div>
<div class="container small" style="margin-top: 4%">
<div class="col fragment">

<a href="http://www.fatiando.org/harmonica">
<img class="project-logo center-block" src="assets/harmonica-logo.svg">
</a>

Processing and modeling <b>gravity & magnetic</b> data

<ul class="fa-ul project-icons">
<li><i class="fa-li fab fa-github fa-fw" title="Github repository"></i>
   <a href="https://github.com/fatiando/harmonica">fatiando/harmonica</a>
</li>
<li><i class="fa-li fa fa-sync-alt fa-fw" style="color: green" title="Project status"></i>
   Ready for use but still changing
</li>
</ul>

</div>
<div class="col fragment">

<a href="http://www.fatiando.org/boule">
<img class="project-logo center-block" src="assets/boule-logo.svg">
</a>

Reference <b>ellipsoids</b> for <b>normal gravity</b>

<ul class="fa-ul project-icons">
<li><i class="fa-li fab fa-github fa-fw" title="Github repository"></i>
   <a href="https://github.com/fatiando/boule">fatiando/boule</a>
</li>
<li><i class="fa-li fa fa-sync-alt fa-fw" style="color: green" title="Project status"></i>
   Ready for use but still changing
</li>
</ul>

</div>
<div class="col fragment">

<a href="http://www.fatiando.org/rockhound">
<img class="project-logo center-block" src="assets/rockhound-logo.svg">
</a>

Repository for our **sample data** (uses Pooch)

<ul class="fa-ul project-icons">
<li><i class="fa-li fab fa-github fa-fw" title="Github repository"></i>
   <a href="https://github.com/fatiando/rockhound">fatiando/rockhound</a>
</li>
<li><i class="fa-li fa fa-flask fa-fw" style="color: orange" title="Project status"></i>
    Early stages of design
</li>
</ul>

</div>
</div>

---

<!-- .slide: class="slide-transition" data-background-color="#000000" data-background-image="assets/demo-time.gif" data-background-repeat="no-repeat" data-background-position="center" data-background-opacity="70%" -->

<div class="centered">
<div>

# Demo time!

</div>
</div>

---

<!-- .slide: class="slide-transition" data-background-color="#060629" -->

<div class="centered">
<div>

<h1>
Ongoing
<br>
developments
<br>
<i class="fa fa-wrench"></i>
</h1>

</div>
</div>

---

<div class="container">
<div class="col-large">

# Equivalent sources

Using **gradient boosting** to scale to millions of data

Preprint on EarthArXiv (minor revision at GJI): [Soler & Uieda (2021)](https://doi.org/10.31223/X58G7C)

Code coming to Harmonica in the next few months

</div>
<div class="col-small">

<img src="assets/gradient-boosting.svg" style="width: 90%">

</div>
</div>

---

# In development

* Frequency domain transformation ([fatiando/harmonica#238](https://github.com/fatiando/harmonica/pull/238))
* Tri-axial ellipsoids ([fatiando/boule#76](https://github.com/fatiando/boule/issues/76))
* Re-organization of the documentation ([Pooch v1.4.0 was the first](https://www.fatiando.org/pooch/v1.4.0/))
* Gather open-access data for tutorials ([included in RockHound](https://github.com/fatiando/meeting-notes/blob/main/community-calls/2021.md#2021-05-13))
* Increase recruitment and diversity of our community

---

<!-- .slide: class="slide-transition" data-background-color="#060629" -->

<div class="centered">
<div>

<h1>
Come for the <strong>code</strong> <i class="fas fa-code"></i>
<br>
Stay for the <strong>community</strong> <i class="fas fa-users"></i>
</h1>

</div>
</div>

---

# Get started

<ul class="fa-ul">

<li class="fragment">
<span class="fa-li"><i class="fab fa-python"></i></span>
Not experienced with Python?
<ul style="margin: 1em 0 0 1em;">
<li>
  Software Carpentry has <a href="https://swcarpentry.github.io/python-novice-inflammation/">great open-access lessons</a>
</li>
</ul>
</li>

<li class="fragment">
<span class="fa-li"><i class="fab fa-youtube"></i></span>
Watch some tutorials on YouTube:
<ul style="margin: 1em 0 0 1em;">
<li>
  Verde (<a href="https://www.youtube.com/watch?v=-xZdNdvzm3E">Transform 2020 </a>) and
  Harmonica (<a href="https://www.youtube.com/watch?v=0bxZcCAr6bwab_channel=SoftwareUnderground">Transform 2021</a>)
</li>
</ul>
</li>

<li class="fragment">
<span class="fa-li"> <i class="fas fa-book"></i> </span>
Documentation for each library
(links at <a href="https://www.fatiando.org">fatiando.org</a>)
</li>

</ul>

---

# Get involved

There are many ways to participate:

<div class="container">
<div class="col-left">
<ul>
<li class="fragment">Write code</li>
<li class="fragment">Documentation and examples</li>
<li class="fragment">Give feedback</li>
</lu>
</div>
<div class="col-right">
<ul>
<li class="fragment">Join the conversation</li>
<li class="fragment">Share your expertise</li>
<li class="fragment">Guide future development</li>
</ul>
</div>
</div>

<div class="fragment">

**Your help is always welcome!**

</div>

---

# Where to find us

<ul class="fa-ul">

<li class="fragment">
<span class="fa-li"><i class="fab fa-slack"></i></span>
<a href="http://contact.fatiando.org/">Slack</a>:
where we chat about meetings, events, questions, experiences
</li>

<li class="fragment">
<span class="fa-li"><i class="fab fa-github"></i></span>
<a href="https://github.com/fatiando/">GitHub</a>:
where we discuss development details and review code
</li>

<li class="fragment">
<span class="fa-li"><i class="fa fa-microphone-alt"></i></span>
<div class="container">
<div class="col-left">
<a href="https://github.com/fatiando/meeting-notes">Video Calls</a>:
<b>Community Calls</b> (monthly) to socialize and plan,
<b>Development Calls</b> (weekly) to discuss the details
</div>
<div class="col-right">
<img src="assets/fatiando-community-call.jpg">
</div>
</div>
</li>

</ul>

---

<div class="centered huge">
<div>

About Fatiando:
[fatiando.org](https://www.fatiando.org)

Our research:
[compgeolab.org](https://www.compgeolab.org)

Slides + demo:
[github.com/leouieda/2021-06-22-gfz](https://github.com/leouieda/2021-06-22-gfz)

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
