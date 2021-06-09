# Python

<details>
 <summary><strong>참고 지식</strong></summary>
 <div>

- [매크로 라이브러리](https://gyoogle.dev/blog/computer-language/Python/%5BPython%5D%20매크로%20라이브러리.html)
- [enumerate](https://wikidocs.net/20792) : 리스트의 인덱스와 내용을 동시에 참조할 때 유용

</div>
</details>

<details>
 <summary><strong>목차</strong></summary>
 <div>

- [파이썬의 특징을 설명해 주세요.](#파이썬의-특징을-설명해-주세요)
    * [컴파일 언어와 인터프리터 언어의 차이점은 무엇인가요?](#컴파일-언어와-인터프리터-언어의-차이점은-무엇인가요)
    * [.pyc파일과 .py파일이 무엇인가요?](#pyc파일과-py파일이-무엇인가요)
- [mutuable과 immutuable에 대해 설명해 주세요.](#mutuable과-immutuable에-대해-설명해-주세요)
- [파이썬의 삼항연산자에 대해 설명해 주세요.](#파이썬의-삼항연산자에-대해-설명해-주세요)
- [아래 Switch 구문을 파이썬으로 구현해 주세요.](#아래-switch-구문을-파이썬으로-구현해-주세요)
    ```cpp
    using namespace std;

    // Function to convert number into string
    string numbers_to_strings(int argument){
        switch(argument) {
            case 0:
                return "zero";
            case 1:
                return "one";
            case 2:
                return "two";
            default:
                return "nothing";
        };
    };

    int main()
    {
        int argument = 0;
        cout << numbers_to_strings(argument);
        return 0;
    }
    ```

</div>
</details>

## 파이썬의 특징을 설명해 주세요.

- 파이썬은 인터프리터 언어입니다. 따라서 별도의 컴파일 과정이 필요없습니다.
- 파이썬은 동적 타입 언어입니다. 변수의 자료형의 선언하지 않고 값을 지정할 수 있습니다.
- 파이썬은 플랫폼 독립적입니다. 대부분의 운영체제에서 모두 동작하므로 운영체제 별로 컴파일할 필요가 없습니다.
- 파이썬은 객체지향언어를 지향합니다. 완벽하게 구현되지는 않지만 객체지향언어와 유사하게 동작할 수 있습니다.

**장점**

1. 문법이 쉽고 간결합니다. 입문자도 쉽게 익힐 수 있으며, 코딩 시 고려 사항이 적습니다.
1. 빠른 개발 속도를 자랑합니다. 짧고 간결한 문법때문에 생산성이 높습니다. 더 적은 코드로 더 많은 작업을 수행하는 것이 가능하며, 복잡한 구문에서 발생하는 오류를 줄일 수 있습니다.
1. 확장성과 이식성이 높습니다. 다른 언어나 라이브러리를 쉽게 접근하고 연동할 수 있습니다.
1. 생태계가 활발합니다. 수많은 라이브러리가 개발되어 있으며, 개발중에 있습니다.

**단점**

1. 속도가 느린 것이 가장 큰 단점입니다. 인터프리터 언어라는 이유 외에도 동적으로 변수 타입을 지정하기에 해당 과정에서 오버헤드가 발생합니다.

##### 참고자료

- https://library.gabia.com/contents/9256/

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#python)**

### 컴파일 언어와 인터프리터 언어의 차이점은 무엇인가요?

컴파일 언어는 컴파일러를 통해 소스 코드를 기계어로 바꾸는 과정 즉, 실행 파일을 만드는 과정이 필요합니다. 인터프리터 언어는 별도의 컴파일 과정 없이 차례대로 스크립트를 해석하여 코드를 실행합니다. 컴파일 언어는 별도의 컴파일 과정에 실행시간이 소요되지만, 한 번 번역된 파일은 인터프리터 언어에 비해 빠른 실행 속도를 보입니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#python)**

### .pyc파일과 .py파일이 무엇인가요?

.pyc파일은 .py파일이 컴파일된 파일입니다. 파이썬은 인터프리터 언어로 .py파일 만으로도 실행이 가능하지만 실행 시 내부적으로 CPU 혹은 VM이 실질적으로 이해할 수 있도록 기계어로 번역하는 과정이 필요합니다. 이 과정에서 나온 결과물을 .pyc로 저장하는 경우도 있으며, 개발자에 따라 소스 코드를 직접 컴파일하여 생성할 수도 있습니다. .pyc파일은 이미 컴파일된 파일이기에 타 플랫폼에서도 독립적으로 실행될 수 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#python)**

## mutuable과 immutuable에 대해 설명해 주세요.

mutuable(Call by Reference)은 변경 가능한 객체입니다. 리스트와 딕셔너리가 이에 해당되면, 객체의 값이 변경되더라도 값이 변하지 않습니다. 이에 반해, immutuable(Call by Value)은 변경 불가한 객체입니다. 일반적인 자료형과 튜플이 이에 해당되며, 해당 객체는 값이 변경될 시 재할당됩니다.

**예제**
```python
# list

a = [1, 2, 3]
b = a
b[0] = 4 # a = [4, 2, 3], b = [4, 2, 3]
a == b # True

# int

a = 1
b = a
b += 1 # a = 1, b = 2
a == b # False
```

따라서, 리스트나 딕셔너리를 다룰 때에는 주의가 필요합니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#python)**

## 파이썬의 삼항연산자에 대해 설명해 주세요.

```c
int main() {
    int x = 10;
    int y;

    y = (x == 10) ? 5 : -5; // x가 10인 경우 y에 5를 아닌 경우엔 -5를 할당
}
```

위와 같이 3개의 항을 이용한 연산을 삼항 연산자라고 하는데, 파이썬에는 해당 연산자가 없습니다. 다만 아래와 같이 구현할 수 있습니다.

```python
x = 10
y = 5 if x == 10 else -5
```

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#python)**

## 아래 Switch 구문을 파이썬으로 구현해 주세요.

```cpp
#include<bits/stdc++.h>
using namespace std;

// Function to convert number into string
string numbers_to_strings(int argument){
    switch(argument) {
        case 0:
            return "zero";
        case 1:
            return "one";
        case 2:
            return "two";
        default:
            return "nothing";
    };
};

int main()
{
    int argument = 0;
    cout << numbers_to_strings(argument);
    return 0;
}
```

**예시코드**

```python
def numbers_to_strings(argument) :
    return {
        0 : 'zero',
        1 : 'one',
        2 : 'two'
    }.get(argument, 'nothing')
```

파이썬은 딕셔너리를 통해 충분히 스위치 구문을 구현할 수 있으므로 스위치 구문을 지원하지 않습니다. 또한, 함수를 `일급 객체`로 취급하기 때문에 아래와 같은 코드도 가능합니다.

```python
def error(x, y) : return 'error'
def add(x, y) : return x + y
def sub(x, y) : return x - y
def mul(x, y) : return x * y
def div(x, y) :
    if y == 0 : return error(x, y)
    return x // y

oper_code, x, y = map(int, input().split())
oper = {
    0 : add,
    1 : sub,
    2 : mul,
    3 : div
}
print(oper.get(oper_code, error)(x, y))
```

## ETC

<details>
 <summary><strong>한정적인 시간 가운데 선택적으로 공부하지 않은 내용입니다.</strong></summary>
 <div markdown = "1">

>시간적 여유가 있을 때 보충예정

- [제너레이터](https://github.com/JaeYeopHan/Interview_Question_for_Beginner/tree/master/Python#generator)
- 파이썬에서 '_'(언더스코어)의 역활

</div>
</details>

---
# Reference

* [Python 면접 예제 1편](https://dingrr.com/blog/post/python-python-면접-예제-1편)
* [Python 면접 예제 2편](https://dingrr.com/blog/post/python-python-면접-예제-2편)