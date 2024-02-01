---
title: "Members"
layout: gridlay
sitemap: false
permalink: /members/
---

# Group Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see open positions)]({{ site.url }}{{ site.baseurl }}/positions) **!**

## Principal Investigators
{% assign typeMember = 'principal' %}
{% include print_members.md %}

## Co-Investigators
{% assign typeMember = 'coinvest' %}
{% include print_members.md %}

## Students
{% assign typeMember = 'student' %}
{% include print_members.md %}

## Local Collaborators
<div class="row">

<div class="col-sm-6 clearfix">
<h4>Institut de Mathématiques de Bordeaux</h4>
{% for member in site.data.collaborators %}
{% if member.location == "IMB" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>

<div class="col-sm-6 clearfix">
<h4>IBM Quantum France</h4>
{% for member in site.data.collaborators %}
{% if member.location == "IBM" %}
<a href="{{ member.website }}">{{ member.name }}</a>
{% endif %}
{% endfor %}
</div>
</div>

## Former members
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Bachelor and Master Students</h4>
{% for member in site.data.former_members %}
{% if member.type == "bachelor" %}
  {{ member.name }}, {{ member.time }}
{% endif %}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>PhD students</h4>
{% for member in site.data.former_members %}
{% if member.type == "phd" %}
  {{ member.name }}, {{ member.time }}
{% endif %}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Postdocs</h4>
{% for member in site.data.former_members %}
{% if member.type == "postdoc" %}
  {{ member.name }}, {{ member.time }}
{% endif %}
{% endfor %}
</div>

</div>

<br>