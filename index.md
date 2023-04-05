---
title: System Map
layout: default
---

<script>
    window.line_geojson = window.line_geojson || [];
    {% for json_file in site.data.geojson %}
        window.line_geojson.push( {
            source: {{ json_file[0] | jsonify }},
            data: {{ json_file[1] | jsonify }} 
        } );
    {% endfor %}
</script>
<style type="text/css">
    #map-container {
        height: min( 70vh, 1000px);
    }
</style>

<div class="scroll-container">
    <div class="scroll-container__fixed">
        {% include map.html simple=true %}
    </div>
    <div class="scroll-container__scrollable">
        <h2>Line List</h2>
        <dl id="line list">
        {% for line in site.lines %}
            <dt><a href="{{line.url | absolute_url }}">{{line.title}}</a></dt>
            <dd>{{line.excerpt}}</dd>
        {% endfor %}
        </dl>
    </div>
</div>

