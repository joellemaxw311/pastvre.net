---
layout: page
title: Gaming
permalink: /gaming/
---

## Friend Codes
{% for service in site.data.friendcodes %}
<h3>{{ service.name }}</h3>
{% if service.image %}
<figure class="image">
    <img src="{{ service.image }}" alt="QR code">
    <figcaption>{{ service.code }}</figcaption>
</figure>
{% else %}
<code>{{ service.code }}</code>
{% endif %}
{% endfor %}

---

## Posts
<ul class="post-list">
{% for post in site.posts %}
{% if post.categories contains "gaming" %}
    <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h3>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h3>
    </li>
{% endif %}
{% endfor %}
</ul>

