---
title: System Map
layout: default
---

<script>
    window.line_geojson = window.line_geojson || [];
    {% for geojson in site.data.geojson %}
        window.line_geojson.push( {{ geojson | jsonify }} );
    {% endfor %}
</script>

{% include map.html %}

<dl id="line list">
{% for line in site.lines %}
    <dt><a href="{{line.url | absolute_url }}">{{line.title}}</a></dt>
    <dd>{{line.excerpt}}</dd>
{% endfor %}
</dl>
