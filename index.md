---
layout: page
title: RennesDevOps
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li>
		<div class="leftbox">
			<span class="arrow">&nbsp;</span>
			<span class="datebox">{{ post.date | date_to_string }}</span>
			<div class="avatarbox">
				<img src="http://lorempixel.com/56/56/people"><br>
				{{ post.author }}
			</div>
			<div class="commentbox">
				<span class="nbr-comments">0</span>
				<br>
				Comments
			</div>
		</div>
		<div class="rightbox">
			<a href="{{ BASE_PATH }}{{ post.url }}">
				<h1>{{ post.title }}</h1>
				<p>{{ post.excerpt }}</p>
			</a>
			<div class="tagsbox">
				TAGS : 
				{% for tag in post.tags %}
				<a href="/tags.html#{{ tag }}">{{ tag }}</a>&nbsp;
				{% endfor %}
			</div>
		</div>
	</li>
  {% endfor %}
</ul>