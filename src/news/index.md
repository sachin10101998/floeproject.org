---
layout: layouts/default
permalink: newsindex.html
---
<div id="content" class="floe-content">
<div class="flc-toc-tocContainer toc"> </div>
<h2> News </h2>
<div class="floe-news-archive">
<ul >
{%- for post in collections.post reversed -%}
<li><a href="{{ '/' | url }}{{ post.data.permalink }}"><p> {{ post.data.title }}</p></a>
<time class="floe-date" datetime="{{ post.data.date | w3DateFilter }}">{{ post.data.date | dateFilter }}</time>
</li>
{%- endfor -%}
</ul>
</div>
</div>