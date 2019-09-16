## <i class="fa fa-chevron-right"></i> All Publications

<a href="https://scholar.google.com/citations?user={{ scholar_id }}" class="btn btn-primary" style="padding: 0.3em;">
  <i class="ai ai-google-scholar"></i> Google Scholar
</a>

{% for p in content %}

### {{ p.title }} 

<table class="table table-hover">
{{ p.details }}
</table>
{% endfor %}
