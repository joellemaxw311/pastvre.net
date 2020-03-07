---
layout: page
title: Gaming
permalink: /gaming/
---

Nintendo Switch Friend Code: [SW-6152-2011-6941]()

<ul class="post-list">
{% for post in site.posts %}
{% if post.categories contains "gaming" %}
    <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
    </li>
{% endif %}
{% endfor %}
</ul>

