---
layout: default
title: Engineering Blog
description: Follow our robotics journey through design, build, and code
---

<!-- Page Header -->
<section class="page-header">
    <div class="container">
        <h1>Engineering Blog</h1>
        <p>Our journey through design, build, and code</p>
    </div>
</section>

<!-- Blog Posts List -->
<section class="blog-section">
    <div class="container">
        {% for post in site.posts %}
        <article class="blog-post">
            <div class="post-header">
                <span class="post-category">{{ post.category }}</span>
                <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
            </div>
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <div class="post-author">By {{ post.author | default: site.team.name }}</div>
            <div class="post-excerpt">
                {{ post.excerpt }}
            </div>
            <a href="{{ post.url | relative_url }}" class="btn btn-primary">Read More</a>
            
            {% if post.tags %}
            <div class="post-tags">
                {% for tag in post.tags %}
                <span class="tag">{{ tag }}</span>
                {% endfor %}
            </div>
            {% endif %}
        </article>
        {% endfor %}
        
        {% if site.posts.size == 0 %}
        <div class="no-posts">
            <h3>No posts yet!</h3>
            <p>Check back soon for updates from our engineering team.</p>
        </div>
        {% endif %}
    </div>
</section>

