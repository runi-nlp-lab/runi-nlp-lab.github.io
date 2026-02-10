---
title: RUNI NLP Lab
---

<div style="display: flex; align-items: center; justify-content: space-between; gap: 20px; flex-wrap: wrap; margin-bottom: 40px;">
  <div style="flex: 1; min-width: 250px;">
    <h1>Welcome to RUNI NLP Lab</h1>
    <p class="lead">Led by <strong>Dr. Kfir Bar</strong>, we are a research group at Reichman University focused on Natural Language Processing.</p>
    <p>Our research explores the intersection of languages and computation, focusing on low-resource languages, LLM understanding, and text generation.</p>
  </div>
  <div>
    <!-- Placeholder for Lab Image or Logo -->
    <img src="/assets/logo.png" alt="RUNI NLP Lab" style="width: 200px; border-radius: 12px; margin-top: 5px;" />
  </div>
</div>

<hr>

## 📰 News
<div class="news-section">
  {% for post in site.posts limit:3 %}
  <div style="margin-bottom: 15px;">
    <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%b %d, %Y" }}</span>
    <br>
    <a href="{{ post.url }}" style="font-weight: bold; font-size: 1.1em;">{{ post.title }}</a>
  </div>
  {% endfor %}
</div>

<hr>

## 🗓️ Upcoming Events
<div class="events-section">
  <!-- Static events list for now -->
  <div style="margin-bottom: 15px;">
    <strong>Weekly Lab Meeting</strong><br>
    Every Wednesday at 14:00 <br>
    <span style="color: #666;">Room A204 / Zoom</span>
  </div>
</div>

<hr>

## 📍 Find Us
<div style="margin-top: 20px; display:flex; gap:40px; align-items:center; flex-wrap: wrap;">
  
  <a
    href="mailto:kai.golanhashiloni@post.runi.ac.il?subject=Inquiry%20RUNI%20NLP"
    aria-label="Email Lab Director"
    style="display:inline-flex; align-items:center; gap:8px; padding:10px 14px; background:#2d9f6e; color:#fff; text-decoration:none; border-radius:8px; font-weight:600;"
  >
    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" aria-hidden="true" xmlns="http://www.w3.org/2000/svg">
      <path d="M4 6.5C4 5.67 4.67 5 5.5 5H18.5C19.33 5 20 5.67 20 6.5V17.5C20 18.33 19.33 19 18.5 19H5.5C4.67 19 4 18.33 4 17.5V6.5Z" stroke="white" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M21 6L12 13L3 6" stroke="white" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
    Email Kai Golan Hashiloni
  </a>

  <div style="font-size: 1.1em;">
    <strong>RUNI NLP Lab</strong><br>
    Reichman University<br>
    Herzliya, Israel
  </div>

</div>

