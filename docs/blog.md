---
layout: secondary_pages
title: Blog
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<h1 class="gallery-header dark-blue">Blog</h1>
<div class="gallery-container">
<hr />
	{% assign sorted_array = site.blog | sort: "start_date" | reverse %}
	{% for blog in sorted_array %}
    <div class="gallery-item">
    <h3><p class="gallery-item__title">{{ event.title }}</p></h3>
        <p>Starting: {{ blog.date | date: "%d-%m-%Y" }} @ {{ blog.start_time }}</p>
        <p class="gallery-item__text">Description: {{ blog.subtitle }}</p>
        <p class="gallery-item__text">Topic: {{ blog.topics }}</p>
        <a href="{{ blog.url }}">
            <div class="gallery-item__link">
                <span>Read More</span>
                <img class="gallery-item__arrow" src="../logos/travel.svg" height=25em>
            </div>
        </a>
<hr />
<br>
</div>
	{% endfor %}
</div>