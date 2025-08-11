---
layout: single
permalink: /cv/
title: "Curriculum Vitae"
author_profile: true
---

{% for section in site.data.cv %}
{% assign section_name = section[0] %}
{% assign section_items = section[1] %}

<div class="cv-section" style="margin-bottom: 2em;">

  <h2 style="border-bottom: 1px solid #e5e5e5; padding-bottom: 0.5em;">{{ section_name | capitalize }}</h2>

  {% for item in section_items %}
    <div style="margin-bottom: 1.5em; page-break-inside: avoid;">
      {% if item.position %}
        <h3 style="margin-bottom: 0.2em; font-size: 1.1em;"><b>{{ item.position }}</b></h3>
        <p class="page__meta" style="margin: 0;">{{ item.company }} | {{ item.year }}</p>
      {% elsif item.degree %}
        <h3 style="margin-bottom: 0.2em; font-size: 1.1em;"><b>{{ item.degree }}</b></h3>
        <p class="page__meta" style="margin: 0;">{{ item.uni }} | {{ item.year }}</p>
      {% else %}
         <h3 style="margin-bottom: 0.2em; font-size: 1.1em;"><b>{{ item.title }}</b></h3>
         <p class="page__meta" style="margin: 0;">{{ item.comment }} | {{ item.year }}</p>
      {% endif %}
      
      {% if item.summary %}
        <p style="margin-top: 0.5em;">{{ item.summary | markdownify }}</p>
      {% elsif item.details %}
        <p style="margin-top: 0.5em;">{{ item.details | markdownify }}</p>
      {% endif %}
    </div>
  {% endfor %}

</div>

{% endfor %}

<div class="cv-section" style="margin-bottom: 2em;">
  <h2 style="border-bottom: 1px solid #e5e5e5; padding-bottom: 0.5em;">{{ "Publications" | capitalize }}</h2>
</div>
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
<div class="cv-section" style="margin-bottom: 2em;">
  <h2 style="border-bottom: 1px solid #e5e5e5; padding-bottom: 0.5em;">{{ "Talks" | capitalize }}</h2>
</div>
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
<div class="cv-section" style="margin-bottom: 2em;">
  <h2 style="border-bottom: 1px solid #e5e5e5; padding-bottom: 0.5em;">{{ "Teaching" | capitalize }}</h2>
</div>
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

<div class="cv-section" style="margin-bottom: 2em;">
  <h2 style="border-bottom: 1px solid #e5e5e5; padding-bottom: 0.5em;">{{ "Awards" | capitalize }}</h2>
</div>
  * <b>2025</b> EuroTech Visiting Researcher (EPFL)
  * <b>2024</b> Summa cum laude - PhD thesis
  * <b>2015</b> Award from the President of BiH for the most successful university students
  * <b>2015</b> Gold Medal (Valedictorian) at the University of Tuzla
  * <b>2012–2014</b> Scholarship of Fund “Bosniaks” for talented students
  * <b>2011</b> Valedictorian of the High School (Bosnia)
  * <b>2011</b> Honourable Mention – 42nd International Physics Olympiad IPhO (Bangkok)
  
