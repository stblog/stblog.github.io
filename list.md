---
title: Карта сайта Мир танков Lesta Games
layout: default
description: Все материалы сайта ProTanks.ru. Читайте новости, гайды, обзоры игр,
  инструкции и обучающие материалы Мир танков Lesta Games на нашем игровом портале.
---

<div class="container-xl category-page">
	
    <div class="row">
        <div class="col-xl-9 col-lg-9 topmargin"><!-- list -->
			<div>
				<h1>Все материалы сайта</h1>
			</div>	
			
			<div class="row list-item">
				<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">
					<ul>
						{% for post in site.posts %} 
								<li>
									<a href="{{ post.url }}">
										{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}
									</a>
								</li>
						{% endfor %}
					</ul>
				</div>
			</div>
		
		</div><!-- topmargin -->
	    
		<div class="col-xl-3 col-lg-3 topmargin sidebar"><!-- sidebar -->
			{%- include sidebar.html -%}
		</div><!-- topmargin -->
    </div><!-- row -->

</div><!-- container -->
