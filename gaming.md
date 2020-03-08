---
layout: page
title: Gaming
permalink: /gaming/
---

This page features content related to video games that I play.

## Profiles

### Steam
<a href="http://steamcommunity.com/id/ThePasture">
    <img src="https://steamsignature.com/profile/default/76561198054959613.png" alt="">
</a>

## Friend Codes

Add me as a friend in one of these games or services! It is likely that all the services I will list here are Nintendo products, because friend codes are pretty obselete.

{% for service in site.data.friendcodes %}
<h3>{{ service.name }}</h3>
{% if service.image %}
<figure class="image">
    <img src="{{ service.image }}" alt="QR code" class="thumbnail qr">
    <figcaption><code>{{ service.code }}</code></figcaption>
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
<li class="w3-bar">
    <div class="w3-bar-item">
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
    </div>
    <div class="w3-bar-item">
        <h3 class="post-link">
            <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h3>
    </div>
    {% if post.thumbnail %}
    <div class="w3-bar-item">
        <img src="{{ post.thumbnail }}" class="thumbnail">
    </div>
    {% endif %}
</li>
{% endif %}
{% endfor %}
</ul>
