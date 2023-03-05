---
title: 개발자 블로그 3. 꿀팁.
date: 2023-02-04 21:21:00 +0800
categories: [블로그, 블로그 만들기]
tags: [개발자 블로그]
math: true
mermaid: true
pin : false
image:
  path: /images/2023-02-04-start-github-blog/thumbnail.png
  alt: 개발자 블로그 2. 깃허브 블로그 내맘대로 바꾸기.
---
<!-- 소제목 -->
> ## 하이라이트 태그 무시
> 하려고 보니까 마음에 드는 템플릿이 없네..?!
> {: style="color:gray; font-size: 85%; text-align: left;"}

```html
---
layout: page
# The Home page layout
---

...생략

<div id="post-list">
  <div class="post-preview">
    <div style="display:grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); grid-gap: 25px;">
      {% raw %}
      {% for post in posts %}
        <div style="width: auto; height: 340px;">
          <div style="height: 70%; position: relative; overflow: hidden;">
            <img src="{{ post.image.path }}" alt="썸네일">
          </div>
          <div style="height: 3%;"></div>
          <div style="height: 25%;">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a><br>
            {% include datetime.html date=post.date %}
            {% if post.pin %}
              <i class="fas fa-thumbtack fa-fw"></i>
            {% endif %}
          </div>
        </div>
      {% endfor %}
      {% endraw %}
    </div>
  </div>
</div> <!-- #post-list -->

```
{: file='프로젝트명/_layout/home.html'}

&#37;

