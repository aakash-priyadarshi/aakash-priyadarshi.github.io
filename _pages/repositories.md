---
layout: page
permalink: /repositories/
title: repositories
description: GitHub statistics and repository showcase
nav: true
nav_order: 4
---

## GitHub Profile Overview

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <div class="repo p-2 text-center w-100">
    <a href="https://github.com/aakash-priyadarshi">
      <img
        class="repo-img-light w-100"
        alt="aakash-priyadarshi - GitHub Stats"
        src="https://github-readme-stats.vercel.app/api/?username=aakash-priyadarshi&theme={{ site.repo_theme_light }}&show_icons=true&hide_border=true&include_all_commits=true&count_private=true"
      >
      <img
        class="repo-img-dark w-100"
        alt="aakash-priyadarshi - GitHub Stats"
        src="https://github-readme-stats.vercel.app/api/?username=aakash-priyadarshi&theme={{ site.repo_theme_dark }}&show_icons=true&hide_border=true&include_all_commits=true&count_private=true"
      >
    </a>
  </div>
</div>

---

## Contribution Activity

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <div class="repo p-2 text-center w-100">
    <a href="https://github.com/aakash-priyadarshi">
      <img
        class="repo-img-light w-100"
        alt="aakash-priyadarshi - GitHub Streak"
        src="https://github-readme-streak-stats.herokuapp.com/?user=aakash-priyadarshi&theme={{ site.repo_theme_light }}&hide_border=true"
      >
      <img
        class="repo-img-dark w-100"
        alt="aakash-priyadarshi - GitHub Streak"
        src="https://github-readme-streak-stats.herokuapp.com/?user=aakash-priyadarshi&theme={{ site.repo_theme_dark }}&hide_border=true"
      >
    </a>
  </div>
</div>

---

## Top Languages

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <div class="repo p-2 text-center w-100">
    <a href="https://github.com/aakash-priyadarshi">
      <img
        class="repo-img-light w-100"
        alt="aakash-priyadarshi - Top Languages"
        src="https://github-readme-stats.vercel.app/api/top-langs/?username=aakash-priyadarshi&theme={{ site.repo_theme_light }}&layout=compact&langs_count=10&hide_border=true"
      >
      <img
        class="repo-img-dark w-100"
        alt="aakash-priyadarshi - Top Languages"
        src="https://github-readme-stats.vercel.app/api/top-langs/?username=aakash-priyadarshi&theme={{ site.repo_theme_dark }}&layout=compact&langs_count=10&hide_border=true"
      >
    </a>
  </div>
</div>

---

## Contribution Graph

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <div class="repo p-2 text-center w-100">
    <a href="https://github.com/aakash-priyadarshi">
      <img
        class="repo-img-light w-100"
        alt="aakash-priyadarshi - Contribution Graph"
        src="https://github-readme-activity-graph.vercel.app/graph?username=aakash-priyadarshi&theme=github-light&hide_border=true"
      >
      <img
        class="repo-img-dark w-100"
        alt="aakash-priyadarshi - Contribution Graph"
        src="https://github-readme-activity-graph.vercel.app/graph?username=aakash-priyadarshi&theme=github-dark&hide_border=true"
      >
    </a>
  </div>
</div>

---

{% if site.repo_trophies.enabled %}

## GitHub Trophies

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username="aakash-priyadarshi" %}
</div>

---

{% endif %}

{% if site.data.repositories.github_repos %}

## Featured Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
