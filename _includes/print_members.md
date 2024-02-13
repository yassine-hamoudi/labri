{% assign number_printed = 0 %}
{% for member in site.data.permanent_members %}
{% if member.type == typeMember %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}</i><br>
  {% if typeMember == "leader" %}
  <a href="{{ member.website }}">Website</a>&nbsp;&nbsp;&nbsp;<a href="{{ member.publications }}">Publications</a>&nbsp;&nbsp;&nbsp;<a href="mailto:{{ member.email }}">Email</a>
  {% else %}
  <a href="{{ member.website }}">Website</a>&nbsp;&nbsp;&nbsp;<a href="mailto:{{ member.email }}">Email</a>
  {% endif %}

  {% if member.number_fields <> 0 %}
  <ul style="margin-top:-25px;padding:16px;overflow: hidden">

  {% if member.number_fields == 1 %}
  <li> {{ member.field1 }} </li>
  {% endif %}

  {% if member.number_fields == 2 %}
  <li> {{ member.field1}} </li>
  <li> {{ member.field2}} </li>
  {% endif %}

  {% if member.number_fields == 3 %}
  <li> {{ member.field1 }} </li>
  <li> {{ member.field2 }} </li>
  <li> {{ member.field3 }} </li>
  {% endif %}

  {% if member.number_fields == 4 %}
  <li> {{ member.field1 }} </li>
  <li> {{ member.field2 }} </li>
  <li> {{ member.field3 }} </li>
  <li> {{ member.field4 }} </li>
  {% endif %}

  {% if member.number_fields == 5 %}
  <li> {{ member.field1 }} </li>
  <li> {{ member.field2 }} </li>
  <li> {{ member.field3 }} </li>
  <li> {{ member.field4 }} </li>
  <li> {{ member.field5 }} </li>
  {% endif %}

  </ul>
    {% endif %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% endfor %}


{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
