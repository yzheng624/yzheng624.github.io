---
layout: page
title: Drowning in Information
tagline: 
---
{% include JB/setup %}

<div class="post">
    {% for post in site.posts limit 5 %}
        <h3 class="title"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a> <span class="date">{{ post.date | date_to_string }}</span></h3>
        <p>{{ post.content | strip_html | truncatewords:75}}</p>
        <a href="{{ post.url }}" class="btn">Read more...</a><br><br>
    {% endfor %}
    
    <hr />
    <center><a href="/archive.html">~~ Browse Archive ~~</a></center>
</div>
