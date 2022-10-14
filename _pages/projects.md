---
permalink: /
classes: wide
layout: splash
---
<div class="sw-header bg-gray">
  <div class="content flex">
    <div>
      <h1 class="font-header-xxl">
        The Science Workshop is an active development space for learning, sharing, and iteration.
      </h1>

      <p class="font-body-m">
        Our hope is to share work-in-progress projects from members of the CZI science team, including early stage designs and prototypes, training materials, past webinars, and more. The featured projects on this page are not an exhaustive list of our work.
      </p>
      <p class="font-body-m">
        These projects are interactive! Feel free to share feedback with our team about any of these featured projects. Folks are encouraged to make pull requests, add comments, and reach out to our team with any questions.
      </p>
      <div class="font-body-s">
        <b>General questions?</b>
        Email <a href="mailto:ghaliburton@chanzuckerberg.com">ghaliburton@chanzuckerberg.com</a>.
      </div>
      <div class="font-body-s">
        <b>Questions about projects or work areas?</b>
        You can find contact information on each specific project page.
      </div>
    </div>
    <img class="flask-svg" src="{{ 'assets/images/science-worshop-banner-img.svg' | relative_url }}" />
  </div>
</div>

<div class="content">
  <div class="warning font-body-l">
    <img class="icon-large" src="{{ 'assets/images/exclamation.svg' | relative_url }}">
    The projects in the Science Workshop may not be currently maintained and may break or disappear without notice!
  </div>

  <div class="jump-menu">
    <span class="font-body-m">Jump to Category:</span>
    {% if site.data.papers %}
      <a class="category-link font-body-m" href="#papers">Papers</a>
    {% endif %}
    {% if site.data.tools %}
      <a class="category-link font-body-m" href="#tools">Tools</a>
    {% endif %}
    {% if site.data.trainings %}
      <a class="category-link font-body-m" href="#trainings">Trainings</a>
    {% endif %}
    {% if site.data.other %}
      <a class="category-link font-body-m" href="#other">Other</a>
    {% endif %}
  </div>

  <!-- Papers project details from _data/projects.yml -->
  {% if site.data.papers %}
    <div id="papers" class="font-header-xl">Papers</div>
    <div class="card-container">
      {% assign sorted = site.data.papers | sort_natural: "title" %}
      {% for project in sorted %}
        {% include project_card.html project=project%}
      {% endfor %}
    </div>
  {% endif %}

  <!-- Tools project details from _data/tools.yml -->
  {% if site.data.tools %}
    <div id="tools" class="font-header-xl">Tools</div>
    <div class="card-container">
      {% assign sorted = site.data.tools | sort_natural: "title" %}
      {% for project in sorted %}
        {% include project_card.html project=project%}
      {% endfor %}
    </div>
  {% endif %}

  <!-- Trainings project details from _data/trainings.yml -->
  {% if site.data.trainings %}
    <div id="trainings" class="font-header-xl">Trainings</div>
    <div class="card-container">
      {% assign sorted = site.data.trainings | sort_natural: "title" %}
      {% for project in sorted %}
        {% include project_card.html project=project%}
      {% endfor %}
    </div>
  {% endif %}

  <!-- Other project details from _data/other.yml -->
  {% if site.data.other %}
    <div id="other" class="font-header-xl">Other</div>
    <div class="card-container">
      {% assign sorted = site.data.other | sort_natural: "title" %}
      {% for project in sorted %}
        {% include project_card.html project=project%}
      {% endfor %}
    </div>
  {% endif %}
</div>
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap"
  rel="stylesheet"
/>