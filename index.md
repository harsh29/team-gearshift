---
layout: default
title: Home
---

<!-- Hero Section -->
<section class="hero">
    <div class="hero-content">
        <h1 class="hero-title">Team {{ site.team.number }}<br><span class="accent">{{ site.team.name | upcase }}</span></h1>
        <p class="hero-subtitle">Building Tomorrow's Innovations Today</p>
        <p class="hero-description">A passionate team of middle school students competing in FIRST LEGO League</p>
        <div class="hero-buttons">
            <a href="{{ '/about' | relative_url }}" class="btn btn-primary">Meet the Team</a>
            <a href="{{ '/blog' | relative_url }}" class="btn btn-secondary">Engineering Blog</a>
        </div>
    </div>
    <div class="hero-image">
        <div class="robot-illustration">🤖</div>
    </div>
</section>

<!-- Season Info -->
<section class="season-info">
    <div class="container">
        <h2>{{ site.team.season }} Season</h2>
        <div class="season-grid">
            <div class="season-card">
                <div class="icon">🎯</div>
                <h3>Our Mission</h3>
                <p>Designing innovative solutions to real-world challenges through robotics and teamwork</p>
            </div>
            <div class="season-card">
                <div class="icon">⚙️</div>
                <h3>Robot Design</h3>
                <p>Engineering a competitive robot using LEGO SPIKE Prime and custom mechanisms</p>
            </div>
            <div class="season-card">
                <div class="icon">🏆</div>
                <h3>Competition</h3>
                <p>Competing for awards in Robot Game, Innovation Project, and Core Values</p>
            </div>
        </div>
    </div>
</section>

<!-- Latest Blog Posts -->
<section class="latest-posts">
    <div class="container">
        <h2>Latest from Our Engineering Blog</h2>
        <div class="blog-grid">
            {% for post in site.posts limit:3 %}
            <article class="blog-card">
                <div class="blog-date">{{ post.date | date: "%b %d, %Y" }}</div>
                <h3>{{ post.title }}</h3>
                <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
            </article>
            {% endfor %}
        </div>
        <div class="center-button">
            <a href="{{ '/blog' | relative_url }}" class="btn btn-primary">View All Posts</a>
        </div>
    </div>
</section>

<!-- Call to Action -->
<section class="cta" id="contact">
    <div class="container">
        <h2>Want to Learn More?</h2>
        <p>Follow our journey as we compete in FIRST LEGO League!</p>
        <div class="contact-info">
            <p>📧 Email: {{ site.team.email }}</p>
            <p>📍 Location: {{ site.team.location }}</p>
        </div>
    </div>
</section>

