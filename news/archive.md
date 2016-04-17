---
layout: page
title: News Archive
permalink: /news/archive/
---

{% for post in site.posts %}

<h2 class="page-header">
  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br/>
  <small>
    Posted <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%b %-d, %Y" }}</time>
    {% if post.author %}
      by <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>
    {% endif %}
  </small>
</h2>

{{ post.excerpt }}

<p><a href="{{ post.url | prepend: site.baseurl }}">Continue reading&hellip;</a></p>

<hr/>

<div class="col-xs-12" style="height:5em;"></div>

{% endfor %}
        
<p class="text-center"><a href="/news/archive/">View the full archive</a> | Subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

