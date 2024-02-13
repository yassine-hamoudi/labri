
{% assign sorted = site.data.seminar | sort: 'day' | reverse %}
{% for talk in sorted %}
  {% capture talkDay %}{{talk.day | date: "%Y%m%d"}}{% endcapture %}
  {% assign talkYear = talk.day | date: "%Y" %}
  {% if talkDay < nowDay and talkYear == year%}
<details markdown=block>
  <summary markdown=span>
    {{ talk.day | date_to_long_string: "ordinal" }}<br>
    <b>{{ talk.speaker }} </b> ({{ talk.affiliation }}) <i>{{ talk.title }}</i> &#9432;
  </summary>
   > {{ talk.abstract }}
</details>
<p></p>
{% endif %}
{% endfor %}
