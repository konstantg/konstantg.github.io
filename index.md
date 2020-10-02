---
layout: about
description: Personal website of Konstantinos Gavriil.
---
<div class="face_container">
		<img src="/assets/img/portrait.svg" alt="Portrait" style="width:auto;height:auto;max-width:100%;max-height: 150px;" class="center">
</div>

I just received my PhD in Technical Mathematics from [TU Wien](https://www.tuwien.ac.at/en/){:target="_blank"}, at the [Applied Geometry](http://www.geometrie.tuwien.ac.at/geom/fg4/){:target="_blank"} group of the [Institute of Discrete Mathematics and Geometry](http://www.dmg.tuwien.ac.at/){:target="_blank"}, under the supervision of [Helmut Pottmann](http://www.dmg.tuwien.ac.at/pottmann/){:target="_blank"}.

The focus of my PhD research was to incorporate various constraint types, such as constraints imposed by material properties, into the abstract geometric modeling design process.

Until recently, I was an ITN Marie Skłodowska-Curie Research Fellow at [Evolute GmbH](https://www.evolute.at/){:target="_blank"}, working on geometric optimization algorithms with applications in architecture, CAD and interactive modeling.

I also enjoy working on problems in computational geometry, combinatorial optimization and algebraic geometry.

<br>

<hr>

<br>

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% assign count = 0 %}
__News &rsaquo;__

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

<br>

{% assign count = 0 %}
__Posts &rsaquo;__

<ul>
    {% for post in site.categories.blog %}

		{% if count == 2 %}
			{% break %}
		{% endif %}

		{% assign count = count | plus: 1 %}
	    <li><p>
	        <a href="{{ post.url }}" class="title_link">{{ post.title }}</a>
	        <br>

	        {{ post.excerpt }} <span class="date">{{ post.date | date: '%b %Y' }}</span>
	        <br>
	    </p></li>

    {% endfor %}

    <li><p>

		<a href="/blog">More...</a>

	</p></li>
</ul>

<br>

<hr>

<br>

<a href="https://www.tuwien.at/en/" target="_blank">
<img src="/assets/img/tuwien_logo.svg" alt="TU Wien Logo" style="opacity: 0.85;width:auto;height:auto;max-width:100%;max-height:80px;" class="center">
</a>

<br>
