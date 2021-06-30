# Android

<details>
<summary><strong>목록</strong></summary>
<div markdown = "1">

- [안드로이드의 4대 구성요소가 무엇인가요?](#안드로이드의-4대-구성요소가-무엇인가요)
    * [안드로이드의 4대 구성요소의 역활을 설명해 주세요.](#안드로이드의-4대-구성요소의-역활을-설명해-주세요)
        + [Content Provider와 Content Resolver의 차이점은 무엇입니까?](#content-provider와-content-resolver의-차이점은-무엇입니까)
- [Activity의 생명주기에 대해 설명해 주세요.](#activity의-생명주기에-대해-설명해-주세요)
    * [Fragment의 생명주기에 대해 설명해 주세요.](#fragment의-생명주기에-대해-설명해-주세요)
- [스레드, 핸들러, 루퍼 예제](#스레드-핸들러-루퍼-예제)
    * [ANR에 대해 설명해 주세요.](#anr에-대해-설명해-주세요)
- [Context에 대해 설명해 주세요.](#context에-대해-설명해-주세요)
- [콜백(Callback)과 리스너(Listener)에 대해서 설명해 주세요.](#콜백callback과-리스너listener에-대해서-설명해-주세요)

</div>
</details>

## 안드로이드의 4대 구성요소가 무엇인가요?

액티비티, 서비스, 브로드캐스트 리시버, 콘텐트 프로바이더가 핵심 구성요소이다.
이외의 구성요소로는 인텐트, 인텐트 필터, 노티피케이션, 프래그먼트 등이 있다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

### 안드로이드의 4대 구성요소의 역활을 설명해 주세요.

공통적으로 하나의 독립적인 형태로 존재하며, 고유의 기능을 수행하며, 인텐트를 통해 서로 상호작용 한다는 점이 있습니다.

- **액티비티(Activity)**

    액티비티는 사용자가 애플리케이션과 상호작용하는 단일 화면을 의미하며, 모든 안드로이드 애플리케이션은 액티비티로 구성되어 있습니다. 2개 이상의 액티비티를 동시에 전시할 수 없으며, 1개 이상의 View 또는 ViewGroup을 포함하여야 합니다.

- **서비스(Service)**

    서비스는 직접적으로 사용자와 상호작용하지 않고, 백그라운드에서 어떠한 작업을 처리하기 위해 사용됩니다. 따라서 별도의 UI를 가지지 않습니다. 액티비티와 동일하게 메인 스레드에서 실행되며, 애플리케이션이 종료되어도 이미 시작된 서비스는 백그라운드에서 계속 동작합니다.

- **브로드캐스트 리시버(Broadcast Receiver)**

    브로드캐스트 리시버는 안드로이드 OS로부터 발생하는 각종 이벤트와 정보를 받아와 핸들링하는 요소입니다. 안드로이드 OS에서 특정 이벤트(ex. 배터리 부족 알림이나 문자 수신 등)를 방송(Broadcast)하면 이를 수신하여 특정 이벤트를 처리할 수 있습니다.

- **콘텐트 프로바이더(Content Provider)**

    콘텐트 프로바이더는 데이터를 관리하고 다른 애플리케이션의 데이터를 제공하는 데 사용되는 요소입니다. 특정한 애플리케이션이 사용하고 있는 데이터베이스를 공유하기 위한 표준화된 인터페이스를 제공합니다. 작은 데이터들은 인텐트로 공유 가능하지만 용량이 큰 데이터의 경우 콘텐트 프로바이더를 통해 제공할 수 있습니다.

##### 참고자료

- https://velog.io/@jojo_devstory/안드로이드-Android-4대-컴포넌트

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

#### Content Provider와 Content Resolver의 차이점은 무엇입니까?

 앱이 Content Provider를 통해서 데이터에 접근할 때 Content Resolver를 통해서 접근해야 합니다. 즉, Content Provider가 제공하는 데이터는 Content Resolver를 통해서 접근하도록 설계되어 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

## Activity의 생명주기에 대해 설명해 주세요.

![Activity 생명주기](./img/Activity%20생명주기.png)

기본적으로 액티비티를 시작하면 onCreate -> onStrar -> onResume 메소드가 순차적으로 실행되면서 액티비티가 실행된다. 이후 onPause -> onStop -> onDestroy 메소드가 순차적으로 실행되면서 액티비티가 완전 종료된다.

- onCreate : 액티비티가 생성될 때 호출되며 사용자 인터페이스 초기화에 사용됨.
- onRestart : 액티비티가 멈췄다가 다시 시작되기 바로 전에 호출됨.
- onStart : 액티비티가 사용자에게 보여지기 바로 직전에 호출됨.
- onResume : 액티비티가 사용자와 상호작용하기 바로 전에 호출됨.
- onPause : 다른 액티비티가 보여질 때 호출됨. 데이터 저장, 스레드 중지 등의 처리를 하기에 적당한 메소드.
- onStop : 액티비티가 더이상 사용자에게 보여지지 않을 때 호출됨. 메모리가 부족할 경우에는 onStop 메소드가 호출되지 않을 수도 있음.
- onDestroy : 액티비티가 소멸될 때 호출됨. finish() 메소드가 호출되거나 시스템이 메모리 확보를 위해 액티비티를 제거할 때 호출됨.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

### Fragment의 생명주기에 대해 설명해 주세요.

![Fragment 생명주기](./img/Fragment%20생명주기.png)

보류

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

## 스레드, 핸들러, 루퍼 예제

##### 참고자료

- https://itmining.tistory.com/4?category=640759
- https://bitsoul.tistory.com/108
- https://velog.io/안드로이드-스레드Thread와-핸들러Handler

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

### ANR에 대해 설명해 주세요.

Application Not Responding의 약자로 input 이벤트에 5초 간 반응하지 않거나, Broadcast Reciever가 10초 내로 실행을 하지 않을 때 즉, 메인 스레드가 일정 시간 특정 Task에 묶여있을 때 발생하는 오류입니다. 이를 해결하기 위해서는 시간을 소모하는 Task는 별도의 워커 스레드에서 처리하거나, 사용자에게 해당 Task의 진행 상태를 전시하여 기다리도록 합니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

## Context에 대해 설명해 주세요.

현재 사용되고 있는 Application(또는 Activity)에 대한 포괄적인 정보를 지니고 있는 객체입니다. Application Context와 Activity Context의 차이점으로는 Application Context의 경우 Application의 생명 주기에 종속되어 있어 현재 Context와 상관없는 다른 Context가 필요하거나 Activity 활동 범위를 벗어난 Context를 필요로 할 때 사용됩니다. Activity Context는 Activity의 생명 주기에 종속되기 때문에 Activity의 생명 주기와 맞물리는 작업(ex. Activity A에서 Activity B로 넘어갈 때 등)에서 필요합니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

## 콜백(Callback)과 리스너(Listener)에 대해서 설명해 주세요.

둘은 비슷한 개념이지만, 콜백은 이벤트 발생 시 특정 메소드를 호출해 알려주고 리스너는 이벤트 발생 시 연결된 리스너들에게 이벤트롤 전달하는 차이가 있습니다. 즉, 리스너를 등록할 수 있는 갯수가 유일한 지, 그렇지 않은 지의 차이입니다. 

##### 참고자료

- https://www.charlezz.com/?p=768
- https://onlyfor-me-blog.tistory.com/47

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#android)**

## ETC

<details>
 <summary><strong>한정적인 시간 가운데 선택적으로 공부하지 않은 내용입니다.</strong></summary>
 <div markdown = "1">

>시간적 여유가 있을 때 보충예정

- [Fragment의 생명주기에 대해 설명해 주세요.](#fragment의-생명주기에-대해-설명해-주세요)

</div>
</details>

---
# Reference

* [taeiim 님의 Android Study](https://github.com/taeiim/Android-Study/blob/master/study/week16/안드로이드%20개발자로%20취업하기%20-%20면접/신입%20안드로이드%20개발자로%20취업하기%20-%20면접.md)

* [단계별 예제로 배우는 안드로이드 지식](https://kairo96.gitbooks.io/android/content/)