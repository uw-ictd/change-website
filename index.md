---
layout: default
title: Change
---

Change is a cross-campus collaboration involving faculty and
students from TASCHA (Technology and Social Change) at the iSchool,
Global WACh and I-TECH (International Training and Education Center
for Health) at the Department of Global Health, and ICTD (Information
and Communication Technologies for Development) at CSE.

<div class="panel panel-primary">
	<div class="panel-heading">Get Involved</div>
	<div class="panel-body">
		<ul>
			<li><a href="docs/ICTD_Open_Session_Research_Brief_Aug2016.pdf">Join the mailing list TODO</a></li>
			<li><a href="docs/Mobile_Money_Security_Research_Brief_Aug2016.pdf">Check out the calendar TODO</a></li>
                        <li>Interested in speaking? Email admin@change.washington.edu</li>
		</ul>
	</div>
</div>

<h2>Updates</h2>
<ul class="news list-unstyled">
{% for post in site.posts limit: site.front_page_news %}
    {% if post.shortnews %}
        <li class="shortnews">
            <span class="date">{{ post.date | date_to_long_string }}</span>
            {{ post.content }}
        </li>
    {% else %}
        <li class="bloglink">
            <span class="date">{{ post.date | date_to_long_string }}</span>
            <a href="{{ post.url }}">&raquo; {{ post.title }}</a>
        </li>
    {% endif %}
{% endfor %}
</ul>
{% assign numposts = site.posts | size %}
 
<p><a href="{{ site.base }}/blog/">Older posts&hellip;</a></p>


 