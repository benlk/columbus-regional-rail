## Checklist for new routes

- [ ] Creates a new line in `_lines` by copying `_lines/_template.md` to a new file
	- [ ] What inspires this line?
	- [ ] Who contributed or deserves props?
	- [ ] Why is it a good idea?
- [ ] Create a GeoJSON file using http://geojson.io/ to draw the line:
	- [ ] Use these table columns:
		- "name": No more than 50 characters
		- "description": Short text description of the thing.
		- "simple": `true` will display this item on the home map
		- "icon": References an icon type in `_includes/map.html`
		- "type": `route`, `station`, `construction``
		- ["stroke"](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke)
		- ["dashArray"](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke-dasharray).
	- [ ] Save the map in `_data/geojson` as a `.json` file. 
	- [ ] Add that file name to your new file in `_lines/` as the "geojson:" key

Closes #

## Necessary stuff

- [ ] I agree to release this content under the terms of the project
- [ ] I have tested that this PR builds successfully