---
layout: tags_page
page_tag: all
hide_hero: true
---

# List of all the Articles, sorted by Tag
<html>
    <div id="archives">
    {% for tag in site.tags %}
    <div class="archive-group">
        {% capture tag_name %}{{ tag | first }}{% endcapture %}
        <div id="#{{ tag_name | slugize }}"></div>
        <p></p>

        <h3 class="category-head">{{ tag_name | capitalize }}</h3>
        <a name="{{ tag_name | slugize }}"></a>
        {% for post in site.tags[tag_name] %}
        <article class="archive-item">
        <h4><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
        </article>
        {% endfor %}
    </div>
    {% endfor %}
    </div>
</html>