---
layout: default
title: 生活
permalink: /pages/life.html
---
<div class="home">

	{% for category in site.categories %} 
		{% flag = 0 %}
		{% for post in category[1] %}
			{% if post.type == 'life' %}
				{% if flag == 0 %}
					<div class="panel panel-primary">
					{% flag+1 %}
				{% endif %}
					<div class="panel-heading center" id="{{ category[0] }}" name="{{ category[0] }}">{{ category[0] }}</div>
						<a  href='{{ post.url }}'  class="list-group-item clearfix pjaxlink">
								{{post.title}}
				            <span class="badge">{{ post.date | date:"%Y年%m月%d日" }}</span>
				        </a>
			{% endif %} 
			{% flag=0 %}
	   {% endfor %}
				</div>
				
	{% endfor %}
	
</div>