---
layout: page
permalink: /repositories/
title: repositories
description: GitHub statistics and repository showcase
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub Statistics

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

## Top Languages

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
  <div class="repo p-2 text-center">
    <a href="https://github.com/{{ user }}">
      <img
        class="repo-img-light w-100"
        alt="{{ user }} - Top Languages"
        src="https://github-readme-stats.vercel.app/api/top-langs/?username={{ user }}&theme={{ site.repo_theme_light }}&layout=compact&langs_count=8"
      >
      <img
        class="repo-img-dark w-100"
        alt="{{ user }} - Top Languages"
        src="https://github-readme-stats.vercel.app/api/top-langs/?username={{ user }}&theme={{ site.repo_theme_dark }}&layout=compact&langs_count=8"
      >
    </a>
  </div>
  {% endfor %}
</div>

---

## GitHub Streak Stats

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
  <div class="repo p-2 text-center">
    <a href="https://github.com/{{ user }}">
      <img
        class="repo-img-light w-100"
        alt="{{ user }} - GitHub Streak"
        src="https://github-readme-streak-stats.herokuapp.com/?user={{ user }}&theme={{ site.repo_theme_light }}"
      >
      <img
        class="repo-img-dark w-100"
        alt="{{ user }} - GitHub Streak"
        src="https://github-readme-streak-stats.herokuapp.com/?user={{ user }}&theme={{ site.repo_theme_dark }}"
      >
    </a>
  </div>
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}

## GitHub Trophies

{% for user in site.data.repositories.github_users %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>
{% endfor %}

---

{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## Featured Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
