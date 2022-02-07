---
title:  "C언어 다차원 배열 동적 생성"
excerpt: "다차원 배열 동적 생성"

categories:
  - c
tags:
  - c
last_modified_at: 2022-02-07
---

C언어 다차원 배열 동적 생성 및 초기화

    int** ArrayResult = (int**)malloc(cnt * sizeof(int));
    
    for (int i = 0; i < cnt; i++)
    {
        ArrayResult[i] = (int*)malloc(cnt * sizeof(int));

        for (int j = 0; j < cnt; j++)
        {
            ArrayResult[i][j] = 0;      //초기화
        }
    }

	free(*ArrayResult);
	free(ArrayResult);

malloc의 짝으로 free도 두번 해줘야 한다.

순서에 유의!