  {% capture speaker %}{{ event.summary | replace_regex: "^\[([^\]]+)\]\s*", "" | replace_regex: "\s*(\(.*|\..*)", "" }}{% endcapture %}
  {% capture affiliation %}{{ event.summary | replace_regex: "^([^\(]+)", "" | replace_regex: "\).*", ")" }}{% endcapture %}
  {% capture title %}{{ event.summary | replace_regex: "^([^\)]+)", "" | replace_regex: "^\)\s*", ""}}{% endcapture %}
  {% capture abstract %}{{ event.description }}{% endcapture %}
  {% if abstract == ""%}
    {%assign abstract = "To Be Announced"%}
  {% endif %}
 