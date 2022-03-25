---
layout: splash
permalink: /
author_profile: true
hidden: true
header:
  image: assets/images/home.gif
feature_row:
  - image_path: /assets/images/home/autolayout.png
    alt: "autolayout"
    title: "Auto Layout"
    excerpt: "iOS Auto Layout에 대해 정리한 포스트를 올리고 있습니다."
    url: "/categories/autolayout/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
  - image_path: /assets/images/home/apple.png
    alt: "iosapp"
    title: "iOS App"
    excerpt: "테이블뷰를 활용하여 간단한 iOS앱을 만들어 보려고 합니다."
    url: "/categories/iosapp/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
  - image_path: /assets/images/home/python.png
    alt: "python"
    title: "Python"
    excerpt: "파이썬에 대해 공부한 내용을 올리고 있습니다."
    url: "/categories/python/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
  - image_path: /assets/images/home/web.png
    alt: "web"
    title: "HTML & CSS"
    excerpt: "HTML과 CSS에 대해 공부한 내용을 올리고 있습니다."
    url: "/categories/web/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
  - image_path: /assets/images/home/swift.png
    alt: "swift"
    title: "Swift"
    excerpt: "Swift 문법을 정리한 포스트를 올리고 있습니다."
    url: "/categories/swift/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
  - image_path: /assets/images/home/etc.png
    alt: "etc"
    title: "etc"
    excerpt: "그 외 기타 포스트들입니다."
    url: "/categories/etc/"
    btn_class: "btn--inverse"
    btn_label: "Go →"
---

<!-- 카테고리 -->

<!-- {% include feature_row %} -->

<!-- 최근 포스트 -->

{{ content }}

<h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>

{% if paginator %}
{% assign posts = paginator.posts %}
{% else %}
{% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}

<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}
