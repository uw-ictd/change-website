---
layout: default
title: People
---

<h3>Faculty</h3>
<div style="padding-left:30px;">
	{% for role in site.data.people.faculty %}
		{% assign person = role[1] %}
		<dt class="person">
		  {% if person.webpage %}
		  <a href="{{ person.webpage |escape }}">
		  {% endif %}
			{{ person.display_name }}
            {% if person.affiliation %}({{ person.affiliation }}){% endif %}
		  {% if person.webpage %}
		  </a>
		  {% endif %}
		  <br />
		  {% if person.img %}
			<img src="img/{{ person.img }}" alt="{{ person.display_name }}" class="img-rounded" width="100">
		  {% else %}
			<img src="img/profile_blank.jpg" alt="{{ person.display_name }}" class="img-rounded" width="100">
		  {% endif %}
		</dt>
	{% endfor %}
</div>

<br style="clear:both">

<h3>Staff</h3>
<div style="padding-left:30px;">
	{% for role in site.data.people.staff %}
		{% assign person = role[1] %}
		<dt class="person">
		  {% if person.webpage %}
		  <a href="{{ person.webpage |escape }}">
		  {% endif %}
			{{ person.display_name }}
            {% if person.affiliation %}({{ person.affiliation }}){% endif %}
		  {% if person.webpage %}
		  </a>
		  {% endif %}
		  <br />
		  {% if person.img %}
			<img src="img/{{ person.img }}" alt="{{ person.display_name }}" class="img-rounded" width="100">
		  {% else %}
			<img src="img/profile_blank.jpg" alt="{{ person.display_name }}" class="img-rounded" width="100">
		  {% endif %}
		</dt>
	{% endfor %}
</div>

<br style="clear:both">

<h3>Current Students, Researchers, and Community Members</h3>
<div style="padding-left:30px;">
{% for role in site.data.people.researchers %}
      <dt class="person">
	      {% assign person = role[1] %}
	  {% if person.webpage %}
	      <a href="{{ person.webpage |escape }}">
	  {% endif %}
	  {{ person.display_name }}
      {% if person.affiliation %}({{ person.affiliation }}){% endif %}
	  {% if person.webpage %}
	      </a>
	  {% endif %}
	  <br />
      </dt>
{% endfor %}
</div>

<br style="clear:both">

<h3>Affiliated Faculty</h3>
<div style="padding-left:30px;">
{% for role in site.data.people.affiliated_faculty %}
      <dt class="person">
	      {% assign person = role[1] %}
	  {% if person.webpage %}
	      <a href="{{ person.webpage |escape }}">
	  {% endif %}
	  {{ person.display_name }}
      {% if person.affiliation %}({{ person.affiliation }}){% endif %}
	  {% if person.webpage %}
	      </a>
	  {% endif %}
	  <br />
      </dt>
{% endfor %}
</div>

<br style="clear:both">

<h3>Alumni</h3>
<div style="padding-left:30px;">
{% for role in site.data.people.alumni %}
      <dt class="person">
	      {% assign person = role[1] %}
	  {% if person.webpage %}
	      <a href="{{ person.webpage |escape }}">
	  {% endif %}
	  {{ person.display_name }}
      {% if person.affiliation %}({{ person.affiliation }}){% endif %}
	  {% if person.webpage %}
	      </a>
	  {% endif %}
      </dt>
{% endfor %}
</div>

<br style="clear:both">

