# Android

<details>
<summary><strong>목록</strong></summary>
<div markdown = "1">

- [안드로이드의 4대 구성요소가 무엇인가요?](#안드로이드의-4대-구성요소가-무엇인가요)
- [Activity의 생명주기가 무엇이가요?](#activity의-생명주기가-무엇이가요)
- [스레드, 핸들러, 루퍼 예제](#스레드-핸들러-루퍼-예제)
- [콜백(Callback)과 리스너(Listener)에 대해서 설명해 주세요.](#콜백callback과-리스너listener에-대해서-설명해-주세요)

</div>
</details>

## 안드로이드의 4대 구성요소가 무엇인가요?

액티비티, 서비스, 브로드캐스트 리시버, 콘텐트 프로바이더가 핵심 구성요소이다.
이외의 구성요소로는 인텐트, 인텐트 필터, 노티피케이션, 프래그먼트 등이 있다.

## Activity의 생명주기가 무엇이가요?

기본적으로 액티비티를 시작하면
onCreate -> onStrar -> onResume 메소드가 순차적으로 실행되면서 액티비티가 실행된다. 이후 onPause -> onStop -> onDestroy 메소드가 순차적으로 실행되면서 액티비티가 완전 종료된다.

- onCreate : 액티비티가 생성될 때 호출되며 사용자 인터페이스 초기화에 사용됨.
- onRestart : 액티비티가 멈췄다가 다시 시작되기 바로 전에 호출됨.
- onStart : 액티비티가 사용자에게 보여지기 바로 직전에 호출됨.
- onResume : 액티비티가 사용자와 상호작용하기 바로 전에 호출됨.
- onPause : 다른 액티비티가 보여질 때 호출됨. 데이터 저장, 스레드 중지 등의 처리를 하기에 적당한 메소드.
- onStop : 액티비티가 더이상 사용자에게 보여지지 않을 때 호출됨. 메모리가 부족할 경우에는 onStop 메소드가 호출되지 않을 수도 있음.
- onDestroy : 액티비티가 소멸될 때 호출됨. finish() 메소드가 호출되거나 시스템이 메모리 확보를 위해 액티비티를 제거할 때 호출됨.

## 스레드, 핸들러, 루퍼 예제

##### 참고자료

- https://itmining.tistory.com/4?category=640759
- https://bitsoul.tistory.com/108
- https://velog.io/안드로이드-스레드Thread와-핸들러Handler

## 콜백(Callback)과 리스너(Listener)에 대해서 설명해 주세요.

둘은 비슷한 개념이지만, 콜백은 이벤트 발생 시 특정 메소드를 호출해 알려주고 리스너는 이벤트 발생 시 연결된 리스너들에게 이벤트롤 전달하는 차이가 있습니다. 즉, 리스너를 등록할 수 있는 갯수가 유일한 지, 그렇지 않은 지의 차이입니다. 

##### 참고자료

- https://www.charlezz.com/?p=768
- https://onlyfor-me-blog.tistory.com/47

---
# Reference

* [taeiim 님의 Android Study](https://github.com/taeiim/Android-Study/blob/master/study/week16/안드로이드%20개발자로%20취업하기%20-%20면접/신입%20안드로이드%20개발자로%20취업하기%20-%20면접.md)

* [단계별 예제로 배우는 안드로이드 지식](https://kairo96.gitbooks.io/android/content/)