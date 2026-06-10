---
layout: post
title: dexterous manipulation
description:  contact-rich grasping, pinching, and in-hand interaction
img: assets/img/pick-sampleorange.svg
importance: 1
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
#     - name: Stable robotic grasping
#       subsections:
#         - name: Videos
---

We study how stable dexterous behaviour emerges from regulating contact geometry, rolling mechanics, force direction, and tactile feedback. This theme spans grasping, pinching, and in-hand manipulation, from early control laws for stable contact to recent tactile and sim-to-real methods for contact-rich robot learning.

### why this matters now
- contact-rich manipulation remains one of the central challenges in dexterous robotics.
- tactile feedback and structured priors are increasingly important for robust manipulation under uncertainty.
- physically grounded contact control can provide useful low-level structure for learned policies.


### selected related work
- **a robust controller for stable 3d pinching using tactile sensing** — tactile estimation of local contact orientation for stable grasping of unknown objects. {% cite Psomopoulou2021 %}
- **stable pinching by controlling finger relative orientation of robotic fingers with rolling soft tips** — rolling contact and relative finger orientation as task-relevant structure for stable pinch grasping. {% cite Psomopoulou2018 %}
- **a controller for stable grasping and desired finger shaping without contact sensing** — early evidence that interaction geometry can simplify sensory requirements. {% cite Grammatikopoulou2014 %}
- **tactile-driven gentle grasping for human-robot collaborative tasks** — tactile multi-finger feedback for stable and gentle grasping with an underactuated hand. {% cite 10161036tactile %}
- **shear-based grasp control for multifingered underactuated tactile robotic hands** — tactile grasp control for manipulation with underactuated robot hands. {% cite 10972061tro %}
- **anyrotate: gravity-invariant in-hand object rotation with sim-to-real touch** — a bridge from tactile control to learned in-hand manipulation with sim-to-real transfer. {% cite yang2024anyrotate %}


### where this is going
we now use these ideas as structure for robot learning: as contact-centric state representations, stabilisation priors, and tactile policy components for contact-rich manipulation.


---


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pinching.png" title="SMG" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2d_grasping.png" title="Kyushu" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Images of the implementation of the developed grasping controller on the Shadow Modular Grasper (left {% cite Psomopoulou2021 %}) and a prototype robotic hand (right {% cite Psomopoulou2018 %}).
</div>

### videos

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">
            {% include video.liquid path="https://www.youtube.com/embed/rfQesw3FDA4" style="min-width:280px; min-height:157px;" class="embed-responsive-item" %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="embed-responsive embed-responsive-16by9">
            {% include video.liquid path="https://www.youtube.com/embed/A6WuCj2WzzM" style="min-width:280px; min-height:157px;" class="embed-responsive-item" %}
        </div>
    </div>
</div>
---
