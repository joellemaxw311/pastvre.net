---
layout: page
title: Gaming
permalink: /gaming/
---

This is where I will 

## Friend Codes

Add me as a friend in one of these games or services! All the services I list here are probably Nintendo products, because friend codes are pretty obselete.

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

## Posts about Gaming

<ul class="post-list w3-ul w3-card-4">
{% for post in site.posts %}
{% if post.categories contains "gaming" %}
    <a href="{{ post.url | prepend: site.baseurl }}">
    <li class="w3-bar pop-on-hover">
        <div class="w3-bar-item">
            <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
            <h3 class="post-link">
                {{ post.title }}
            </h3>
        </div>
        {% if post.thumbnail %}
        <div class="w3-bar-item">
            <img src="{{ post.thumbnail }}" class="post-thumbnail">
        </div>
        {% endif %}
    </li>
    </a>
{% endif %}
{% endfor %}
</ul>
