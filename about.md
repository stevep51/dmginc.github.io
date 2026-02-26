---
layout: page
title: About
permalink: /about/
---

{{ site.data.site_text.about.intro }}

{{ site.data.site_text.about.heading }}

{% for item in site.data.site_text.about.bullets %}
- {{ item }}
{% endfor %}

{{ site.data.site_text.about.outro }}
