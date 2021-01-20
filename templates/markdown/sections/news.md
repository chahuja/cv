{% extends "section.md" %}

{% block body %}
<table class="table table-hover">
{% for i in items[:5] %}
<tr>
  <td class='col-md-3'>{{ i.date }}</td>
  <td>{{ i.info }}</td>
</tr>
{% endfor %}
</table>

{% if items|length > 5 %}
<button type="button" class="btn btn-info" data-toggle="collapse" data-target="#demo" onclick="change()" id="more">More</button>
<div id="demo" class="collapse">
<table class="table table-hover">
  {% for i in items[5:] %}
      <tr>
	    <td class='col-md-3'>{{ i.date }}</td>
	    <td>{{ i.info }}</td>
	  </tr>	  
  {% endfor %}
</table>
</div>
{% endif %}

{% endblock body %}
