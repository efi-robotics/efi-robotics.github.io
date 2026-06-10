---
layout: post
title: shared interaction
description: handovers, bilateral teleoperation, and human-guided manipulation
img: assets/img/robot-armorange.svg
importance: 2
category: research themes
bibliography: distill.bib
date: 2022-10-15
related_posts: false
toc:
  sidebar: left
related_publications: true

# authors:
#   - name: See references list
#     affiliations:
#       name: See references list
# toc:
#     - name: Human-to-robot object handovers
#       subsections:
#       - name: Video
---

We study how robots exchange forces, objects, and intent with humans through physical interaction. This theme spans handovers, haptic collaboration, and teleoperation, from early work on load transfer and human-like haptic interaction to more recent systems for shared manipulation and force-aware teleoperation.

### why this matters now

- physical collaboration requires more than trajectory tracking: robots must manage contact transitions, load exchange, and human intent.
- haptic feedback and local interaction cues are crucial for safe, fluent shared manipulation.
- cooperative interaction provides an important setting for structured and embodied policy design.


### selected related work
- **a robot hand-over control scheme for human-like haptic interaction** — foundational work on haptic interaction during object transfer under uncertainty. {% cite Psomopoulou2014 %}.
- **a human inspired stable object load transfer for robots in hand-over tasks** — stable grasping and receiver-initiated load transfer based on local sensing. {% cite Psomopoulou2015 %}
- **human-inspired object load transfer in hand-over tasks** — early formulation of coordinated object transfer through haptic interaction. {% cite Psomopoulou2015b %}.
- **a human inspired handover policy using gaussian mixture models and haptic cues** — demonstration-based approach for fluent handover with haptic release cues. {% cite Sidiropoulos2019 %}
- **evaluation of force feedback for palpation and application of active constraints on a teleoperated system** — teleoperation and human-guided instrument control. {% cite Psomopoulou2020 %}
- **towards finger motion tracking and analyses for cardiac surgery** — human motion analysis and teleoperation-related surgical interaction. {% cite Sani2020 %}


### where this is going

we now see these ideas as foundations for shared-contact adaptation, human-guided manipulation, and interaction policies that combine haptic structure with learning and assistance.

---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/handover_sim.png" class="img-fluid rounded z-depth-1" %}
   </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/handover_real.png" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/handbottle.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Simulation (in V-REP) and experiments of an object handover.
</div>


---


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
    Follower arm (KUKA iiwa) touching a virtual surface (left) and real soft silicon materials (right).
</div>

### videos 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">
            {% include video.liquid path="https://www.youtube.com/embed/ivSKAxDJ7S8" style="min-width:280px; min-height:157px;" class="embed-responsive-item" %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">

        </div>
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">
            {% include video.liquid path="https://www.youtube.com/embed/eWn1Kby0mK8" style="min-width:280px; min-height:157px;" class="embed-responsive-item" %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">

        </div>
    </div>
</div>
---

