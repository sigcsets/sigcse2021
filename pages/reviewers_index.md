---
layout: page
title: "For Reviewers"
meta_title: "Information for Reviewers for SIGCSE TS 2021"
permalink: "/reviewers/"
sidebar: reviewers
---

We have broken out submission guidelines by type. There are many ways to share the excellent work you are doing, and we would encourage you to consider all of them as you think about what would make the best vehicle for sharing your efforts with the larger community.

<h2>
	<p>Follow the links below for detail information about submission guidelines to the submission type.</p>
<ul>
    {% assign posts = site.reviewers | sort: 'order' %}
    {% for post in posts %}
    <li><a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
