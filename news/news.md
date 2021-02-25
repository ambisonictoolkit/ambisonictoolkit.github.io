---
layout: page
title: Recent News
permalink: /news/
---


{% for post in site.posts limit:3 %}

<h2 class="page-header">
  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br/>
  <small>
    Posted <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%b %-d, %Y" }}</time>
    {% if post.author %}
      by <span itemprop="author" itemscope itemtype="https://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>
    {% endif %}
  </small>
</h2>

{{ post.content }}

<hr/>

<div class="col-xs-12" style="height:5em;"></div>

{% endfor %}
        
<p class="text-center"><a href="/news/archive/">View the full archive</a> | Subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

