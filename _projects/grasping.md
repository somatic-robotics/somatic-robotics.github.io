---
layout: post
title: Grasping
description:  
img: assets/img/grasping.png
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

## Stable robotic grasping {% cite Psomopoulou2021 Psomopoulou2018 Grammatikopoulou2014 %}
---

* Non model-based torque controller using passivity theory for stability analysis.
* Deep learning using convolutional neural networks on images from an optical tactile sensor (the TacTip, developed in Bristol Robotics Laboratory).
* Implementation on two different fully actuated robotic hands.

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

### Videos

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

