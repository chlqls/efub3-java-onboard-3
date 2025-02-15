# 자바 핵심 개념 정리 3
<details>
<summary>POJO란 무엇일까요?</summary>
<div markdown="1">

- Spring의 특징 중 하나인 POJO는 Plain Old Java Object의 줄임말로 "오래된"  방식의 “순수한“ 자바 객체를 말한다.
- 순수한 자바 객체란 특정 기술에 종속되지 않고 Java 및 java의 스펙에 정의된 기술만 사용하는 것을 말한다. 
- Spring 이전에는 다른 기술과 환경에 지나치게 의존하기 때문에 객체 지향의 장점을 잃어버렸으나, Spring은 유연하게 변화와 확장에 대처 가능하고, 자바의 객체 지향 정신에 부합한다.

</div>
</details>
<br>

<details>
<summary>제너릭이 무엇인가요? 컬렉션 클래스에서 제너릭을 사용하는 이유를 설명해 주세요.</summary>
<div markdown="1">

- 제네릭(Generic)은 클래스 내부에서 지정하는 것이 아닌 외부에서 사용자에 의해 지정되는 것을 의미한다.
- 다음과 같은 제네릭의 특성으로 인해 컬렉션 클래스에서 제너릭을 사용한다.
1. 제네릭을 사용하면 잘못된 타입이 들어올 수 있는 것을 컴파일 단계에서 방지할 수 있다.
2. 클래스 외부에서 타입을 지정해주기 때문에 따로 타입을 체크하고 변환해줄 필요가 없다. 즉, 관리하기가 편하다.
3. 비슷한 기능을 지원하는 경우 코드의 재사용성이 높아진다.

</div>
</details>
<br>

<details>
<summary>자바의 클래스 멤버 변수 초기화 순서에 대해 알려주세요.</summary>
<div markdown="1">

- 클래스별로 유일한 클래스 변수(static 변수)는 클래스가 처음 메모리에 로딩될 때 단 한번 차례대로 초기화된다.
- 순서는 기본값 -> 명시적 초기화 -> 클래스 초기화 블럭이다.

</div>
</details>
<br>

<details>
<summary>직렬화란 무엇인가요?</summary>
<div markdown="1">

- 직렬화(Serialize)는 자바 시스템 내부에서 사용되는 Object 또는 Data를 외부의 자바 시스템에서도 사용할 수 있도록 byte 형태로 데이터를 변환하는 기술이다. 
- 즉, JVM(Java Virtual Machine)의 메모리에 상주(힙 또는 스택)되어 있는 객체 데이터를 바이트 형태로 변환하는 기술을 말한다.

</div>
</details>
<br>

<details>
<summary>[예습] SOLID에 대해 알아봅시다.</summary>
<div markdown="1">

1. SRP(Single Responsibility Principle): 단일 책임 원칙
    - 클래스(객체)는 단 하나의 기능만 담당해야한다는 원칙
    - 수정할 이유가 단 한 가지여야 함
    - 프로그램의 유지보수성을 높이기 위해 필요
2. OCP(Open Closed Priciple): 개방 폐쇄 원칙
    - 확장에 열려있어야하며, 수정에는 닫혀있어야함
    - 즉, 기능을 추가할 때 클래스 확장을 통해 손쉽게 구현하고, 확장에 따른 클래스 수정은 최소화 해야함
    - 추상화 사용을 통한 관계 구축 권장
3. LSP(Listov Substitution Priciple): 리스코프 치환 원칙
    - 하위(자손) 타입은 언제나 상위(부모) 타입으로 교체할 수 있어야 함
    - 다형성의 원리를 이용하기 위한 원칙
    - 업캐스팅된 상태에서 부모의 메서드를 사용해도 동작이 되도록 해야 함
4. ISP(Interface Segregation Principle): 인터페이스 분리 원칙
    - 인터페이스를 각각 사용에 맞게끔 잘게 분리해야 함
    - 인터페이스의 단일 책임 강조
    - 클라이언트의 목적과 용도에 적합한 인터페이스만을 제공하는 것이 목표
5. DIP(Dependency Inversion Principle): 의존 역전 원칙
    - 사용하고자 하는 클래스를 직접 참조하는 것이 아니라 대상의 상위 요소(추상 클래스 또는 인터페이스)를 참조
    - 클래스에 의존하지 말고, 인터페이스에 의존

</div>
</details>
<br>

<details>
<summary>[예습] DI는 무엇일까요?</summary>
<div markdown="1">

- 스프링의 또다른 특징인 의존성 주입(DI)은 객체를 직접 생성하는 것이 아니라 외부에서 생성한 후 주입시켜주는 방식을 말한다.
- 모듈 간의 결합도가 낮아지고 유연성이 높아진다.
</div>
</details>
<br>