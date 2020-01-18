---
layout: base
title: speveril.github.io
---

<div class="posts">
    {% for post in site.posts limit:3 %}
        <article>
            <h1>{{ post.title }}</h1>
            <h2 class="date">{{ post.date | date: "%B %d, %Y" }}</h2>
            {{ post.content }}
        </article>
    {% endfor %}
</div>