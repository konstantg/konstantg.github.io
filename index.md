---
layout: about
description: Personal website of Konstantinos Gavriil.
---
<div class="face_container">
		<img src="/assets/img/portrait_light.png" alt="Portrait" style="width:auto;height:auto;max-width:100%;max-height: 150px;" class="center">
</div>

I am a PhD candidate at the [Applied Geometry](http://www.geometrie.tuwien.ac.at/geom/fg4/){:target="_blank"} group of the [Institute of Discrete Mathematics and Geometry](http://www.dmg.tuwien.ac.at/){:target="_blank"} at [TU Wien](https://www.tuwien.ac.at/en/){:target="_blank"}, under the supervision of [Helmut Pottmann](http://www.dmg.tuwien.ac.at/pottmann/){:target="_blank"}.

Until recently, I was an ITN Marie Skłodowska-Curie Research Fellow at [Evolute GmbH](https://www.evolute.at/){:target="_blank"}, working on geometric optimization algorithms with applications in architecture, CAD and interactive modeling.

The focus of my PhD research is to incorporate various constraint types, such as constraints imposed by material properties, into the abstract geometric modeling design process.

I also enjoy working on problems in computational geometry, combinatorial optimization and algebraic geometry.

<br>

<hr>

<br>

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
{% assign count = 0 %}
__Upcoming &rsaquo;__

<ul>
	{% for item in site.data.events reversed %}
		{% if count == 3 %}
			{% break %}
		{% endif %}
		{% capture eventtime %}{{item.dateend | date: '%s'}}{% endcapture %}
		{% if eventtime > nowunix %}
			{% assign count = count | plus: 1 %}
			<li><p>

				{% if item.event %}
					{% if item.eventurl %}
						<a href="{{ item.eventurl }}" target="_blank">{{ item.event }}</a>
					{% else %}
						{{ item.event }}
					{% endif %}
					<br>
				{% endif %}

				{% if item.title %}
					{% if item.titleurl %}
						<a href="{{ item.titleurl }}" target="_blank">{{ item.title }}</a>
					{% else %}
						{{ item.title }}
					{% endif %}
					<br>
				{% endif %}

				{% if item.location %}
					{{ item.location }}
					<br>
				{% endif %}

				{% if item.datetext %}
					<span class="date">{{ item.datetext }}</span>
					<br>
				{% endif %}

			</p></li>
			<br />
		{% endif %}
	{% endfor %}

	<li><p>

		<a href="/map">More...</a>

	</p></li>

</ul>

<br>

{% assign count = 0 %}
__Latest posts &rsaquo;__

<ul>
    {% for post in site.posts %}

		{% if count == 2 %}
			{% break %}
		{% endif %}

		{% assign count = count | plus: 1 %}
	    <li><p>
	        <a href="{{ post.url }}">{{ post.title }}</a>
	        <br>

	        {{ post.excerpt }} <span class="date">{{ post.date | date: '%B %Y' }}</span>
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
