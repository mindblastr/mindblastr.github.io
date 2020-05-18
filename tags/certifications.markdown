---
layout: tags_page
page_tag: certifications
hide_hero: true
---

# List of all the Certifications related Articles
<html>
<div>
    {% for tag in site.tags %}
        {% if page.page_tag== tag[0]%}
        <div>
            {% capture tag_name %}{{ tag | first }}{% endcapture %}
            {% for post in site.tags[tag_name] %}
            <article class="archive-item">
            <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
            </article>
            {% endfor %}
        </div>
        {% endif %}
    {% endfor %}
</div>
</html>

