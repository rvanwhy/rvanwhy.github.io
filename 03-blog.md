---
layout: default
current: Non-math Writing
permalink: blog.html
---

This is where I will sporadically post non-math writings.
I go through phases of writing, deleting, and not-writing.

<style>
.blog-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 40px;
  align-items: start;

  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 25px;
}

  .blog-post {
    padding: 15px;
  }

  @media (max-width: 768px) {
    .blog-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="blog-grid">

{% for post in site.posts %}

  <article class="blog-post">
    <h1>{{ post.title }}</h1>
    <h4>{{ post.date | date: '%B %d, %Y' }}</h4>

    {{ post.content }}
  </article>

{% endfor %}

</div>