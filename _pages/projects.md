---
permalink: /
classes: wide
layout: splash
---
<div class="bg-gray">
  <div class="flex">
    <div>
      <h1 class="font-header-xxl">The Science Workshop is an active development space for learning and sharing ideas.</h1>

      <p class="font-body-m">
        Our hope is to share work-in-progress projects from members of the CZI science team, including early stage designs and prototypes, training materials, past webinars, and more. The featured projects on this page are not an exhaustive list of our work.
        These projects are interactive! Feel free to share feedback with our team about any of these featured projects. Folks are encouraged to make pull requests, add comments, and reach out to our team with any questions.
      </p>
    </div>
    <img class="flask-svg" src="{{ "assets/images/science-worshop-banner-img.svg" | relative_url }}" />
  </div>
  <div>
    <div>General questions? Email ghaliburton@chanzuckerberg.com.</div>
    <div>Questions about projects or work areas? You can find contact information on each specific project page.</div>
  </div>
</div>

<div class="warning font-body-l">
  <img class="icon-large" src="{{ "assets/images/exclamation.svg" | relative_url }}">
  The projects in the Science Workshop may not be currently maintained and may break or disappear without notice!
</div>

<span class="font-body-m">Jump to Category:</span>
<a class="category-link font-body-m" href="#papers">Papers</a>
<a class="category-link font-body-m" href="#tools">Tools</a>
<a class="category-link font-body-m" href="#trainings">Trainings</a>
<a class="category-link font-body-m" href="#other">Other</a>

<!-- Papers project details from _data/projects.yml -->
{% if site.data.papers %}
  <div id="papers" class="font-header-xl">Papers</div>
  <div class="card-container">
    {% for project in site.data.papers %}
      {% include project_card.html project=project%}
    {% endfor %}
  </div>
{% endif %}

<!-- Tools project details from _data/tools.yml -->
{% if site.data.tools %}
  <div id="tools" class="font-header-xl">Tools</div>
  <div class="card-container">
    {% for project in site.data.tools %}
      {% include project_card.html project=project%}
    {% endfor %}
  </div>
{% endif %}

<!-- Trainings project details from _data/trainings.yml -->
{% if site.data.trainings %}
  <div id="trainings" class="font-header-xl">Trainings</div>
  <div class="card-container">
    {% for project in site.data.trainings %}
      {% include project_card.html project=project%}
    {% endfor %}
  </div>
{% endif %}

<!-- Other project details from _data/other.yml -->
{% if site.data.other %}
  <div id="other" class="font-header-xl">Other</div>
  <div class="card-container">
    {% for project in site.data.other %}
      {% include project_card.html project=project%}
    {% endfor %}
  </div>
{% endif %}
