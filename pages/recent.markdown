---
layout: page
title: Recent Content
permalink: /recent/
description: Explore the latest published study materials on Rana's Study Notes.
---

<section class="recent-page">

  <div class="subject-intro">
    <span class="subject-icon">🕒</span>
    <h2>Recently Published Materials</h2>
    <p>
      Explore the latest published question papers,
      answer papers and study notes.
    </p>
  </div>

  <div class="recent-content-list">

    {% assign published_materials = site.pages | where: "published", true | sort: "date" | reverse %}

    {% assign material_count = 0 %}

    {% for item in published_materials %}

      {% if item.url contains "/classes/class-" %}

        {% assign material_count = material_count | plus: 1 %}

        {% if material_count <= 20 %}

          <a href="{{ item.url | relative_url }}" class="search-result-card">

            <h3>{{ item.title }}</h3>

            <p>{{ item.description | default: "Explore this study material." }}</p>

            <span class="recent-meta">
              {{ item.class }} · {{ item.subject }} · {{ item.content_type }}
            </span>

          </a>

        {% endif %}

      {% endif %}

    {% endfor %}

    {% if material_count == 0 %}

      <p class="empty-message">
        No published study materials are available yet.
        Please check back later.
      </p>

    {% endif %}

  </div>

</section>
