---
layout: post
title: 자바로 블랙잭 프로그램 작성하기
date: 2019-12-31 13:18:23
author: 고유성
categories: posts
short_description: 블랙잭 게임을 자바로 작성하기
image_preview: https://kangwonland.high1.com/site/casino/images/contents/cst_1764_img.jpg
#external_url: https://habrahabr.ru/post/278937/
---
블랙잭의 규칙은 딜러와 카드를 한장씩 받아 21에 가까운 수를 만드는 사람이 이기며 21을 초과하면 지는 것이니
while문을 써서 21을 초과하면 결과를 출력하고 종료하고 만들었고 받는 카드의 값은 랜덤값으로 출력되게 해놨고
처음에 돈을 1000원으로 세팅해 매판 돈을 배팅하고 돈이 0이 되면 프로그램을 종료하게 해놨고 이기면 배팅한 금액의 2배를 받게 세팅했다
~~~
package practice;
import java.util.Random;
import java.util.Scanner;
public class Blackzack2 {
public static void main(String[] args) {
Scanner scan = new Scanner(System.in);
int player, dealer;
dealer = 0;
player = 0;
Random random = new Random();
int a, i = 0, j;
int money = 1000;
int yes = 1;
int betting;
int end = 2;
int x = 0;
while(end == 2 || money <= 0)
{
dealer = 0;
player = 0;
yes = 1;
System.out.println("현재 잔액은 "+money+"입니다\n얼마를 배팅하시겠습니까?");
betting = scan.nextInt(); //배팅액 입력
while(dealer <= 20) //딜러의 숫자 랜덤으로 출력
{
i = (int)(Math.random()*10);
dealer = dealer + i;
}
dealer = dealer - i;
System.out.println("블랙잭을 시작합니다.\n");
while(yes == 1 && player <21)
{
System.out.println("현재 카드의 합: "+player+"\n HIT하시겠습니까?");
yes = scan.nextInt();
i = (int)(Math.random()*10); // 플레이어의 카드 랜덤값으로 출력
if(i == 1)
{
System.out.println("에이스가 나왔습니다 1로 계산하시겠습니까 11로 계산하시겠습니까?");
i = scan.nextInt();
}
player = player + i;
}
if(yes == 2)
{
player = player - i;
}
if(player >21)
{
System.out.println(player +"으로 버스트 되셨습니다 게임에서 패배했습니다"); //블랙잭 규칙대로 21 넘으면 패배
}
else
{
System.out.println("딜러의 합 : "+dealer+"\n플레이어의 합 : "+player);
if(dealer < player)
{
System.out.println("플레이어가 승리하였습니다 배당금의 2배를 받습니다.");
x = 1;
}
if(dealer > player)
{
System.out.println("플레이어가 패배하셨습니다 배당금을 잃습니다.");
x = 2;
}
if(dealer == player)
{
System.out.println("무승부입니다 배당금을 돌려받습니다.");
x = 3;
}
}
if(x == 1)
{
money = money + betting;
}
if(x == 2)
{
money = money - betting;
}
System.out.println("게임을 종료하시겠습니까?");
end = scan.nextInt(); // end를 1로 치면 while문 깨지면서 종료
if(end == 1)
{
break;
}
}
System.out.println("게임이 종료되었습니다\n잔액은 "+money+"입니다."); //마지막 결과 정리
// TODO Auto-generated method stub
}
}
~~~