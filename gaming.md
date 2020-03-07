---
layout: page
title: Gaming
permalink: /gaming/
---

# Friend Codes
{% for service in site.data.friendcodes %}
<h2>{{ service.name }}</h2>
{% if service.image %}
<figure class="image">
    <img src="{{ service.image }}" alt="QR code">
    <figcaption>{{ service.code }}</figcaption>
</figure>
{% else %}
<code>{{ service.code }}</code>
{% endif %}
{% endfor %}

# Posts
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

