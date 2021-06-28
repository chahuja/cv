{% extends "section.md" %}

{% block body %}
<table class="table table-hover">
{% for item in items %}
<tr>
  <td>
    {% if item.url %}
        <b><a href="{{ item.url }}">{{ item.title }}</a></b>
    {% else %}
        <b>{{ item.title }}</b>
	{% endif %}
	{% if item.location %}	
      <br> {{ item.location }}
	{% endif %}
  </td>
  <td class='col-md-2' style='text-align:right;'>{{ item.year }}</td>
</tr>
{% endfor %}
</table>
{% endblock body %}
