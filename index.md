---
layout: default
title: Change
---

<h2>About</h2>
Change is a cross-campus collaboration involving faculty and
students from TASCHA (Technology and Social Change) at the iSchool,
Global WACh and I-TECH (International Training and Education Center
for Health) at the Department of Global Health, and ICTD (Information
and Communication Technologies for Development) at CSE.

<h2>Participate</h2>
<a href="https://changemm.cs.washington.edu/mailman/listinfo/change">Join the mailing list</a><br/>
<a href="https://calendar.google.com/calendar?cid=dXdjaGFuZ2VAZ21haWwuY29t">Check out the calendar</a>

<h2>Current Events</h2>
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

