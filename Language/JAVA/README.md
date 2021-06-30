# Java

<details>
 <summary><strong>목차</strong></summary>
 <div>

- [Java 언어의 특징을 설명해 주세요.](#java-언어의-특징을-설명해-주세요)
- [객체와 클래스의 차이점을 설명해 주세요.](#객체와-클래스의-차이점을-설명해-주세요)
- [추상화란 무엇입니까?](#추상화란-무엇입니까)
    * [추상클래스와 인터페이스에 대해 설명해 주세요.](#추상클래스와-인터페이스에-대해-설명해-주세요)
- [자바 메모리 관리에 대해 설명해 주세요.](#자바-메모리-관리에-대해-설명해-주세요)
    * [Garbage Collection에 대해 설명해 주세요.](#garbage-collection에-대해-설명해-주세요)
    * [static에 대해서 설명해 주세요.](#static에-대해서-설명해-주세요)

</div>
</details>

## Java 언어의 특징을 설명해 주세요.

Java는 C언어에 객체 지향적 기능을 추가하여 만든 C++과는 달리, 처음부터 [객체 지향 언어](https://github.com/tini-min/Tech-Interview/tree/master/SoftwareEngineering/#객체지향-프로그래밍이-무엇인가요)로 개발된 프로그래밍 언어입니다. Java는 자바 가상 머신(JVM, Java Virtual Machine)을 사용하여, 운영체제와는 독립적으로 동작할 수 있습니다. 따라서 다른 플랫폼에서도 같은 형태로 실행될 수 있습니다.

> 현재 Java는 전 세계에서 가장 많이 사용하는 프로그래밍 언어 중 하나입니다.

**장점**

1. 자바는 운영체제와는 독립적으로 실행할 수 있습니다.
2. 자바는 불필요한 기능을 과감히 제거하여 다른 언어에 비해 배우기가 쉽습니다.
3. 자바는 자동 메모리 관리 등을 지원하여 다른 언어에 비해 안정성이 높습니다
4. 자바는 연산자 오버로딩을 금지하고 제네릭을 도입함으로써 코드의 가독성을 높였습니다.
5. 자바에 관한 수많은 참고 자료를 찾을 수 있습니다.

**단점**

1. 자바는 실행을 위해 자바 가상 머신을 거쳐야 하므로, 다른 언어에 비해 실행 속도가 느립니다.
2. 자바는 예외 처리가 잘 되어 있지만, 개발자가 일일이 처리를 지정해 줘야 한다는 불편함이 있습니다.
3. 자바는 다른 언어에 비해 작성해야 하는 코드의 길이가 긴 편입니다.

##### 참고자료

- http://tcpschool.com/java/java_intro_basic

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

## 객체와 클래스의 차이점을 설명해 주세요.

클래스는 객체의 설계도이며, 객체는 클래스를 이용해 생성한 실체입니다. 즉, 객체는 클래스의 인스턴스입니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

## 추상화란 무엇입니까?

어떤 객체를 표현함에 있어 모든 것을 다 표현하는 것이 아니라 일정 부분 특징만을 표현하는 것을 추상화라고 합니다. 목적을 위해 필요한 부분만을 찾을 수 있기에 사용합니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

### 추상클래스와 인터페이스에 대해 설명해 주세요.

추상클래스는 추상 메서드를 포함하는 클래스입니다. 인터페이스 또한 비슷하지만 추상 메서드와 상수 만으로 구성된 경우입니다.<br>
둘 모두 선언만 있고 구현 내용이 없기에 new를 통해 객체를 생성할 수 없으며, 상속받은 자식만이 인스턴스를 생성할 수 있습니다. 상속 시 반드시 추상 메서드를 구현해야 합니다. (추상 클래스에 선언된 일반 메서드는 자식 클래스에서 사용하지 않아도 무방합니다)<br>
차이점은 아래와 같습니다.

|추상클래스|인터페이스|
|:---|:---|
|일반 메서드 포함 가능|모든 메서드가 추상 메서드|
|일반 변수(Optional) + 일반 메서드(Optional) + 추상 메서드 형태|상수 + 추상 메서드 형태|
|다중 상속 불가능|다중 상속 지원|

##### 참고자료

- https://private.tistory.com/20

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

## 자바 메모리 관리에 대해 설명해 주세요.

먼저, Stack과 Heap에 대해서 설명을 드리면, Heap은 주로 긴 생명주기를 가지는 데이터(ex. Object)를 저장하는 공간이며, Stack은 원시타입의 데이터의 실제 값이나 Object 타입의 데이터의 참조값이 할당됩니다. 다만, immutable한 객체의 경우 수정을 수행할 시 기존 객체가 변경되지 않고 새로운 객체를 생성하여 값을 할당합니다. 이러한 과정 속에서 Heap에 Unreachalbe한 객체가 쌓이게 되는데 이를 Garbage Collector가 Mark and Sweep하는 과정(즉, Unreachable한 객체를 제거하는 과정)을 통해 메모리 관리를 수행합니다.

##### 참고자료

- https://yaboong.github.io/java/2018/05/26/java-memory-management/

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

### Garbage Collection에 대해 설명해 주세요.

Java는 C와 같이 OS 레벨의 메모리에 직접 접근하여 실행되지 않고, JVM을 통해 간접적으로 메모리를 접근해 실행됩니다. 따라서, 운영체제로부터 독립적이란 점 이외에도 OS 레벨의 memory leak이 발생하지 않는데, 이런 누수현상을 방지하기 위한 또 다른 정책이 `Garbage Collection`입니다. 스택의 모든 변수를 스캔하면서 어떤 오브젝트를 참조하고 있는지 찾는 Mark라는 과정으로 통해 Reachable 객체를 marking합니다. 이후 marking되어 있지 않는 모든 객체를 제거하는 Sweep이라는 과정을 거쳐 Garbage(Unreachable한 객체)를 제거합니다. 다만, 이 과정 속에서 모든 스레드를 중단(Stop the World)하게 되는데, 불필요한 Garbage Collection은 프로그램에 악영향을 미칠 수 있습니다.<br>
Garbage Collection의 종류는 아래와 같습니다.

|GC 종류|Minor GC|Major GC|
|:---:|:---:|:---:|
|대상|Young Generation|Old Generation|
|실행 시점|Eden 영역이 꽉 찬 경우|Old 영역이 꽉 찬 경우|
|실행 속도|빠르다|느리다|

##### 참고자료

- https://yaboong.github.io/java/2018/06/09/java-garbage-collection/
- https://mangkyu.tistory.com/118

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

### static에 대해서 설명해 주세요.

Java에는 한 번 할당되어 프로그램이 종료될 때 해제되는 데이터를 모으는 Static 영역이 있습니다. 필드 부분에서 선언된 전역변수나 static 키워드를 사용한 데이터들은 해당 영역에 저장이 되며 큰 특징으로는 Garbage Collector가 이를 관리하지 않고, 해당 영역에 할당된 메모리는 모든 객체가 공유하는 메모리라는 점이 있습니다.

##### 참고자료

- https://mangkyu.tistory.com/47
- https://wikidocs.net/228

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#java)**

## ETC

<details>
 <summary><strong>한정적인 시간 가운데 선택적으로 공부하지 않은 내용입니다.</strong></summary>
 <div markdown = "1">

>시간적 여유가 있을 때 보충예정

- [Java 컬렉션 종류와 차이점1](https://gangnam-americano.tistory.com/41)
- [Java 컬렉션 종류와 차이점2](https://www.crocus.co.kr/1553)
- [Java 컬렉션 종류와 차이점3](http://tcpschool.com/java/java_collectionFramework_concept)

</div>
</details>