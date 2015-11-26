---
layout: default
title: 生活
permalink: /pages/life.html
---
<div class="home">
	{% for category in site.categories %}
	<h1>category:{{ category }}</h1>
	<h1>category[0]:{{ category[0] }}</h1>
	<h1>category[1]:{{ category[1] }}</h1>
	<h1>category.first:{{ category.first }}</h1>
	<h1>category.last:{{ category.last }}</h1>
	{% if category[0] == 'life' %}
		<h2>{{ category | first }}</h2>
			<ul class="arc-list">
			{% for post in category.last %}
				<li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
			{% endfor %}
			</ul>
	{% endif %}
	{% endfor %}
</div>