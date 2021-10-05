---
layout: default
title: Статьи World of Tanks
description: Статьи об игре World of Tanks и других играх. Обзоры будущих обновлений WoT, анонс новых игр для ПК, обзоры новинок и прохождения игр...
---



<div class="container category-page">
	
    <div class="row">
        <div class="col-sm-9 topmargin"><!-- list -->
		<div>
			<h1>Статьи</h1>
		</div>	
		
		{% for post in site.categories.articles limit:3 %} 
			<div class="row list-item">
				<div class="col-sm-3">
					<div class="list-item-img">
						<a href="{{ post.url }}">
							<img src='/uploads/{{ post.date|date:"%Y" }}/{{ post.date|date:"%m" }}/{{ post.thumb }}'>
						</a>
					</div>
				</div>
				<div class="col-sm-9">
					<a href="{{ post.url }}">
						<h3>{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}</h3>
					</a>
					<p>
						<time datetime='{{ post.date|date:"%d.%m.%Y" }}' class="item-published"><i class="fa fa-calendar" aria-hidden="true"></i> {{ post.date|date:"%d.%m.%Y" }}</time>
					</p>
					<p>{{ post.content | strip_html | truncatewords: 35 }}</p>
				</div>
			</div>
		{% endfor %}
		
	</div><!-- topmargin -->
	    
	<div class="col-sm-3 topmargin sidebar"><!-- sidebar -->
		{%- include sidebar.html -%}
	</div><!-- topmargin -->
    </div><!-- row -->

</div><!-- container -->
