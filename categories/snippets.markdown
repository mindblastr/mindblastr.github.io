---
layout: category_page
page_category: snippets
hide_hero: true
---

# List of all the Snippet Articles
<html>
<div>
    {% for category in site.categories %}
        {% if page.page_category== category[0]%}
        <div>
            {% capture category_name %}{{ category | first }}{% endcapture %}
            {% for post in site.categories[category_name] %}
            <article class="archive-item">
            <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
            </article>
            {% endfor %}
        </div>
        {% endif %}
    {% endfor %}
</div>
</html>

