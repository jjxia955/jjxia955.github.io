---
title: Publications
layout: page
---

For the most up-to-date list, see my [Google Scholar profile](https://scholar.google.com/citations?user=FWu4_iIAAAAJ&hl=en).

{% for section in site.data.publications %}
## {{ section.section }}

{% for item in section.items %}
### {{ item.title }}
{{ item.authors | markdownify | remove: '<p>' | remove: '</p>' }}

{% if item.venue %}*{{ item.venue }}*{% if item.details %} {{ item.details }}{% endif %} ({{ item.year }}).{% else %}{{ item.year }}.{% endif %}{% if item.link_url %} [{{ item.link_label }}]({{ item.link_url }}){% endif %}

{% endfor %}
{% endfor %}
