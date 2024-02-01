
{% for talk in site.data.seminar %}
  {% capture talkDay %}{{talk.day | date: '%s'}}{% endcapture %}
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
