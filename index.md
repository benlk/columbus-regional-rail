---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<script>
    window.line_geojson = [];
    {% for geojson in site.data.geojson %}
        window.line_geojson.push( {{ geojson | jsonify }} );
    {% endfor %}
</script>

{% include map.html %}

<dl id="line list">
{% for line in site.lines %}
    <dt><a href="{{line.url}}">{{line.title}}</a></dt>
    <dd>{{line.excerpt}}</dd>
{% endfor %}
</dl>