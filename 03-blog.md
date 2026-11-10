---
layout: default
current: Non-math Writing
permalink: blog.html
---
<div class="special jumbotron">

<p> This is where I will sporadically post non-math writings.
I go through phases of writing, deleting, and not-writing.</p>

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

  @media (max-width: 768px) {
    .blog-grid {
      grid-template-columns: 1fr;
    }
  }

    .blog-post {
  font-size: 21px;
  line-height: 1.5;
  padding: 15px;
}

.blog-post p {
  font-size: inherit;
}

.blog-post h1 {
  font-size: 2rem;
}

.blog-post h4 {
  font-size: 1rem;
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

</div>