---
title: "Members"
layout: gridlay
sitemap: false
permalink: /members/
---

<!-- # Group Members -->

#### **Our group has several [open positions]({% link _pages/positions.md %}) available.**

<!-- ## Group Leaders
{% assign typeMember = 'leader' %}
{% include print_faculty.md %} -->

## Faculty Members
{% assign typeMember = "faculty" %}
{% include print_faculty.md %}

## Postdocs
{% assign typeMember = 'postdoc' %}
{% include print_postdoc.md %}

## Students
{% assign typeMember = 'student' %}
{% include print_student.md %}

## Local Collaborators
<div class="row">

<div class="col-sm-3 clearfix">
<h4>LaBRI</h4>
{% for member in site.data.collaborators %}
{% if member.location == "LaBRI" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
<h4>Institut de Mathématiques de Bordeaux</h4>
{% for member in site.data.collaborators %}
{% if member.location == "IMB" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
<h4>Laboratoire Ondes et Matière d'Aquitaine</h4>
{% for member in site.data.collaborators %}
{% if member.location == "LOMA" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
<h4>IBM Quantum France</h4>
{% for member in site.data.collaborators %}
{% if member.location == "IBM" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>
</div>

## Former Members
<div class="row">

<div class="col-sm-5 clearfix">
<h4>Undergraduate and Master Students</h4>
{% for member in site.data.former_members %}
{% if member.type == "student"%}
  {{ member.name }}, {{ member.start_date | date:"%B %Y" }} - {{ member.end_date | date:"%B %Y" }}
{% endif %}
{% endfor %}
</div>

<!-- <div class="col-sm-4 clearfix">
<h4>PhD students</h4>
{% for member in site.data.former_members %}
{% if member.type == "phd" %}
  {{ member.name }}, {{ member.time }}
{% endif %}
{% endfor %}
</div> -->

<div class="col-sm-4 clearfix">
<h4>Postdocs</h4>
{% for member in site.data.former_members %}
{% if member.type == "postdoc" %}
  {{ member.name }}, {{ member.start_date | date:"%B %Y" }} - {{ member.end_date | date:"%B %Y" }}
{% endif %}
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
<h4>Faculty</h4>
{% for member in site.data.former_members %}
{% if member.type == "faculty" %}
  {{ member.name }}
{% endif %}
{% endfor %}
</div>

</div>
