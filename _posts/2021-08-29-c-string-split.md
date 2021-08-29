---
title:  "string 문자열 분리"
excerpt: "string 문자열 나누기"

categories: cpp
tags: cpp
---

string 라이브러리의 문자열인 분리

띄어쓰기로 구분되는 string type의 문자열이 들어오는 경우


	
	
	
	
	
	
#include \<string\>


void main()
{


    string str = "123 456 789";
    string string123;
    string string456;
    string string789;

	// ' ' 문자열의 위치를 찾아서 시작 위치부터 해당 문자열까지 문자열을 분리
    int stringPositionStart = 0;
    int stringPositionEnd = str.find(' ', stringPositionStart);
    string123 = str.substr(stringPositionStart, stringPositionEnd);

	// ' ' 이전 자른 위치의 마지막을 새로운 문자열의 시작 위치로 해서 다시 자른다.
    stringPositionStart = stringPositionEnd + 1;
    stringPositionEnd = str.find(' ', stringPositionStart);
    string456 = str.substr(stringPositionStart, stringPositionEnd- stringPositionStart);

    stringPositionStart = stringPositionEnd + 1;
    stringPositionEnd = str.find(' ', stringPositionStart);
	// 마지막문자열의 경우 찾고자하는 문자열을 찾지 못한 경우 -1이 반환되므로 시작위치부터 마지막 까지 잘라주면 원하는 문자열 값을 얻을 수 있다.
    if (stringPositionEnd < 0)
    {
        string789 = str.substr(stringPositionStart);
    }
    else
    {
        string789 = str.substr(stringPositionStart, stringPositionEnd - stringPositionStart);
    }
     
    return;
}

![substr](https://user-images.githubusercontent.com/84770786/131251434-925e5fe8-41f2-45b6-9ae9-dc31aeba6c3e.JPG)