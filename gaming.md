---
layout: page
title: Gaming
permalink: /gaming/
---

# Friend Codes
## Nintendo Switch
`{{ site.nintendoSwitchFC }}`
## Pokemon Home
{% include image.html url="{{ site.pokemonHomeQR }}" description="{{ site.pokemonHomeFC }}" %}

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

