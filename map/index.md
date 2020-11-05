---
title: Map - Konstantinos Gavriil
description: Future and past events.
layout: map
---

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}

__Upcoming &rsaquo;__

<ul>
	{% for item in site.data.events reversed %}
		{% capture eventtime %}{{item.dateend | date: '%s'}}{% endcapture %}
		{% if eventtime > nowunix %}
			<li><p>

				{% if item.event %}
					{% if item.eventurl %}
						<a href="{{ item.eventurl }}" target="_blank" class="title_link">{{ item.event }}</a>
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
</ul>

<br>
__Past &rsaquo;__

<ul>
	{% for item in site.data.events %}
		{% capture eventtime %}{{item.dateend | date: '%s'}}{% endcapture %}
		{% if eventtime < nowunix %}
			<li><p>

				{% if item.event %}
					{% if item.eventurl %}
						<a href="{{ item.eventurl }}" target="_blank" class="title_link">{{ item.event }}</a>
					{% else %}
						<strong>{{ item.event }}</strong>
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
</ul>
