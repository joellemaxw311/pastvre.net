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
        <th>Class</th>
        <th>Portrait</th>
    </tr>
    {% for character in site.data.dndcharacters %}
    <tr>
        <td>
            <b>{{ character.name }}</b><br>
            {{ character.race }} <br>
            Level {{ character.level }}
        </td>
        <td>
            {{ character.class | split: "/" | join: "<br>" }}
        </td>
        <td><img src="{{ character.photo }}"></td>
    </tr>
    {% endfor %}
</table>
