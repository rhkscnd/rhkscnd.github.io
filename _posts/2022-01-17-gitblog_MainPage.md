---
title:  "Main Page"
excerpt: "Category 페이지 주소 변경"

categories:
  - Blog
tags:
  - Blog
last_modified_at: 2022-01-17M08:06:00-05:00
---

현재 메인페이지에 있는 Category를 클릭할 경우 not Found 페이지가 나온다.

현재 categories/ 페이지는 빈 페이지이기 때문이다.

클릭 시 이동하는 페이지를 변경하려면, Git이 설치된 폴더에 _data/navigation.yml 파일을 수정해주면 된다.

아래 내용을 참조하자

main:
  - title: "Categories"
    url: /categories/cpp
  - title: "Tags"
    url: /tags/
  - title: "About"
    url: /about/
  - title: "연도별 포스트"
    url: /posts/