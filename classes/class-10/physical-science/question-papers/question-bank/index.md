---
layout: page
title: Physical Science Question Bank
permalink: /classes/class-10/physical-science/question-papers/question-bank/
description: Class 10 Physical Science question bank.
---

<section class="subject-page">

  <div class="subject-intro">
    <span class="subject-icon">📚</span>
    <h2>Physical Science Question Bank</h2>
    <p>
      Explore Class 10 Physical Science questions from the Question Bank.
    </p>
  </div>

  <div class="question-bank-list">

    <h2>Model Question Papers</h2>

    {% assign question_sets = site.pages
      | where: "source", "question-bank"
      | where: "published", true
      | sort: "paper_number"
    %}

    {% for item in question_sets %}
      {% if item.subject == "physical-science" and item.paper_type == "model-paper" %}

        <div class="question-set-card">
          <h3>
            <a href="{{ item.url | relative_url }}">
              {{ item.title }}
            </a>
          </h3>

          <p>
            Full question paper · {{ item.total_marks }} Marks · {{ item.duration }}
          </p>
        </div>

      {% endif %}
    {% endfor %}

  </div>

</section>
