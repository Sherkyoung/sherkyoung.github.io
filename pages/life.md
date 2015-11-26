---
layout: default
title: 生活
permalink: /pages/life.html
---
<div class="home">
	{% for category in site.categories.life %}
		<h2>{{ category | first }}</h2>
			<ul class="arc-list">
			{% for post in category.last %}
				<li>{{ post.date | date:"%d/%m/%Y"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
			{% endfor %}
			</ul>
	{% endfor %}
</div>