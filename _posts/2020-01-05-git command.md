---
layout: post
title: git 명령어 정리
date: 2020-01-05 14:28:23
author: 고유성
categories: summary
short_description: git 명령어 공부하며 정리
image_preview: https://miro.medium.com/max/910/1*BCZkmZR1_YzDZy22Vn4uUw.png
#external_url: https://habrahabr.ru/post/278937/
---
전역 사용자명/이메일 구성하기

~~~
git config - -global user.name “Your name”
git config - -global user.email “Your email address”
~~~

새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기

~~~
git add <파일>
git commit -m "<메세지>"
~~~

전역 설정 정보 조회

~~~
git config - -global - -list
~~~

저장소별 설정 정보 조회
~~~
git config - -list
~~~

저장소 복제하기
~~~
git clone <저장소 url>
~~~

git 생성하기
~~~
git init 
~~~

변경된 내용 푸쉬(발행)하기
~~~
git push
~~~
