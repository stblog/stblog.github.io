---
layout: default
title: Новости игры World of Tanks
description: Новости World of Tanks - обзоры выходящих обновлений игры, обзоры изменений веток и новых танков WoT, ангаров и другого контента в игре. Информация об изменениях баланса между танками, планы разработчиков на будущее и другая важная информация для поклонников мира танков...
---



<div class="container category-page">
	
    <div class="row">
        <div class="col-sm-9 topmargin"><!-- list -->
		<div>
			<h1>Новости</h1>
		</div>	
		
		{% for post in site.categories.news limit:3 %} 
			<div class="row list-item">
				<div class="col-md-3 col-sm-4">
					<div class="list-item-img">
						<a href="{{ post.url }}">
							<img src='/uploads/{{ post.date|date:"%Y" }}/{{ post.date|date:"%m" }}/{{ post.thumb }}'>
						</a>
					</div>
				</div>
				<div class="col-md-9 col-sm-8">
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
