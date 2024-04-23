---
title: Моды для Мир кораблей Lesta Games (World of Tanks)
layout: default
description: Скачать моды для Мир кораблей Lesta Games (World of Tanks) последней
  версии и лучшие сборки модов. Популярные модификации и модпаки бесплатно! Актуальные
  версии.
---

<div class="container-xl category-page mods-page">
	
    <div class="row">
        <div class="col-12 topmargin"><!-- list -->
			<div>
				<h1>Моды</h1>
			</div>	
			<div>	
				<p>Скачать моды и модпаки для Мир кораблей Lesta Games (World of Tanks). Благодаря модификация в танках вы сможете значительно улучшить свой уровень игры и показывать гораздо лучшие результаты в матчах. На странице вы найдете самые популярные и проверенные сборки модов, вотспик, а также лучшие последние моды, которые использует большинство игроков.</p>
			</div>	
			
			<div class="row">
			{% for post in site.categories.mods limit:16 %} 
					<div class="list-item col-xl-3 col-lg-3 col-md-4 col-sm-2 col-xs-1">
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
		
		</div><!-- topmargin -->
	    
    </div><!-- row -->
	
	<div class="row">
        <div class="col-12 topmargin">
			<a class="dl-mod" style="text-align: center;" href="/list">Больше материалов</a>
		</div>
	</div><!-- row -->

</div><!-- container -->
