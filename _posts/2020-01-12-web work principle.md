---
layout: post
title: 웹페이지 작동 원리
date: 2020-01-12 9:26:48
author: 고유성
categories: summary
short_description: 웹페이지가 작동하는 원리를 쉽게 정리
image_preview: http://tcpschool.com/lectures/img_webbasic_10.png
#external_url: https://habrahabr.ru/post/278937/
---
우선 아래에 사용될 헷갈릴만한 용어를 정리하면 

DNS

Domain Name System Servers (도메인 이름 시스템 서버)

   - 웹 사이트를 위한 주소록

   - 브라우저가 웹사이트를 검색하기 전에 살펴보는 곳

HTTP 

   - Hypertext Transfer Protocol (하이퍼텍스트 전송 규약)

   - 클라이언트와 서버가 서로 통신할 수 있게 하기 위한 언어를 정의하는 어플리케이션 규약


웹의 동작 원리


~~~
먼저 사용자가 웹브라우저를 통해 찾고 싶은 웹 페이지의 URL 주소를 입력하면

사용자가 입력한 주소의 도메인을 DNS서버에 검색하고

DNS 서버에서 해당 도메인을 검색해 IP 주소와 사용자가 입력한 URL의 정보를 전달한다

그리고 받은 IP 주소와 URL 정보는 HTTP 요청 메세지가 생성되서 인터넷을 거쳐 해당 IP 주소의 컴퓨터로 전송된다

도착한 HTTP 요청 메시지는 HTTP 프로토콜을 사용하여 웹 페이지 URL 정보로 변환되고

웹서버는 도착한 웹페이지 URL 정보를 검색하여

다시 HTTP 프로토콜을 사용하여 HTTP 응답 메시지를 생성하고

이렇게 생성된 HTTP 응답 메시지는 TCP 프로토콜을 사용하여 인터넷을 거쳐 원래 컴퓨터로 전송되어

도착한 HTTP 응답 메시지는 HTTP 프로토콜을 사용하여 웹 페이지 데이터로 변환된 후

웹 브라우저에 의해 출력되어 사용자가 볼 수 있게 된다
~~~


쉽게 줄이면 


사용자가 정보 입력 -> 정보를 검색해서 다시 돌려줌 -> 정보를 변환해서 인터넷을 이용하여 해당 웹 서버에 전달

 -> 웹 서버에서 웹 페이지의 정보를 전달 -> 웹 페이지의 데이터를 다시 변환하여 인터넷을 이용하여 사용자에게 전달

 이 된다 

