---
layout: default-plus
title: Research
feed-in-sidebar: true
---


<h1>Research</h1>

<div class="research-cont">

<h4>Preprints</h4>

<ol class="references">
  {% for item in site.data.research.preprints %}
  <li>
    {{ item.authors }} (<span class="reference-year">{{ item.year }}</span>). {{ item.title }}.
    <i>{{ item.venue }}</i>{% if item.arxiv %} arXiv:{{ item.arxiv }}.{% endif %}
    {% if item.link %}<a href="{{ item.link }}">{{ item.link_text | default: "Link" }}</a>{% endif %}
    {% if item.abstract %}
    <details class="reference-abstract">
      <summary>Abstract</summary>
      <div class="reference-abstract-body">
        {% include abstract.html abstract=item.abstract %}
      </div>
    </details>
    {% endif %}
  </li>
  {% endfor %}
</ol>

<h4>Publications</h4>

<ol class="references">
  {% for item in site.data.research.publications %}
  <li>
    {{ item.authors }} (<span class="reference-year">{{ item.year }}</span>). {{ item.title }}.
    <i>{{ item.venue }}</i>
    {% if item.link %}<a href="{{ item.link }}">{{ item.link_text | default: "Link" }}</a>{% endif %}
    {% if item.abstract %}
    <details class="reference-abstract">
      <summary>Abstract</summary>
      <div class="reference-abstract-body">
        {% include abstract.html abstract=item.abstract %}
      </div>
    </details>
    {% endif %}
  </li>
  {% endfor %}
</ol>

<h4>Thesis</h4>

<ul>
  <li>
    Find my PhD thesis, titled <i>{{ site.data.research.thesis.title }}</i>, at
    <a href="{{ site.baseurl }}{{ site.data.research.thesis.link }}">{{ site.data.research.thesis.link_text }}</a>.
  </li>
</ul>

<h4>Talks</h4>

<ol class="references">
  {% for talk in site.data.research.talks %}
  <li>
    {{ talk.venue }} ({% if talk.upcoming %}Upcoming, <span class="reference-year">{{ talk.date }}</span>{% else %}<span class="reference-year">{{ talk.date }}</span>{% endif %}) -
    <i>{{ talk.title }}</i>
  </li>
  {% endfor %}
</ol>

<h4>Misc.</h4>

<ul>
  {% for item in site.data.research.misc %}
  <li>
    {{ item.text }} <a href="{{ item.link }}">{{ item.link_text }}</a>{{ item.suffix }}
  </li>
  {% endfor %}
</ul>

 </div>
