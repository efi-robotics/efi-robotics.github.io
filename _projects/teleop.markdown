---
layout: distill
title: Teleoperation
description: 
img: assets/img/teleop.png
importance: 3
category: themes
bibliography: papers.bib
date: 2022-10-15
authors:
  - name: See references list
    affiliations:
      name: See references list
---

## Bilateral teleoperation with haptic feedback for minimally invasive surgery.

### Abstract

A desktop haptic device is used to teleoperate an industrial redundant and compliant robotic arm with a surgical instrument mounted on its end-effector. The master and slave devices are coupled in a bilateral position-position architecture. Force feedback is provided by the master haptic device to the user, from the position of the slave’s wrist. A surgical task (palpation) that involves force feedback is presented and tested in a user study with surgeons and non-medical participants. Results show that users easily discern between three different materials during palpation given minimal familiarisation time. Active constraint enforcement is also integrated with the system as a sensitive area around the palpation samples which the slave instrument is prohibited to enter <d-cite key="Psomopoulou2020"></d-cite>.

### Key points

* A position-position control architecture is utilised to provide force feedback where both robots are controlled to track each other’s TCP.
* Substantially different master and slave robots (in terms of size and dynamics).
* Palpation of Soft Tissue-Like Materials.
* Application of Active Constraints Enforcement.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AC_rviz.png" title="SMG" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AC_slave.jpg" title="SMG" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AC_slave_focus.jpg" title="SMG" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Slave arm (KUKA iiwa) touching a virtual surface (left) and real soft silicon materials (right).
</div>

### Video 

<iframe width="560" height="315" src="https://www.youtube.com/embed/ivSKAxDJ7S8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Project scope

This work was part of the [SMARTsurg project](https://www.smartsurg-project.eu/). Other publications include: <d-cite key="Abeywardena2020,Sani2020,Abeywardena2019,Sayyaddelshad2018,Tzemanaki2018"></d-cite>.