---
title: "Git Blog"
layout: category
permalink: categories/blog
author_profile: false
sidebar_main: true
---


{% assign posts = site.categories.blog %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}