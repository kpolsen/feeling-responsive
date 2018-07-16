---
layout: page
show_meta: false
title: "Adventures with Karen"
subheadline: "blogging"
header:
   image_fullwidth: "header_unsplash_5.jpg"
permalink: "/more/blog/"
---
<ul>
    {% for post in site.categories.blog %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>