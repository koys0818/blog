---
layout: post
title: 리녹스 명령어 정리
date: 2020-01-02 17:21:29
author: 고유성
categories: summary
short_description: 리녹스 명령어 공부하며 정리하기
image_preview: http://image.itdonga.com/files/2015/04/09/e5.jpg
#external_url: https://habrahabr.ru/post/278937/
---
리녹스는 모든 명령어는 명령어 뒤에 --help 옵션을 주면 자세한 사용 방법이 나온다.

예를들어 ls 명령어의 자세한 사용 방법과 모든 옵션을 알고싶으면 ls –help를 입력하면 된다.

pwd (print working directory)
현재 작업중인 디렉토리 정보 출력


**cd (change directory)**
경로 이동

절대 경로와 상대 경로로 이동 가능하다.


ls (list)
디렉토리 목록 확인

cp (copy)
파일 혹은 디렉토리를 복사

디렉토리를 복사할때는 -r 옵션을 주어야함

mv (move)
파일 혹은 디렉토리 이동

실제로 원하는 위치로 이동할때도 사용하지만, 이름을 변경하는 용도로도 사용한다.

cp와는 달리 디렉토리를 이동할때도 별다른 옵션이 필요 없다.

mkdir (make directory)
디렉토리 생성

-p 옵션을 주면 하위 디렉토리까지 한 번에 생성 가능

아래 예제중 ls -R 옵션은 디렉토리의 하위목록까지 전부 보여주는 옵션이다.


rm (remove)
파일이나 디렉토리를 삭제

디렉토리를 삭제할때는 r 옵션을 주어야 한다.

-f 옵션을 주면 사용자에게 삭제 여부를 묻지 않고 바로 삭제한다.
