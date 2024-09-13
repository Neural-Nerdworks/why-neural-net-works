---
layout: default
title: Home
---

<section class="hero">
    <p>We are a group of individuals working on this website to better present you how and</p>
    <h2>Why Neural Net-Works</h2>
</section>

<section class="team">
    <h2>Meet Our Team</h2>
    <div class="team-members">
        <div class="member">
            <img src="{{ '/assets/imgs/team/rusen.png' | relative_url }}" alt="Member 1">
            <h3>Ruşen Birben</h3>
            <p>Coffee Lover.</p>
        </div>
        <div class="member">
            <img src="{{ '/assets/imgs/team/gokturk.png' | relative_url }}" alt="Member 2">
            <h3>Göktürk Dervişoğlu</h3>
            <p>Anime Lover.</p>
        </div>
        <div class="member">
            <img src="{{ '/assets/imgs/team/anil.png' | relative_url }}" alt="Member 3">
            <h3>Anıl Dervşioğlu</h3>
            <p>Algorithm Lover.</p>
        </div>
        <div class="member">
            <img src="{{ '/assets/imgs/team/busra.png' | relative_url }}" alt="Member 4">
            <h3>Büşra Şahin</h3>
            <p>Naruto Lover.</p>
        </div>
    </div>
</section>

<section class="projects">
    <h2>Our Projects</h2>
    <div class="projects-grid">
        {% for project in site.projects %}
        <div class="project">
            <a href="{{ project.url | relative_url }}">
                <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
                <h3>{{ project.title }}</h3>
                <div class="tags">
                    {% for tag in project.tags %}
                    <span class="tag" style="background-color:{{ tag.color }}">{{ tag.name }}</span>
                    {% endfor %}
                </div>
            </a>
        </div>
        {% endfor %}
    </div>
</section>
