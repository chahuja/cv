{% extends "section.md" %}

{% block body %}
{% for item in items %}
  {% if loop.index0 % 2 == 0 %}

  <table class="full-width">
  {% endif %}

  {% if item.kind == 'youtube' %}
  <div class="video video-hover"><iframe width="450" height="315" src="{{ item.link }}" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> <center><h4>{{ item.title }}</h4></center></div>
  {% else %}
  <div class="video video-hover">
  <a href="{{ item.link }}" target="_blank"><img width="450" height="315" src="pics/talks/{{ item.filename }}"></a>
  <center><h4>{{ item.title }}</h4></center>
  </div>
  
  {% endif %}

  {% if loop.index0 % 2 == 1 %}
  </table>
  {% endif %}

{% endfor %}

{% endblock body %}
