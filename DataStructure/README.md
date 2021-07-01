# Data Structure

<details>
 <summary><strong>목차</strong></summary>
 <div markdown = "1">

- [Linked List를 사용하는 이유는?](#linked-list를-사용하는-이유는)
- [Heap의 삽입과 삭제 구현 방법은?](#heap의-삽입과-삭제-구현-방법은)
- [BST의 문제점은 무엇이 있나요?](#bst의-문제점은-무엇이-있나요)
- [AVL Tree와 Red-Black Tree가 무엇입니까?](#avl-tree와-red-black-tree가-무엇입니까)
- [해시에 대해 설명해 주세요.](#해시에-대해-설명해-주세요)
    * [해시의 충돌 현상을 해결할 수 있는 방법이 어떤 것들이 있나요?](#해시의-충돌-현상을-해결할-수-있는-방법이-어떤-것들이-있나요)

</div>
</details>

## Linked List를 사용하는 이유는?

비슷한 선형 데이터를 저장하는 배열의 경우 크기가 고정되어 있고 새로운 요소를 삽입하는 것은 공간을 만들고 기존 원소를 전부 이동시켜야 하는 등 비용이 많이 듭니다. 하지만 Linked List의 경우 동적으로 크기를 할당하는 것이 가능하고, 삭제와 삽입이 용이합니다. 다만 임의로 엑세스 할 수 없기에 사용에 주의를 요합니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**

## Heap의 삽입과 삭제 구현 방법은?

삽입의 경우 마지막 노드에 삽입 후 힙의 조건을 만족시킬 때까지 부모 노드와 비교와 교체를 반복합니다. 삭제의 경우 최우선 순위 노드(루트 노드)를 삭제 후 마지막 노드를 해당 위치에 가져옵니다. 후에 힙의 조건을 만족시킬 때까지 자식 노드와 비교와 교체를 반복합니다. 힙은 Complete Binary Tree를 만족하므로 높이가 log n입니다. 따라서 삽입, 삭제 모두 O(log n)의 복잡도를 가집니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**

## BST의 문제점은 무엇이 있나요?

편향트리가 발생할 수 있다는 것입니다. 이 경우 높이가 n이 되기 때문에 트리를 사용하는 이점(검색이 빠르다)가 없어집니다. 트리의 편향성을 개선하기 위해 제시된 트리로는 AVL Tree, Red-Black Tree 등이 있습니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**

### AVL Tree와 Red-Black Tree가 무엇입니까?

BST와 가장 큰 차이는 AVL에는 균형인수(Balance Factor)가, Red-Black Tree에는 Color라는 속성이 있어 균형을 유지한다는 점입니다.<br>
AVL Tree의 경우 모든 내부 노드 v에 대하여 v의 자식 노드들의 높이 차이가 최대 1인 성질을 유지해야한다. 이 경우 트리의 높이가 log n이므로 탐색 속도가 O(log n)임을 알 수 있습니다.<br>
Red-Black Tree는 BST에 Color라는 속성과 그에 관한 4가지 조건을 추가한 트리입니다. 4가지 조건은 각각 Root Property, External Property, Internal Property, Depth Property입니다. 루트 노드부터 자식 노드까지의 거리가 최대 2배이기에 탐색시 O(log n)의 복잡도를 가질 수 있습니다.

##### 참조자료

- https://velog.io/@soonbee/AVL-Tree를-알아보자
- https://zeddios.tistory.com/237

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**

## 해시에 대해 설명해 주세요.

데이터를 효율적으로 관리하기 위해, 임의의 길이 데이터를 고정된 길이의 데이터로 매핑하는 것입니다. 데이터가 많아지면 다른 데이터가 같은 해시 값을 가져 Collision현상이 일어나는 단점을 가지고 있지만, 적은 자원으로 많은 데이터를 효율적으로 관리하기 위해 사용됩니다.

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**

### 해시의 충돌 현상을 해결할 수 있는 방법이 어떤 것들이 있나요?

크게 Chaining과 Open Addressing이 있습니다. Chaining은 연결리스트로 노드를 계속 추가(같은 주소로 해싱되는 원소를 추가)해 나가는 방식이며, Open Addressing은 해시 함수로 얻은 주소가 아닌 다른 주소에 데이터를 저장할 수 있도록 허용하는 것입니다. 다음 주소를 결정하는 방식이 다양한데, 대표적으로는 선형 탐사, 제곱 탐사, 더블 해싱이 있습니다. 선형탐사는 정해진 고정 폭으로 옮겨 해시값의 중복을 피하는 방식이며, 제곱 탐사는 정해진 고정 폭을 제곱수로 옯겨 해시값의 중복을 피하는 방식입니다. 더블 해싱은 다른 해시 함수를 통해 2번째 해시 함수값 만큼씩 점프하여 중복을 피하는 방식입니다.

**Chaining과 Open Addressing의 차이점**

|Chaining|Open Addressing|
|:--:|:--:|
|추가적인 공간을 사용한다.|기존 메모리를 사용한다.|
|수정에 대한 작업이 용이하다.<br>(Linked List 수정과 동일)|수정에 대한 작업이 복잡하다.|

**[뒤로](https://github.com/tini-min/Tech-Interview) / [위로](#data-structure)**