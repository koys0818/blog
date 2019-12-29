---
layout: post
title: 객체 지향 프로그래밍
date: 2019-12-29 09:28:23
categories: Summary
short_description: 객체 지향 프로그래밍에 대해 정리한 글
#image_preview: https://avatars2.githubusercontent.com/u/4660275?v=3&s=460
---
클래스

클래스는 간단하게 유사한 특징을 가진 객체들을 모아둔 집합이다.
예를들면 고양이나 개나 사슴과 같은 여러 동물들은 동물이라는 특성으로
모을 수가 있다.
그리고 간단하게 그것을 작성해보면
public class Animal {


   public static void main(String[] args) {
      Animal cat = new Animal();
      Animal dog = new Animal();
  }
}
로 작성할 수 있다.
여기서 new는 객체를 생성할 때 사용하는 연사자이다.
이렇게 쓰면 Animal 클래스의 인스턴스(객체)인 cat과 dog가 생성된다.


객체 변수


여기서 Animal이라는 클래스를 더 발전시켜 보면 클래스에 여러 변수를
추가할 수 있다.
예들들어 나이나 몸무게등의 int 변수나 이름과 같은 String 변수등을 추가할 수 있고 이렇게 클래스에 선언된 변수를 객체 변수라고 한다.
예를들어 
public class Animal {
      String name;
 }
와 같이 만들 수 있는데 이 객체 변수를 출력하려면 도트연산자(.)를
사용하여야 한다.
객체.객체변수
위에서 예로 든 Animal 클래스에서는 cat이라는 객체를 생성했으니
객체 변수 name를 출력 하려면
cat.name
과 같이 사용해야하고 이걸 사용하면
public class Animal {
   String name;


   public static void main(String[] args) {
     Animal cat = new Animal();
     System.out.println(cat.name);
   }
}


라고 작성할 수 있는데 이대로 실행해보면 null이라고 결과가 출력된다
null이라는 것은 값이 할당되어 있지 않다는건데 객체 변수로
name를 선언했지만 아무런 값도 대입하지 않았기 때문에 null이 출력된다.


메소드


자바는 클래스 밖에 있는 것은 존재할 수 없기 때문에 자바의 함수는 다른 언어들과 다르게 자바의 클래스 안에 존재한다.
여기서 자바의 클래스 내에 있는 함수를 메소드라고 한다.
메소드를 사용하는 이유는 가끔 프로그래밍을 할 때 똑같은 내용을 반복해서 사용하고 있다면 그 때가 메소드가 필요한 때이다
여러 번 반복해서 같은 내용을 작성하기 보다는 이것을 하나로 뭉쳐서
어떤 값을 대입하면 어떤 리턴값을 돌려준다는 식의 메소드를 작성하는 것이
나을 것이다.
간단하게 예를 들어보면
public int sum(int a, int b) {
    return a+b;
}
를 들 수  있는데 위 메소드의 의미는
"sum이라는 메소드는 2개의 int 자료형 입력값을 받고 2개를 더한 int형의 리턴값이 나온다."
이다.
자바의 메소드의 구조는
public 리턴값의 자료형 메소드 명 (입력자료형1 입력변수1, 입력자료형2 입력변수 2, …) {
…
return 리턴값;  // 리턴자료형이 void인 경우에는 return은 필요없다.
}
인데 여기서 리턴자료형은 메소드가 끝난 후에 돌려줄 결과값의 자료형을 
의미한다.
메소드는 입출력의 유무에 따라 4가지로 분류할 수 있다.
1. 입력과 출력이 모두 있는 메소드
2. 입력과 출력이 모두 없는 메소드
3. 입력은 없고 출력은 있는 메소드
4. 입력은 있고 출력은 없는 메소드



1번부터 알아보면 입력값과 출력값이 모두 있는 평범한 메소드이고
예는 위에 든 예시와 같다.


2번인 입력값도 출력값도 없는 메소드는 간단하게 예를 들면
public void say() (
   System.out.println("Hello")
}


상속


상속은 말 그대로 자식이 부모로부터 무언가를 물려받는 것이다.
자바의 상속도 똑같이 부모 클래스로부터 자식 클래스가 무엇가를 상속받는 것이다.
클래스 상속을 위해서는 extends라는 키워드를 사용하게 되는데
자식 클래스 extends 부모 클래스
의 형태이다.
예를 들어 Animal 클래스를 상속하는 Dog 클래스를 만들려면
Animal.java
public class Animal {
    String name;

    public void setName(String name) {
        this.name = name;
    }
}


를 만든 후
Dog.java
public class Dog extends Animal {

}


extends를 사용하면 Dog 클래스는 Animal 클래스를 상속하게 된다