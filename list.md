---
title: Карта сайта Мир танков Lesta Games
layout: default
description: Все материалы сайта ProTanks.ru. Читайте новости, гайды, общоры игр,
  инструкции и обучающие материалы Мир танков Lesta Games на нашем игровом портале.
---

<div class="container-xl category-page">
	
    <div class="row">
        <div class="col-xl-9 col-lg-9 topmargin"><!-- list -->
		<div>
			<h1>Гайды</h1>
		</div>	
		
		{% for post in site.categories.guides limit:10 %} 
			<div class="row list-item">
				<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">
					<a href="{{ post.url }}">
						<h3>{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}</h3>
					</a>
				</div>
			</div>
		{% endfor %}
		
	</div><!-- topmargin -->
	    
	<div class="col-xl-3 col-lg-3 topmargin sidebar"><!-- sidebar -->
		{%- include sidebar.html -%}
	</div><!-- topmargin -->
    </div><!-- row -->

</div><!-- container -->
