---
title: Моды для World of Tanks - скачать модпаки, официальные и лучшие сборки
layout: default
description: Скачать моды для World of Tanks последней версии и лучшие сборки модов
  WoT можно на нашем сайте. В разделе вы найдете популярные модификации и модпаки
  для игры бесплатно! В том числе вотспик актуальной версии...
---

<div class="container-xl category-page mods-page">
	
    <div class="row">
        <div class="col-12 topmargin"><!-- list -->
			<div>
				<h1>Моды</h1>
			</div>	
			<div>	
				<p>Скачать моды и модпаки для World of Tanks. Благодаря модификация в танках вы сможете значительно улучшить свой уровень игры и показывать гораздо лучшие результаты в матчах. На странице вы найдете самые популярные и проверенные сборки модов, вотспик, а также лучшие последние моды, которые использует большинство игроков.</p>
			</div>	
			
			<div class="row">
			{% for post in site.categories.mods limit:4 %} 
					<div class="list-item col-xl-3 col-lg-3 col-md-3 col-sm-3">
						<div class="list-item-img">
							<a href="{{ post.url }}">
								<img src='{{ post.image }}'>
							</a>
						</div>
						<a href="{{ post.url }}">
							<h3>{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}</h3>
						</a>
						<p>{{ post.content | strip_html | truncatewords: 25 }}</p>
					</div>
			{% endfor %}
			</div>
			
			<div class="row">
			{% for post in site.categories.mods limit:4 offset:4 %} 
					<div class="list-item col-xl-3 col-lg-3 col-md-3 col-sm-3">
						<div class="list-item-img">
							<a href="{{ post.url }}">
								<img src='{{ post.image }}'>
							</a>
						</div>
						<a href="{{ post.url }}">
							<h3>{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}</h3>
						</a>
						<p>
							<time datetime='{{ post.date|date:"%d.%m.%Y" }}' class="item-published"><i class="fa fa-calendar" aria-hidden="true"></i> {{ post.date|date:"%d.%m.%Y" }}</time>
						</p>
						<p>{{ post.content | strip_html | truncatewords: 25 }}</p>
					</div>
			{% endfor %}
			</div>
		
		</div><!-- topmargin -->
	    
    </div><!-- row -->

</div><!-- container -->
