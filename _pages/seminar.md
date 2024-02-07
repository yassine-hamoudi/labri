---
title: "Seminar"
layout: default
sitemap: false
permalink: /seminar/
---

[![email]({{ site.url }}{{ site.baseurl }}/images/logo/email.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Subscribe to the mailing list**](https://diff.u-bordeaux.fr/sympa/info/labri.gt-info-quantique) &nbsp;&nbsp;
[![calendar]({{ site.url }}{{ site.baseurl }}/images/logo/calendar.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Subscribe to iCalendar**]({{ site.url }}{{ site.baseurl }}/files/calendar.ics) &nbsp;&nbsp;
[![zoom]({{ site.url }}{{ site.baseurl }}/images/logo/zoom.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Watch on Zoom**](https://u-bordeaux-fr.zoom.us/j/89861302375?pwd=UW03M05sZzZ0cWFUT3lwNC92b1Y1Zz09)


#### The seminar takes place on Tuesdays from 15:00 to 16:00 CET. It is located at [LaBRI]({{ site.url }}{{ site.baseurl }}/contact), either on ground floor (rooms 073, 076, amphi) or first floor (room 178). The talks are usually in english and broadcasted on [Zoom](https://u-bordeaux-fr.zoom.us/j/89861302375?pwd=UW03M05sZzZ0cWFUT3lwNC92b1Y1Zz09). For questions, you can reach [Yvan Le Borgne](mailto:borgne@labri.fr).
<br>

{% capture nowDay %}{{'now' | date: '%s'}}{% endcapture %}

# Upcoming talks

{% for talk in site.data.seminar %}
  {% capture talkDay %}{{talk.day | date: '%s'}}{% endcapture %}
  {% if talkDay >= nowDay %}
<details markdown=block>
  <summary markdown=span>
    {{ talk.day | date_to_long_string: "ordinal" }} at {{ talk.time}} (Room {{ talk.room }})<br>
    <b>{{ talk.speaker }} </b> ({{ talk.affiliation }}) <i>{{ talk.title }}</i> &#9432;
  </summary>
   {{ talk.abstract }}
</details>
<p></p>
  {% endif %}
{% endfor %}

<br>
# Past talks

### 2024

{% assign year = '2024' %}
{% include print_past_seminars.md %}

### 2023

{% assign year = '2023' %}
{% include print_past_seminars.md %}

### [Older events](https://combalgo.labri.fr/pmwiki.php/Groupe/Info-Quantique)

<br>
