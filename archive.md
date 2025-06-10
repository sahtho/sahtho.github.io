---
layout: default           # ใช้ layout หลักของเว็บไซต์ (default)
title: บทความทั้งหมด      # หัวข้อของหน้า Archive
permalink: /archive.html # (Optional) กำหนด URL ที่ชัดเจนว่าจะเป็น /archive.html
---

<div class="archive">
  <h1>{{ page.title }}</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <h2>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h2>
      </li>
    {% endfor %}
  </ul>
</div>