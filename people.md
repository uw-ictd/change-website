---
layout: default
background: img/papua.jpg
title: people
---

<h3>Organizers</h3>
<div style="padding-left:30px;">
	{% for role in site.data.people.organizers %}
		{% assign person = role[1] %}
		<dt class="person">
		  {% if person.webpage %}
		  <a href="{{ person.webpage |escape }}">
		  {% endif %}
			{{ person.display_name }}
            {% if person.affiliation %}<br />({{ person.affiliation }}){% endif %}
		  {% if person.webpage %}
		  </a>
		  {% endif %}
		  <br />
		  {% if person.img %}
		     {% if person.webpage %}
		        <a href="{{ person.webpage |escape }}"><img src="img/{{ person.img }}" alt="{{ person.display_name }}" class="img-rounded" height="120"/></a>
		     {% else %}
		        <img src="img/{{ person.img }}" alt="{{ person.display_name }}" class="img-rounded" height="120"/>
		     {% endif %}
		  {% else %}
			<img src="img/profile_blank.jpg" alt="{{ person.display_name }}" class="img-rounded" height="120"/>
		  {% endif %}
		</dt>
	{% endfor %}
</div>

<br style="clear:both">

