---
layout: page
title: Projects
permalink: /projects/
---

## GitHub
The following an automatically generated list of my public GitHub repositories:
<ul class="post-list w3-ul w3-card-4">
{% for repository in site.github.public_repositories | sort: "updated_at" %}
<li class="w3-bar project">
    <div class="w3-bar-item">
        <h3 class="post-link">
            <a href="{{ repository.html_url }}">{{ repository.name }}</a>
        </h3>
        <p>{{ repository.description }}</p>
    </div>
    <div class="w3-bar-item">
        <span class="post-meta date"><span class="start-date">{{ repository.created_at | date: "%b %-d, %Y" }}</span> - <span class="end-date">{{ repository.updated_at | date: "%b %-d, %Y" }}</span></span>
    </div>
</li>
{% endfor %}
</ul>

## Other Projects
<ul class="post-list w3-ul w3-card-4">
{% for project in site.data.projects %}
<li class="w3-bar project">
    <div class="w3-bar-item">
        <h3 class="post-link">
        {% if project.url %}<a href="{{ project.url }}">{% endif %}
            {{ project.name }}
        {% if project.url %}</a>{% endif %}
        </h3>
        {% if project.description %}
        <p>{{ project.description }}</p>
        {% endif %}
    </div>
</li>
{% endfor %}
</ul>

