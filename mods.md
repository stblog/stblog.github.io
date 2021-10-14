---
title: Моды для World of Tanks - скачать модпаки, официальные и лучшие сборки
layout: default
description: Скачать моды для World of Tanks последней версии и сборки модов WoT можно
  на нашем сайте. В разделе вы найдете лучшие модификации и модпаки для игры бесплатно!
  В том числе вотспик последней версии...
---

<div class="container-xl category-page">
	
    <div class="row">
        <div class="col-xl-9 col-lg-9 topmargin"><!-- list -->
		<div>
			<h1>Моды</h1>
		</div>	
		<div>	
			<p>Скачать моды и модпаки для World of Tanks. Благодаря модам в танках вы сможете значительно улучшить свой уровень игры и показывать гораздо лучшие результаты в матчах. На странице вы найдете последние сборки модов для танков, вотспик, а также все лучшие и последние моды, которые использует большинство игроков.</p>
		</div>	
		
		{% for post in site.categories.mods limit:5 %} 
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

</div><!-- container -->
