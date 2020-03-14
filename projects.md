---
layout: page
title: Projects
permalink: /projects/
---

## GitHub
The following an automatically generated list of my public GitHub repositories:
<ul class="post-list w3-ul w3-card-4">
{% assign sorted = (site.github.public_repositories | sort: 'updated_at') | reverse %}
{% for repository in sorted %}
<li class="w3-bar project">
    <div class="w3-bar-item">
        <h3 class="post-link">
            <a href="{{ repository.html_url }}">{{ repository.name }}</a>
        </h3>
        <p>{{ repository.description }}</p>
    </div>
    <div class="w3-bar-item">
        <span class="post-meta date"><span class="start-date">{{ repository.created_at | date: "%b %Y" }}</span> - <span class="end-date">{{ repository.updated_at | date: "%b %Y" }}</span></span>
    </div>
</li>
{% endfor %}
</ul>

## Other Projects
<ul class="post-list w3-ul w3-card-4">
{% for project in site.data.projects %}
<li class="w3-bar project">
    <div class="w3-bar-item">
        <h3 class="post-link">{{ project.title }}</h3>
        {% if project.description %}
        <p>{{ project.description }}</p>
        {% endif %}
        {% if project.url %}
            <a href="{{ project.url }}" class="post-meta date">{{ project.url }}</a>
        {% endif %}
    </div>
</li>
{% endfor %}
</ul>

<hr>
<p><small>Lasted updated {{ site.time | date: '%-d %B %Y' }}</small></p>
