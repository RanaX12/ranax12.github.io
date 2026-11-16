---
layout: page
title: Classes
permalink: /classes/
description: Explore study materials by class.
---

<section class="classes-page">

  <div class="classes-intro">
    <h2>Explore Classes</h2>
    <p>
      Choose your class to explore study notes,
      learning resources and academic materials.
    </p>
  </div>

  <div class="classes-grid">

    {% assign class_numbers = "5,6,7,8,9,10" | split: "," %}

    {% for class_number in class_numbers %}

      <a
        href="{{ '/classes/class-' | append: class_number | append: '/' | relative_url }}"
        class="class-card"
      >

        <div class="class-icon">🎓</div>

        <div class="class-info">
          <h3>Class {{ class_number }}</h3>
          <p>Explore study materials and notes.</p>
        </div>

        <span class="class-arrow">→</span>

      </a>

    {% endfor %}

  </div>

</section>

