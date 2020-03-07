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
        <span class="post-meta">{{ repository.latest_release.published_at | date: "%b %-d, %Y" }}</span>
    </div>
    <div class="w3-bar-item">
        <h3 class="post-link">
            <a href="{{ repository.html_url }}">{{ repository.project_title }}</a>
        </h3>
    </div>
    <div class="w3-bar-item">
        {{ repository.project_tagline }}
    </div>
    <div class="w3-bar-item">
        <em>{{ repository.contributors | join: "</em> - <em>" }}</em>
    </div>
    {% if repository.url %}
    <div class="w3-bar-item">
        <a href="{{ repository.url }}">{{ repository.url }}</a>
    </div>
    {% endif %}
</li>
{% endfor %}
</ul>
