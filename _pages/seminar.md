---
title: "Seminar"
layout: gridlay
excerpt: "Allan Lab at Leiden University."
sitemap: false
permalink: /seminar/
---

[![emaim](/images/logo/email.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**Subscribe to the mailing list**](https://diff.u-bordeaux.fr/sympa/info/labri.gt-info-quantique)

[![calendar](/images/logo/calendar.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**Subscribe to iCalendar**](/files/calendar.ics)

#### The seminar takes place on Tuesdays from 15:00 to 16:00 CET. It is located at [LaBRI]({{site.baseurl}}/contact), either on ground floor (rooms 073, 076, amphi) or first floor (room 178). The talks are in english and broadcasted on Zoom, upon agreement of the speaker. For questions, you can reach [Yvan Le Borgne](mailto:borgne@labri.fr) or [Yassine Hamoudi](mailto:yassine.hamoudi@labri.fr).
<br>

{% capture nowDay %}{{'now' | date: '%s'}}{% endcapture %}

# Upcoming talks

{% for talk in site.data.seminar %}
  {% capture talkDay %}{{talk.day | date: '%s'}}{% endcapture %}
  {% if talkDay >= nowDay %}
<details markdown=block>
  <summary markdown=span>
    {{ talk.day | date_to_long_string: "ordinal" }} at {{ talk.time}} (Room {{ talk.room }}, Zoom link)<br>
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
