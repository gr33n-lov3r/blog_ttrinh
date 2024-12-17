---
layout: page
title: Home
id: home
permalink: /
---

# Hello, welcome!

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>

My name is Tam Trinh, and I'm a learning cyber professional/SOC analyst. On this blog, you'll find my portfolio of write-ups relevant to my homelabs and 

I haven't maintained a website in about a decade, so this site won't be very effective or aesthetically pleasing to navigate for a little while. I'm using [this template](https://github.com/maximevaillancourt/digital-garden-jekyll-template) to jumpstart my blog. For the time being, all my posts are lumped together below.

The easiest way to get started is to read this [step-by-step guide explaining how to set this up from scratch](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

<strong>Recent blog posts</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
