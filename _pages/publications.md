---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  You can find most of my articles on <u><a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% if post.pubtype == 'review' %}
      <h2>Preprints</h2>
      <ul>
      {% for post in site.publications reversed %}
          {% if post.pubtype == 'review' %}
              {% include archive-single.html %}
          {% endif %}
      {% endfor %}
      </ul>
      {% break %}
  {% endif %}
{% endfor %}

<h2>Journal Articles</h2>
<ul>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'journal' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}
</ul>

<h2>Conference Papers</h2>
<ul>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'conference' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}
</ul>

<h2>Dissertation</h2>
<ul>
{% for post in site.publications reversed %}
  {% if post.pubtype == 'dissertation' %}
      {% include archive-single.html %}
  {% endif %}
{% endfor %}
</ul>

<sup>*</sup> indicates equal authorship.

