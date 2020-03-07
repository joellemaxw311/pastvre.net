---
layout: page
title: Dungeons & Dragons
permalink: /dnd/
---

## Hall of Fame

The following are characters that I have created and played as:

<table>
    <tr>
        <th>Character</th>
        <th>Details</th>
        <th>Portrait</th>
    </tr>
    {% for character in site.data.dndcharacters %}
    {% assign classes = character.class | split: "/" %}
    <tr>
        <td>
            <h3>{{ character.name }}</h3>
            {% if character.title %}
            <i>{{ character.title }}</i>
            {% endif %}
        </td>
        <td>
            <dl>
                <dt>Level</dt>
                <dd>{{ character.level }}</dd>
                <dt>Race</dt>
                <dd>{{ character.race }}</dd>
                <dt>Class</dt>
                {% for class in classes %}
                <dd>{{ class }}</dd>
                {% endfor %}
            </dl>
        </td>
        <td><img src="{{ character.photo }}"></td>
    </tr>
    {% endfor %}
</table>
