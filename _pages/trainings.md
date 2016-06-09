---
layout: splash  
permalink: /trainings/
title: "<br /> <br /> <br />Software Trainings"
excerpt: "High quality hands-on training on different language and frameworks <br /> <br /> <br />"
header:
  overlay_color: "#5e616c"
  overlay_image: splash/unsplash-16.jpeg
  cta_label: "<i class='fa fa-phone' aria-hidden='true'></i> Contact"
  cta_url: "../contact/"
  caption: "Photo credit: [*Unsplash*](https://unsplash.com)"
author_profile: false
quote:
  - excerpt: '> Learning Without Thought Is Labor Lost. Thought Without Learning Is Intellectual Death.
              <br />  - [Confucius](https://en.wikipedia.org/wiki/Confucius)'
end:
  - excerpt: ''
---
{% include base_path %}
{% include feature_row id="quote" type="center" %}

# Overview

The space of software design and development, has always required well versed and skilled man-power.
Master the skills, with high quality, hands-on trainings with the industry experts and build a better world.
{% include feature_row id="end" type="center"%}
## Programming Language

We provide trainings in different programming languages. Please find the courses listed below:

<div class="grid__wrapper">
  {% for post in site.train-language %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>


{% include feature_row id="end" type="center"%}

## Application Frameworks

Make the most out of the different frameworks and libraries with our specially designed courses on different application frameworks and libraries.

<div class="grid__wrapper">
  {% for post in site.train-framework %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

{% include feature_row id="end" type="center"%}

## Test Driven Development

Learn the nuances of building high quality and robust application with the TDD courses.

<div class="grid__wrapper">
  {% for post in site.train-tdd %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

{% include feature_row id="end" type="center"%}

## Build Tools

Build tools are an important part of the development cycle. They are a great productivity boost, when used properly.
update to the most sought after build tools:

<div class="grid__wrapper">
  {% for post in site.train-tools %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>

{% include feature_row id="end" type="center"%}
