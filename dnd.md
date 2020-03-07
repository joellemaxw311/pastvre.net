---
layout: page
title: Dungeons & Dragons
permalink: /dnd/
---

## Hall of Fame

The following are characters that I have created and played as:

| Character | Bio | Portrait |
|-|:-:|-:|
{% for character in site.data.dndcharacters %}
| {{ character.name }} | {{ character.class }}<br>{{ character.race }}<br>{{ character.level }} | ![]({{ character.photo }}) |
{% endif %}
{% endfor %}
