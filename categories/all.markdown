---
layout: category_page
page_category: all
hide_hero: true
---

# List of all the Articles, sorted by Category
<html>
    <div id="archives">
    {% assign sorted_categories = site.categories | sort %}
    {% for category in sorted_categories %}
    <div class="archive-group">
        {% capture category_name %}{{ category | first }}{% endcapture %}
        <div id="#{{ category_name | slugize }}"></div>
        <p></p>

        <h3 class="category-head">{{ category_name | capitalize }}</h3>
        <a name="{{ category_name | slugize }}"></a>
        {% for post in site.categories[category_name] %}
        <article class="archive-item">
        <h4><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
        </article>
        {% endfor %}
    </div>
    {% endfor %}
    </div>
</html>