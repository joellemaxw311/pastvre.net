---
layout: page
title: Projects
permalink: /projects/
---

## GitHub

<ul class="post-list w3-ul w3-card-4">
{% for repository in site.github.public_repositories %}
<li class="w3-bar">
    <div class="w3-bar-item">
        <h3 class="post-link">
            <a href="{{ repository.html_url }}">{{ repository.name }}</a>
        </h3>
    </div>
</li>
{% endfor %}
</ul>
