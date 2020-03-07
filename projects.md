---
layout: page
title: Projects
permalink: /projects/
---

## GitHub
{% for repository in site.github.public_repositories %}
* [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}
