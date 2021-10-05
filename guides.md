---
layout: default
title: Гайды
---



<div class="container">
	
    <div class="row">
        <div class="col-sm-9 topmargin"><!-- list -->
		<div>
			<h3><strong>ПОСЛЕДНИЕ</strong> НОВОСТИ</h3>
		</div>	
		
		{% for post in site.categories.guides limit:3 %} 
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
						<h3>{{ post.title }}</h3>
					</a>
					<p>{{ post.content | strip_html | truncatewords: 35 }}</p>
				</div>
			</div>
		{% endfor %}
		
	</div><!-- topmargin -->
	    
	<div class="col-sm-3 topmargin"><!-- sidebar -->
		<div>
			<h4><strong>ЧИТАЙТЕ</strong> ТАКЖЕ</h4>
		</div>
		<div class="row">
			<div class="col-sm-12">sidebar sidebar sidebar sidebar sidebar sidebar sidebar </div>
		</div>
		<div class="row">
			<div class="col-sm-12">sidebar sidebar sidebar sidebar sidebar sidebar sidebar </div>
		</div>
	</div><!-- topmargin -->
    </div><!-- row -->

</div><!-- container -->
