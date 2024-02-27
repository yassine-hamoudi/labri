---
title: "Seminar"
layout: default
sitemap: false
permalink: /seminar/
---

[![email]({{ site.url }}{{ site.baseurl }}/images/logo/email.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Subscribe to the mailing list**](https://diff.u-bordeaux.fr/sympa/info/labri.gt-info-quantique) &nbsp;&nbsp;
[![calendar]({{ site.url }}{{ site.baseurl }}/images/logo/calendar.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Subscribe to iCalendar**]({{ site.url }}{{ site.baseurl }}/files/calendar.ics) &nbsp;&nbsp;
[![zoom]({{ site.url }}{{ site.baseurl }}/images/logo/zoom.png){: style="vertical-align:middle; max-width: 40px; height: auto;"}**&nbsp;&nbsp; Watch on Zoom**](https://u-bordeaux-fr.zoom.us/j/89861302375?pwd=UW03M05sZzZ0cWFUT3lwNC92b1Y1Zz09)

#### The seminar takes place on Tuesdays from 15:00 to 16:00 CET. It is located at [LaBRI]({% link _pages/contact.md %}), either on ground floor (rooms 073, 076, amphi) or first floor (room 178). The talks are usually in english and broadcasted on [Zoom](https://u-bordeaux-fr.zoom.us/j/89861302375?pwd=UW03M05sZzZ0cWFUT3lwNC92b1Y1Zz09).
<br>

{% capture nowDay %}{{'now' | date:  "%Y%m%d"}}{% endcapture %}

# Upcoming talks

{% ical url: https://webmel.u-bordeaux.fr/home/bf-labri.ca@u-bordeaux.fr/gt.info-quantique.ics after_date:01-01-2024  %}
  {% capture talkDay %}{{event.start_time | date: "%Y%m%d"}}{% endcapture %}
  {% if talkDay >= nowDay %}
    {% include parse_ics.md %}
<details markdown=block>
  <summary markdown=span>
    {% if event.location %}{{ event.start_time | date_to_long_string: "ordinal" }} at {{ event.start_time | date: "%H:%M" }} ({{ event.location }})<br>
      <b>{{ speaker }} </b> ({{ affiliation }}) <i>{{ title }}</i> &#9432;
    {% else %}{{ event.start_time | date_to_long_string: "ordinal" }} at {{ event.start_time | date: "%H:%M" }} <br>
      <b>{{ speaker }} </b> ({{ affiliation }}) <i>{{ title }}</i> &#9432;{% endif %}
  </summary>
   <blockquote><p> {{ event.description }} </p></blockquote>
</details>
<p></p>
  {% endif %}
{% endical %}

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
