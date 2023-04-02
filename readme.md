---
title: About this GitHub Repository
published: false
---

This repo contains the code for [the Columbus Regional Rail website](https://benlk.github.io/columbus-regional-rail).

Here's the ways you can help:

- Research: check out [the issues list](https://benlk.github.io/columbus-regional-rail/issues) and look at the issues tagged "research needed". Dig into those, then either get a GitHub account and reply in the thread with your findings, or @ me on Mastodon at [@benlk@urbanists.social](https://urbanists.social/@benlk).
- Code: The site is built and hosted with GitHub Pages, which is basically the Jekyll static-site builder. Fork the repo, [get Jekyll running on your local environment](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll), make your changes, and open a pull request.

### Making a new line

- copy `_lines/_template.md` to a new file
- use http://geojson.io/ to draw the line:
	- Table columns: "name", "description", "icon", "type", ["stroke"](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke), ["dashArray"](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stroke-dasharray)
	- save the map in `_data/geojson` as a `.json` file. 
	- add it to your new file in `_lines/` as the "geojson:" key

### Other todos

- [ ] pedestrian observations blog post about good types of transit
- [ ] costs page
	- [ ] per-mile costs to build of various types of transportation in US
	- [ ] staffing: automation vs not
	- [ ] hours to run
- [ ] history
	- [ ] suggestion from M: map timeline of gas prices, interest rates, vs cost of proposal
	- [ ] the tram lines
