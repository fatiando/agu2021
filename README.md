# Design useful tools that do one thing well and work together: rediscovering the UNIX philosophy while building the Fatiando a Terra project

Leonardo Uieda<sup>1</sup>,
Lu Li<sup>2</sup>,
Santiago Soler<sup>3,4</sup>,
Agustina Pesce<sup>3,4</sup>

> <sup>1</sup>Department of Earth, Ocean and Ecological Sciences, School of Environmental Sciences, University of Liverpool, UK
> <br>
> <sup>2</sup> School of Earth Sciences, The University of Western Australia, Australia
> <br>
> <sup>3</sup> CONICET, Argentina
> <br>
> <sup>4</sup> Instituto Geofísico Sismológico Volponi, UNSJ, Argentina

This is an invited presentation about the past, current, and future of the
[Fatiando a Terra](https://www.fatiando.org) project. We will cover the
current functionality, recent developments, and lessons learned along the way.

| | Information |
|---:|:----|
| Abstract | [NS15C-0380](https://agu.confex.com/agu/fm21/meetingapp.cgi/Paper/818064) |
| Session | [NS013 - Open-source software for near-surface geophysics and its applications](https://agu.confex.com/agu/fm21/meetingapp.cgi/Session/122971) |
| When | Monday 13 December 2021 / 22:00 - 00:00 UTC |
| Poster | [iPoster platform](https://agu2021fallmeeting-agu.ipostersessions.com/Default.aspx?s=D6-7C-10-44-E1-93-A6-5D-31-A5-54-52-5C-80-2D-0B) |
| Slides | [fatiando.org/agu2021](https://www.fatiando.org/agu2021) |

The presentation is centered around a tutorial that walks you through the steps
of transforming observed absolute gravity measurements into a grid of residual
gravity disturbances at a constant height.
The tutorial showcases some of the core utilities of all of our open-source
libraries:

1. Fetch and cache the data using [Pooch](https://github.com/fatiando/pooch)
1. Calculate the gravity disturbance using [Boule](https://github.com/fatiando/boule)
1. Interpolate data and apply map projections to grids using [Verde](https://github.com/fatiando/verde)
1. Perform topographic correction and equivalent-source interpolation using [Harmonica](https://github.com/fatiando/harmonica)

💻 Access the tutorial and **run it online** at: https://github.com/fatiando/tutorials

The slides are for a 5-minute lightning talk.

![Screenshot of our poster](https://github.com/fatiando/agu2021/raw/main/poster.png)

## Abstract

The Fatiando a Terra project (https://www.fatiando.org) was started in 2010
as a Python library for visualization, forward modelling, and inversion across
different geophysical methods.
Over the following 8 years, the project attracted new contributors and grew to
include cutting-edge methods, toy examples for teaching, and helper functions
for visualization.
Standards around testing, documentation, and code style evolved and new tools
appeared around the ecosystem (such as SimPEG, PyVista, Devito, and pyGIMLi),
making some of our functionality redundant and outdated.

In an attempt to better interface with the emerging ecosystem, we started a
major restructuring of the code base in 2018.
Our goals were to:

1. Split the project into several software packages, each with a narrow and
   well-defined scope. This change would allow contributors to focus on the
   parts of the project that they care about the most. It would also be crucial
   to establish our niche in the current geophysics OSS landscape.
2. Set high standards for documentation and test coverage. We aim for full test
   coverage of the code and comprehensive API and narrative documentation,
   which would be enforced through automated checks and code review.
3. Carefully design of our APIs (application programming interfaces) and focus
   on meeting real-world use cases. Our approach is to design and thoroughly
   discuss the code interfaces by creating examples of usage before writing the
   actual implementation.
4. Connect and nurture our community. The project developer pool has always
   been small and it would take constant deliberate effort to foster a
   community that is willing to take ownership of the project.

The project is currently composed of the following packages:

* Pooch: download and cache data files for research projects and documentation
  sample data.
* Verde: machine-learning inspired point-cloud data processing and
  interpolation.
* Harmonica: gravity and magnetic data processing, forward modelling, and
  inversion.
* Boule: reference ellipsoids and normal gravity calculations.
* RockHound: a collection of open-access datasets for use in documentation and
  tutorials.

This presentation will cover the current available functionality and some of
the lessons learned from developing, growing, and maintaining the project,
including current challenges and our future plans.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img
alt="Creative Commons License" style="border-width:0"
src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br>
This content is licensed under a <a rel="license"
href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution
4.0 International License</a>.
