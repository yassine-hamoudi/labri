  {% capture speaker %}{{ event.summary | replace_regex: "^\[([^\]]+)\]", "" | replace_regex: "(\(.*|\..*)", "" }}{% endcapture %}
  {% capture affiliation %}{{ event.summary | replace_regex: "^([^\(]+)\(", "" | replace_regex: "\).*", "" }}{% endcapture %}
  {% capture title %}{{ event.summary | replace_regex: "^([^\)]+)\)\s*", "" }}{% endcapture %}
  {% if title == ""%}
    {%assign title = "TBA"%}
  {% endif %}
