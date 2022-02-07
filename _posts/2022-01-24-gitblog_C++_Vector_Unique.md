---
title:  "Vector 중복 제거"
excerpt: "erase, unique"

categories:
  - cpp
tags:
  - cpp
last_modified_at: 2022-02-04
---

vector 원소의 중복 제거

vector<int> test;
test.erase(unique(test.begin(), test.end()), test.end());

주의할 점
1) 연속된 원소의 중복만을 제거하므로 정렬 후 제거한다.

#include<algorithm> 이 필요