---
layout: page
title: Blog
---
## Blog Posts



### Anything that I studied or found interesting is here!



{% for post in site.posts %}

* {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}

