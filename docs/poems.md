---
layout: secondary_pages
title: Poems
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<h1 class="gallery-header dark-blue">Poems</h1>
<div class="gallery-container">
    <hr />
        {% assign sorted_array = site.writing | sort: "start_date" | reverse %}
        {% for item in sorted_array %}
            {% if item.type == 'poem' %}
            <div class="gallery-item">
            <h3><p class="gallery-item__title">{{ item.title }}</p></h3>
                <p>Date: {{ item.date | date: "%d-%m-%Y" }}</p>
                <p class="gallery-item__text">Description: {{ item.subtitle }}</p>
                <p class="gallery-item__text">Topic: {{ item.topics }}</p>
                <a href="{{ item.url }}">
                    <div class="gallery-item__link">
                        <span>Read More</span>
                        <img class="gallery-item__arrow" src="" height=25em>
                    </div>
                </a>
                <hr />
                <br>
            </div>
            {% endif %}
	    {% endfor %}
</div>