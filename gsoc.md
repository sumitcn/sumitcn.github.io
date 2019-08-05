---
layout: default
title: gsoc
permalink: /gsoc/
---

<div id="home">
    <h1>Google Summer of Code - LibreOffice </h1>
    <hr />
    <ol class="gsoc">
		{% for post in site.categories.gsoc %}

     			<li><a href="{{ post.url }}">{{ post.title }}</a> {{ seriesPost }} &raquo; <i><span>{{ post.date | date_to_string }}</span></i></li>
		{% endfor %}     
	</ol>


</div>
<!-- end #home -->
