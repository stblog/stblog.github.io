---
title: Статьи
layout: default
description: Статьи об игре "Мир танков" Lesta Games и других играх - обзоры обновлений,
  анонсы новых ПК-игр, новинки и прохождения.
---

<div class="container-xl category-page">
	
    <div class="row">
        <div class="col-xl-9 col-lg-9 topmargin"><!-- list -->
		<div>
			<h1>Статьи</h1>
		</div>	
		
		{% for post in site.categories.articles limit:10 %} 
			<div class="row list-item">
				<div class="col-xl-4 col-lg-4 col-md-4 col-sm-4">
					<div class="list-item-img">
						<a href="{{ post.url }}">
							<img src='{{ post.image }}'>
						</a>
					</div>
				</div>
				<div class="col-xl-8 col-lg-8 col-md-8 col-sm-8">
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
	    
		<div class="col-xl-3 col-lg-3 topmargin sidebar"><!-- sidebar -->
			{%- include sidebar.html -%}
		</div><!-- topmargin -->
		
    </div><!-- row -->
	
	<div class="row">
        <div class="col-9 topmargin" style="text-align: right;">
			<a href="/list" >Больше материалов...</a>
		</div>
	</div><!-- row -->

</div><!-- container -->
