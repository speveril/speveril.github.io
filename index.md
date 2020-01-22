---
layout: default
title: speveril.github.io
---

welcome to site

<div class="posts">
    {% for post in site.posts limit:3 %}
        <article>
            <!-- <h1 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h1>
            <h2 class="date">Posted {{ post.date | date: "%B %d, %Y" }}</h2> -->
            {{ post.content }}
        </article>
    {% endfor %}
</div>