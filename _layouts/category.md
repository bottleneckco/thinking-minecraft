---
layout: page
---

<div class="blog list">
  <h4>Filed Under "{{ page.tag }}"</h4>

  <ul class="post-list">
    {% for post in site.categories[page.tag] %}
        {% include post_preview.html %}
    {% endfor %}
  </ul>
</div>
