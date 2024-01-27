---
layout: about
description: Personal website of Konstantinos Gavriil.
---
<div class="face_container">
		<img style="width:100%; height:100%; object-fit: cover; display: block; position:relative; bottom: 0;" src="/assets/img/average.png" alt="Portrait" >
		<img style="width:auto;height:100%;max-height: 260px; display: block; position:absolute; bottom: 0;" src="/assets/img/portrait2023.png" alt="Portrait" >
</div>

I am a __Research Scientist__ at the [Geometry group](https://www.sintef.no/en/digital/departments-new/applied-mathematics/geometry/){:target="_blank"} of [__SINTEF Digital__](https://www.sintef.no/en/digital/){:target="_blank"} in Oslo, Norway. I am interested in applied geometry, geometry processing, computational design and machine learning.

I received my PhD in Technical Mathematics from [TU Wien](https://www.tuwien.ac.at/en/){:target="_blank"}, at the [Applied Geometry](http://www.geometrie.tuwien.ac.at/geom/fg4/){:target="_blank"} group of the [Institute of Discrete Mathematics and Geometry](http://www.dmg.tuwien.ac.at/){:target="_blank"}, under the supervision of [Helmut Pottmann](https://www.geometrie.tuwien.ac.at/pottmann/){:target="_blank"}. The focus of my PhD research was to incorporate various constraint types, such as constraints imposed by material properties, into the abstract geometric modeling design process.

Until recently, I was an ITN Marie Skłodowska-Curie Research Fellow at [Evolute GmbH](https://www.evolute.at/){:target="_blank"}, working on geometric optimization algorithms with applications in architecture, CAD and interactive modeling.

I also enjoy working on problems in computational geometry, and combinatorial optimization.

<br>

<!-- <div class="positioner"> -->
<div class="banner">
	<div class="banner_wrapper">
	<div class="banner_header">
		<span class="banner_title">Latest posts</span>
		<a href="blog/">{{ post.title }}<span class="banner_more">See more →</span></a>
	</div>
	<div class="banner_container">
		<a href="{{site.categories.blog[0].url}}" class="banner_item_first">
			<div>
				<img src="{{site.categories.blog[0].image}}">
				<div class="banner_category">{{site.categories.blog[0].tags[0]}}</div>
				<div class="banner_item_first_title">{{site.categories.blog[0].title}}</div>
				<!-- <div class="banner_item_first_description">{{site.categories.blog[0].description}}</div> -->
			</div>
		</a>
		<div class="banner_right">
			<a href="{{site.categories.blog[1].url}}" class="banner_square_item">
				<div >
					<img src="{{site.categories.blog[1].image}}">
					<div class="banner_category">{{site.categories.blog[1].tags[0]}}</div>
					<div class="banner_square_item_title">{{site.categories.blog[1].title}}</div>
				</div>
			</a>

			<a href="{{site.categories.blog[2].url}}" class="banner_square_item">
				<div>
					<img src="{{site.categories.blog[2].image}}">
					<div class="banner_category">{{site.categories.blog[2].tags[0]}}</div>
					<div class="banner_square_item_title">{{site.categories.blog[2].title}}</div>
				</div>
			</a>
		</div>
	</div>
	</div>
</div>
<!-- </div> -->

<br>

<!-- <hr> -->

<br>

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% assign count = 0 %}
<a href="news/" class="title_link">News &rsaquo;</a>

<ul>
		{% for post in site.categories.news %}

			{% if count == 5 %}
				{% break %}
			{% endif %}

			{% assign count = count | plus: 1 %}
	    <li>
	        <span class="date">{{ post.date | date: '%b %Y' }}</span> <a href="{{ post.url }}" class="title_link">{{ post.title }}</a>

					<br>

					{{ post.excerpt }}
	    </li>
    {% endfor %}

    <li><p>

		<a href="/news">More...</a>

		</p></li>
</ul>


<!-- <br> -->

<!-- <hr>

<br> -->

<!-- <a href="https://www.sintef.no/en/" target="_blank">
<img src="/assets/img/sintef_logo.svg" alt="SINTEF Logo" style="opacity: 0.85;width:auto;height:auto;max-width:100%;max-height:30px;" class="center">
</a> -->

<br>
