---
title:  "Category 메뉴 생성"
excerpt: "Category 메뉴 생성하기"

categories:
  - Blog
tags:
  - Blog
last_modified_at: 2022-01-17M08:06:00-05:00
---

포스트를 등록할 경우 카테고리를 입력하자. 해당 카테고리만응 따로 구분해서 확인할 수 있다.

새로운 카테고리 추가 방법

_includes/nav_list_main 파일의 내부구조 변경

<span class="nav__sub-title">Blog</span>	// 타이틀
            <ul>
                {% for category in site.categories %}
                    {% if category[0] == "Blog" %}	// 세부 항목
                        <li><a href="/categories/blog" class="">Git Blog({{category[1].size}})</a></li>	//이동할 주소
                    {% endif %}
                {% endfor %}
            </ul>
			
새로운 카테고리 생성시 아래 메뉴에 입력해 주면 메인 메뉴에 새롭게 생성된다.