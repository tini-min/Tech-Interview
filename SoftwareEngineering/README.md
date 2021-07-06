# Software Engineering

<details>
 <summary><strong>목차</strong></summary>
 <div markdown = "1">

- [TDD란 무엇인가요?](#tdd란-무엇인가요)
- [애자일(Agile)이 무엇인가요?](#애자일agile이-무엇인가요)
    * [데브옵스가 무엇인가요?](#데브옵스가-무엇인가요)
    * [스크럼이 무엇인가요?](#스크럼이-무엇인가요)
- [객체지향 프로그래밍이 무엇인가요?](#객체지향-프로그래밍이-무엇인가요)
    * [OOP의 특징은 무엇이 있나요?](#OOP의-특징은-무엇이-있나요)
        + [응집도와 결합도가 무엇인가요?](#응집도와-결합도가-무엇인가요)
        + [오버라이딩과 오버로딩을 설명해 주세요.](#오버라이딩과-오버로딩을-설명해-주세요)
    * [객체 지향 설계 원칙에 대해 설명해 주세요.](#객체-지향-설계-원칙에-대해-설명해-주세요)
- [함수형 프로그램밍이 무엇입니까?](#함수형-프로그램밍이-무엇입니까)
    * [객체 지향 프로그래밍과 함수형 프로그래밍의 차이는 무엇인가요?](#객체-지향-프로그래밍과-함수형-프로그래밍의-차이는-무엇인가요)
- [프레임워크가 무엇인가요?](#프레임워크가-무엇인가요)
- [디자인패턴](#디자인패턴)

</div>
</details>

## TDD란 무엇인가요?

테스트 주도 개발(Test Driven Development)이란 것은 테스트 케이스를 먼저 작성한 후 실제 코드를 개발하는 방법입니다. 반복적인 테스트와 수정을 통해 고품질의 소프트웨어를 개발하는 게 목적입니다. 장점으로는 작업과 동시에 테스트를 진행하면서 실시간으로 오류 파악이 가능하단 점이 있으며, 짧은 개발 주기를 통해 고객의 요구사항 빠르게 수용 가능합니다. 즉, 피드백이 가능하고 진행 상황 파악이 쉽습니다. 다만, 기존 개발 프로세스에 테스트케이스 설계가 추가되므로 생산 비용 증가하고, 테스트의 방향성이나 프로젝트 성격에 따른 테스트 프레임워크 선택 등 추가로 고려할 부분의 증가한다는 단점이 있습니다. 따라서, 유지보수의 비용이 초기 개발의 비용보다 비싸거나 안정성이 중요한 프로젝트의 경우 주로 사용됩니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## 애자일(Agile)이 무엇인가요?

초기 소프트웨어 개발을 하던 시대 비해 최근에 들어서 트랜드가 급격하게 변화하고 있습니다. 전통적으로 계획을 설립하고 개발하기엔 개발의 불확실성이 늘어났습니다. 그래서 일단 해보고 고쳐나가자는 방식으로 진행을 하다가 이러한 개발 방법론을 공유하고 공통점을 추린 것이 애자일입니다. 애자일의 핵심은 협력과 피드백입니다. 지속적으로 요구사항을 수정할 수 있을 뿐더러, 변경사항에 대해 유연하고 기민하게 대응할 수 있습니다.

##### 참고자료

- https://gmlwjd9405.github.io/2018/05/26/what-is-agile.html

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

### 스크럼이 무엇인가요?

애자일을 통한 개발 방법론 중 가장 많이 사용되는 방식입니다. 먼저 개발할 제품에 대한 요구사항 목록을 작성합니다. 이후 스프린트의 Backlog를 작성하여 상황을 설계합니다. 일정 주기를 정해 놓고 해당 목적을 위해 전력질주하여 개발을 진행합니다. 그러면서 매일 스크럼 회의를 가지는 데, 15분 정도 짧게 진행 상황을 점검하는 목적입니다. 이런 스프린트 주기가 모두 끝나면, 제품 기능 목록에서 작성한 제품이 완성됩니다.<br>
장점으로는 스프린트마다 생산되는 실행 가능한 제품을 통해 사용자와 의견을 나눌 수 있고, 회의를 통해 팀원들 간 신속한 협조와 조율이 가능하다는 점입니다. 프로젝트 진행 현상을 통해 신속하게 목표와 결과 추정이 가능하며, 변화 시도가 용이한 점도 있습니다. 다만, 단점으로는 스프린트마다 테스트 제품을 만들어야 하기 때문에 추가 작업시간이 필요하고, 15분이라는 회의 시간을 지키기 힘든 점도 있습니다. 또한, 스크럼은 프로젝트 관리에 중심을 두기에 품질 평가에는 미약한 점이 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

### 데브옵스가 무엇인가요?

소프트웨어 개발자와 정보기술 전문가 간의 소통, 협업 및 통합을 강조하는 개발 환경이나 문화를 의미합니다. 소프트웨어 제품과 서비스를 빠른 시간에 개발 및 배포하는 것이 목표입니다. 해당 개념은 애자일 기법이나 지속적 통합의 개념과도 관련이 있습니다.

##### 참고자료

- https://gyoogle.dev/blog/computer-science/software-engineering/DevOps.html

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## 객체지향 프로그래밍이 무엇인가요?

객체지향 프로그래밍(Object Oriented Programming)은 현실 세계의 사물들을 객체라고 보고 그 객체로부터 개발하고자 하는 애플리케이션에 필요한 특징들을 뽑아와 프로그래밍하는 것입니다. OOP로 코드를 작성하면 이미 작성한 코드에 대한 재사용성이 높습니다. 그리고 라이브러리를 각종 예외상황에 맞게 잘 만들어두면 개발자가 사소한 실수를 하더라도 그 에러를 컴파일 단계에서 잡아낼 수 있으므로 버그 발생이 줄어듭니다. 또한, 내부적으로 어떻게 동작하는지 몰라도 개발자는 라이브러리가 제공하는 기능들을 사용할 수 있기 때문에 생산성이 높아지게 됩니다. 객체 단위로 코드가 나눠져 작성되기 때문에 디버깅이 쉽고 유지보수에 용이하다는 점도 있습니다. 다만, 개발속도나 실행속도가 느리고 코딩 난이도가 상승된다는 점이 단점이 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

### OOP의 특징은 무엇이 있나요?

크게 `추상화`, `캡슐화`, `상속`, `다형성` 등이 있습니다. `추상화`란 세부적인 사물들의 공통적인 특징을 파악한 후 하나의 집합으로 나타내는 것입니다. 새로운 사물을 구현할 때도 별도로 수정할 필요없이 추가로 만들 부분만 새로 생성하면 됩니다. `캡슐화`란 한 곳에서 변화가 일어나도 다른 곳에 미치는 영향을 최소화 시키는 것입니다. 객체들 간의 의존도가 높아지면 굳이 객체 지향으로 설계하는 의미가 없어지기 때문입니다. `상속`이라고 하는 것은 자식 클래스를 외부로부터 은닉하는 캡슐화의 일종입니다. `다형성`은 서로 다른 클래스의 객체가 같은 메시지를 받았을 때 각자의 방식으로 동작하는 능력입니다. 정확히는 부모 클래스의 메소드를 자식 클래스가 오버라이딩해서 자신의 역활에 맞게 활용하는 것이 다형성이다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

#### 응집도와 결합도가 무엇인가요?

정보 은닉 및 모듈화에 충실하기 위해 OOP는 높은 응집도와 낮은 결합도를 지향해야 합니다. 여기서 `응집도`란 한 모듈 내부의 처리 요소들 간의 기능적 연관도를 내타내는 거이며, `결합도`란 서로 다른 모듈 간에 상호 의존도 혹은 연관도를 의미합니다. 이런 독립성이 높은 모듈의 경우 해당 모듈을 수정하더라도 다른 모듈에 끼치는 영향이 적으며, 오류가 발생하더라도 쉽게 문제를 발견하고 해결할 수 있기에 유지 보수가 편리합니다.

##### 참고자료

- https://madplay.github.io/post/coupling-and-cohesion-in-software-engineering

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

#### 오버라이딩과 오버로딩을 설명해 주세요.

다형성을 지원하는 방식으로 오버라이딩과 오버로딩이 있습니다. 오버라이딩은 상위 클래스가 가지고 있는 메서드를 하위 클래스에서 재정의하여 사용하는 것을 의미하고, 오버로딩은 같은 이름의 메서드를 매개변수의 타입이나 갯수가 다르게 각각 정의하는 기술입니다.

##### 참고자료

- https://private.tistory.com/25

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

### 객체 지향 설계 원칙에 대해 설명해 주세요.

**SRP, OCP, LSP, ISP, DIP**가 있습니다.<br>

1. **SRP(Single Responsibility)** - 단일 책임 원칙<br>
클래스는 단 한 개의 책임을 가져야 하며, 클래스를 변경하는 이유는 단 한 개여야 합니다.<br>
이를 지키지 않으면, 한 책임의 변경에 의해 다른 책임과 관련된 코드에 영향이 갈 수 있습니다.

1. **OCP(Open-Closed)** - 개방-폐쇄 원칙<br>
확장에는 열려 있어야 하고, 변경에는 닫혀 있어야 합니다. 즉, 기능을 변경하거나 확장할 수 있지만, 그 기능을 사용하는 코드는 수정하지 않아야 합니다.<br>
이를 지키지 않으면, instanceof와 같은 연산자를 사용하거나 다운 캐스팅이 일어난다.

1. **LSP(Liskov Substitution)** - 리스코프 치환 원칙<br>
상위 타입의 객체를 하위 타입의 객체로 치환해도, 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 합니다.<br>
상속 관계가 아닌 클래스들을 상속 관계로 설정하면, 이 원칙이 위배됩니다.

1. **ISP(Interface Segregation)** - 인터페이스 분리 원칙<br>
인터페이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 합니다. 각 클라이언트가 필요로 하는 인터페이스들을 분리함으로써, 각 클라이언트가 사용하지 않는 인터페이스에 변경이 발생하더라도 영향을 받지 않도록 만들어야 합니다.

1. **DIP(Dependency Inversion)** - 의존 역전 원칙<br>
고수준 모듈은 저수준 모듈의 구현에 의존해서는 안됩니다.<br>
저수준 모듈이 고수준 모듈에서 정의한 추상 타입에 의존해야 합니다. 즉, 저수준 모듈이 변경돼도 고수준 모듈은 변경할 필요가 없는 것입니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## 함수형 프로그램밍이 무엇입니까?

>  함수형 프로그래밍의 가장 큰 특징 두 가지는 immutable data와 first class citizen으로서의 function이다.

먼저, 순수 함수에 대해 설명하면 순수 함수(Pure Function)란 동일한 입력값을 넣었을 때 항상 동일한 리턴값을 반환하며 외부에 영향을 받지 않는 함수입니다. 함수형 프로그래밍은 이런 순수 함수를 이용한 프로그래밍입니다. 순수 함수의 특성 상 함수형 프로그래밍의 경우 사이드 이펙트를 미연에 방지하고, 코드가 OOP에 비해 간결하다는 장점이 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

### 객체 지향 프로그래밍과 함수형 프로그래밍의 차이는 무엇인가요?

가장 근본적인 차이는 문제해결의 관점에 있습니다. 객체 지향의 경우 데이터를 어떻게 처리할 지에 대해 명령을 통해 해결했습니다. 이에 반해 함수형은 무엇을 풀어나가야 할 지에 대해 결정하는 것입니다.

> 객체 지향은 동작하는 부분을 캡슐화해서 이해할 수 있게 하고, 함수형은 동작하는 부분을 최소화해서 코드 이해를 돕는다.
> <br>- 마이클 페더스

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## 프레임워크가 무엇인가요?

> 프레임워크란, 소프트웨어의 구체적인 부분에 해당하는 설계와 구현을 재사용이 가능하게끔 일련의 협업화된 형태로 클래스들을 제공하는 것<br>
> \- **Ralph Johnson**

라이브러리와 흡사하게 기존의 설계와 구현을 재사용하는 것이지만 라이브러리는 사용자가 해당 흐름을 가지고 프로그래밍을 주도할 수 있지만 프레임워크는 이미 정해진 틀 안에서 일부만 사용자가 설계할 수 있습니다. 프레임워크의 사용은 효율적이며, 이미 검증된 코드이기에 버그 가능성을 미리 처리하는 등의 유지 보수가 간편합니다. 다만, 프레임워크의 코드를 습득하고 이해하는 데 시간이 소요되고, 프레임워크 제작자가 설계한 구조를 어느 정도 유지한 채 코드를 설계하기에 자유롭고 유연한 개발에는 한계가 있습니다.

##### 참고자료

- https://moolgogiheart.tistory.com/87

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## 디자인패턴

<details>
 <summary><strong>목차</strong></summary>
 <div markdown = "1">

- [싱글턴 패턴](#싱글톤-패턴)
- [MVC 패턴](#mvc-패턴)

</div>
</details>

### 싱글턴 패턴

#### 필요성

`Singleton Pattern(싱글턴 패턴)`이란 애플리케이션에서 인스턴스를 하나만 만들어 사용하기 위한 패턴입니다. 커넥션 풀, 스레드 풀, 디바이스 설정 객체 등의 경우, 인스턴스를 여러 개 만들게 되면 자원을 낭비하게 되거나 버그를 발생시킬 수 있으므로 오직 하나만 생성하고 그 인스턴스를 사용하도록 하는 것이 이 패턴의 목적입니다.

#### 구현

```java
public class Singleton {
    private static Singleton singletonObject;

    private Singleton() {}

    public static Singleton getInstance() {
        if (singletonObject == null) {
            singletonObject = new Singleton();
        }
        return singletonObject;
    }
}
```
> 동기화 문제가 해결되지 않음.

```java
public class Singleton {
    private static Singleton singletonObject;

    private Singleton() {}

    public static synchronized Singleton getInstance() {
        if (singletonObject == null) {
            singletonObject = new Singleton();
        }
        return singletonObject;
    }
}
```
> `synchronized`를 이용하여 간단하게 동기화 문제를 해결할 수 있지만 성능상 단점이 존재.

```java
public class Singleton {
    private static Singleton singletonObject;

    private Singleton() {}

    public static Singleton getInstance() {
        if (singletonObject == null) {
            synchronized (Singleton.class) {
                if (singletonObject == null) {
                    singletonObject = new Singleton();
                }
            }
        }
        return singletonObject;
    }
}
```
> `DCL(Double Checking Locking)`을 써서 `getInstance()`에서 동기화 되는 영역을 줄일 수 있음. 초기에 객체를 생성하지 않으면서도 동기화하는 부분이 작음. 그러나 해당 코드는 멀티코어 환경에서 동작할 때, 하나의 CPU 를 제외하고는 다른 CPU 가 lock 이 걸림.

```java
public class Singleton {
    private static volatile Singleton singletonObject = new Singleton();

    private Singleton() {}

    public static Singleton getInstance() {
        return singletonObject;
    }
}
```
> 클래스가 로딩되는 시점에 미리 객체를 생성해두고 그 객체를 반환. 인스턴스가 사용되지 않더라도 처음부터 끝까지 객체가 메모리에 있음.<br>
> cf) volatile : 컴파일러가 특정 변수에 대해 옵티마이져가 캐싱을 적용하지 못하도록 하는 키워드

```java
public class Singleton {
    private Singleton() {}

    private static class SingletonHolder {
        public static final Singleton INSTANCE = new Singleton();
    }

    public static Singleton getInstance() {
        return SingletonHolder.INSTANCE;
    }
}
```
> `getInstance()`가 호출되는 시점에 Singletone 객체가 생성됨. 최신 VM은 클래스를 초기화하기 위한 필드 접근은 동기화 되므로 2개의 인스턴스가 생성되지는 않음.

##### 참고자료
- https://asfirstalways.tistory.com/335

**[위로](#디자인패턴)**

### MVC 패턴

M(Model), V(View), C(Controller)로 나누어 서버를 구성하는 모델을 의미합니다.

![MVC 구동원리](./img/MVC%20구동원리.jpeg)

Client-Server 구조로 요청을 하면 그에 맞는 응답을 하는 구조를 기본으로 하고 있습니다.

1. 웹 브라우저가 웹 서버에 웹 애플리케이션 실행을 요청한다. (MVC 구조가 WAS라고 보면 된다.)
2. 웹 서버는 들어온 요청을 처리할 수 있는 Servelet을 찾아서 요청을 전달한다.
3. Servelet은 모델 자바 객체의 메서드를 호출한다.
4. 데이터를 가공하여 값 객체를 생성하거나, JDBC를 사용하여 데이터베이스와의 인터랙션을 통해 값 객체를 생성한다.
5. 업무 수행을 마친 결과값을 컨트롤러에게 반환한다.
6. 컨트롤러는 모델로부터 받은 결과값을 View에게 전달한다.
7. JSP는 전달받은 값을 참조하여 출력할 결과 화면을 만들고 컨트롤러에게 전달한다.
8. 뷰로부터 받은 화면을 웹 서버에게 전달한다.
9. 웹 브라우저는 웹 서버로부터 요청한 결과값을 응답받으면 그 값을 화면에 출력한다.

##### 참고자료

- https://asfirstalways.tistory.com/180

**[위로](#디자인패턴)**

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#software-engineering)**

## ETC

<details>
 <summary><strong>한정적인 시간 가운데 선택적으로 공부하지 않은 내용입니다.</strong></summary>
 <div markdown = "1">

>시간적 여유가 있을 때 보충예정

- [MVC패턴과 MTV패턴](https://tibetsandfox.tistory.com/16)
- [MVC, MVP, MVVM 비교](https://beomy.tistory.com/43)

</div>
</details>