---
title: Главная
layout: default
---

<div class="top-posts">
	<div class="container-xl">
		<div class="row">
			<div class="col-xl-8 col-lg-8 col-md-8">
				{% assign c = site.posts %}
				<div class="big-item">
					<a href="{{ c[0].url }}">
						<div class="big-item-img">
							<img src='{{ c[0].image }}'>
						</div>
						<div class="big-item-title">
							<h3 style="display: NONE;">{% if c[0].header %}{{ c[0].header | escape }}{% else %}{{ c[0].title | escape }}{% endif %}</h3>
							<time datetime='{{ c[0].date|date:"%d.%m.%Y" }}' class="item-published"><i class="fa fa-calendar" aria-hidden="true"></i> {{ c[0].date|date:"%d.%m.%Y" }}</time>
						</div>
					</a>	
				</div>
				
			</div>
			<div class="col-xl-4 col-lg-4 col-md-4">
				<div class="row">
					<div class="col-sm-12 mini-one">
						<div class="mini-item">
							<a href="{{ c[1].url }}">
								<div class="mini-item-img">
									<img src='{{ c[1].image }}'>
								</div>
								<div class="mini-item-title">
									<h3 style="display: NONE;">{% if c[1].header %}{{ c[1].header | escape }}{% else %}{{ c[1].title | escape }}{% endif %}</h3>
								</div>
							</a>
						</div>
						
					</div>
				</div>
				<div class="row">
					<div class="col-sm-12 mini-two">
						<div class="mini-item">
							<a href="{{ c[2].url }}">
								<div class="mini-item-img">
									<img src='{{ c[2].image }}'>
								</div>
								<div class="mini-item-title">
									<h3 style="display: NONE;">{% if c[2].header %}{{ c[2].header | escape }}{% else %}{{ c[2].title | escape }}{% endif %}</h3>
								</div>
							</a>	
						</div>

					</div>
				</div>
			</div>
		</div>
	</div>
</div>


<div class="container-xl main-page">
     <div class="row">
        <div class="col-sm-12 topmargin">
		<div>
			<h2><strong>ПОЛЕЗНЫЕ</strong> ГАЙДЫ</h2>
		</div>
		<div class="row">
				
			{% for post in site.categories.guides limit:4 %} 
				<div class="col-xl-3 col-lg-3 col-md-6 col-sm-6 item-img">
					<div class="mini-item row-block">
						<a href="{{ post.url }}">
							<div class="mini-item-img">
								<img src='{{ post.image }}'>	
							</div>
							<div class="mini-item-title">
								<h3>{% if post.header %}{{ post.header | escape }}{% else %}{{ post.title | escape }}{% endif %}</h3>
							</div>
						</a>	
					</div>
				</div>
			{% endfor %}
			
		</div><!-- row -->
	</div><!-- topmargin -->
    </div><!-- row -->
	
    <div class="row">
        <div class="col-xl-9 col-lg-9 topmargin"><!-- list -->
		<div>
			<h2><strong>ИНТЕРЕСНЫЕ</strong> СТАТЬИ</h2>
		</div>	
		
		{% for post in site.categories.articles limit:7 %} 
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
					<p>{{ post.content | strip_html | truncatewords: 55 }}</p>
				</div>
			</div>
		{% endfor %}
		
	</div><!-- topmargin -->
	    
	<div class="col-xl-3 col-lg-3 topmargin sidebar"><!-- sidebar -->
		{%- include sidebar.html -%}
	</div><!-- topmargin -->
    </div><!-- row -->

</div><!-- container -->	
