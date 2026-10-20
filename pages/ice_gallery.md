---
title: Ice Gallery
layout: page
permalink: /ice_gallery.html

# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---
# Ice Gallery


{% assign items = site.data[site.metadata] | where_exp: 'item', 'item.subject contains "ice"' | sort: "date_range" %}

<div class="row my-3 py-3">
{% for item in items %}
<div class="col-md-4">
{% include feature/image.html objectid=item.objectid %}
</div>
{% endfor %}
</div>

