---
layout: post
title: 자바 연습 01
date: 2020-01-02 17:21:29
author: 고유성
categories: summary
short_description: 자바 예제 문제 풀기
#image_preview: https://miro.medium.com/max/910/1*BCZkmZR1_YzDZy22Vn4uUw.png
#external_url: https://habrahabr.ru/post/278937/
---
pro46
~~~
package lecture20190728;
public class Pro46 {
public static void main(String[] args) {
String a = "julio";
String b = "abraham";
String c = "dodo";
System.out.println(a.charAt(0));
System.out.println(b.charAt(0));
System.out.println(c.charAt(0));
// TODO Auto-generated method stub
}
}
~~~

ex47
~~~
package lecture20190728;
public class Ex47 {
public static void main(String[] args) {
System.out.println(text_1);
System.out.println(text_2);
System.out.println(text_3);
// TODO Auto-generated method stub
}
}
~~~

ex48
~~~
package lecture20190728;
public class Ex48 {
public static void main(String[] args) {
String text = "hello "
+ "my name is "
+ "Q";
System.out.println(text);
// TODO Auto-generated method stub
}
}
~~~

pro49
~~~
package lecture20190728;
public class Pro49 {
public static void main(String[] args) {
System.out.println("지나간 것은\n지나간 대로\n그런 의미가 있죠");
// TODO Auto-generated method stub
}
}
~~~

pro50
~~~
package lecture20190728;
public class Pro50 {
public static void main(String[] args) {
String a = "a\nb\tc\td\n\n";
String b = "efg\n\"h\"";
System.out.println(a);
System.out.println(b);
// TODO Auto-generated method stub
}
}
~~~

pro51
~~~
package lecture20190728;
public class Pro51 {
public static void main(String[] args) {
String a = "ronaldo";
String b = "portugal";
int c = 33;
int d = 185;
System.out.printf("my name is %s and i'm from %s\n",a,b);
System.out.printf("i'm %d years old and %d cm tall",c,d);
// TODO Auto-generated method stub
}
}
~~~

pro52
~~~
package lecture20190728;
public class Pro52 {
public static void main(String[] args) {
String a = "billy";
String b = "juno";
String c = "tall";
String d = "smart";
System.out.printf("%s is %s\n",a,c);
System.out.printf("%s is %s",b,d);
// TODO Auto-generated method stub
}
}
~~~

pro53
~~~
package lecture20190728;
public class Pro53 {
public static void main(String[] args) {
String a = "가나\n다라\n마바사\t아";
String b = "자차카";
String c = "타\n파하";
System.out.print(a);
System.out.println(b);
System.out.print(c);
// TODO Auto-generated method stub
}
}
~~~

pro54
~~~
package lecture20190728;
public class Pro54 {
public static void main(String[] args) {
System.out.println("국가 : 대한민국\n수도 : 서울\n언어 : 한국어\n인구 : 51,779,148명");;
// TODO Auto-generated method stub
}
}
~~~

test01
~~~
package lecture20190728;
public class Test01 {
public static void main(String[] args) {
System.out.println("안녕하세요 제 이름은 ooo입니다.");
// TODO Auto-generated method stub
}
}
~~~

test02
~~~
package lecture20190728;
public class Test02 {
public static void main(String[] args) {
int math = 96;
int sci = 91;
int eng = 100;
System.out.println("수학 :" + math);
System.out.println("과학 :" + sci);
System.out.println("영어 :" + eng);
// TODO Auto-generated method stub
}
}
~~~

test03
~~~
package lecture20190728;
public class Test03 {
public static void main(String[] args) {
int radius = 5;
double pi = 3.14;
double result = radius * 2 * pi;
System.out.println(result);
// TODO Auto-generated method stub
}
}
~~~

test04
~~~
package lecture20190728;
public class Test04 {
public static void main(String[] args) {
//이 부분을 주석처리해서 프로그램이 정상적으로 실행되도록 해보세요
System.out.println("helloworld");
// TODO Auto-generated method stub
}
}
~~~

test05
~~~
package lecture20190728;
public class Test05 {
public static void main(String[] args) {
String name = "홍길동";
int num = 2018122104;
double tall = 1.78;
boolean isMale = true;
System.out.println("이름 " + name);
System.out.println("학번 " + num);
System.out.println("신장 " + tall);
System.out.println("남자인가요? " + isMale);
// TODO Auto-generated method stub
}
}
~~~

test06
~~~
package lecture20190728;
public class Test06 {
public static void main(String[] args) {
int i;
for(i=0;i<100;i++)
{
System.out.print("*");
}
int a = 0;
for(i=1;i<=100;i++)
{
a = a+i;
}
System.out.println(a);
// TODO Auto-generated method stub
}
}
~~~

test07
~~~
package lecture20190728;
import java.util.Scanner;
public class Test07 {
public static void main(String[] args) {
Scanner scan = new Scanner(System.in);
int a = 0;
a = scan.nextInt();
if(a>0 || a<100)
{
System.out.println("입력된 값 : " + a);
}
else
{
System.out.println("입력오류");
}
// TODO Auto-generated method stub
}
}
~~~

test08
~~~
package lecture20190728;
import java.util.Scanner;
public class Test08 {
public static void main(String[] args) {
Scanner scan = new Scanner(System.in);
String a;
String b;
int c = 0;
double d = 0;
a = scan.nextLine();
b = scan.nextLine();
c = scan.nextInt();
d = scan.nextDouble();
System.out.println("이름 : " + a);
if(b == "m")
{
System.out.println("성별 : 남자");
}
else
{
System.out.println("성별 : 여자");
}
System.out.println("나이 : " + c);
System.out.println("신장 : " + d);
// TODO Auto-generated method stub
}
}
~~~