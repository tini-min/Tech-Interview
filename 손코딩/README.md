# 손코딩 문제

**개인적으로 기술 면접을 대비하면서 손코딩 문제 및 예상 답안입니다.**
> 대부분의 문제는 백준 브론즈~실버3 수준입니다.

## Min_Stack 구현
> 최솟값을 O(1) 연산으로 도출하는 Stack을 파이썬으로 구현

```python
class Stack :
	def __init__(self) :
		self.container = []
		self.min_cont = []

	def push(self, elem) :
		self.container.append(elem)

		if not self.min_cont : self.min_cont.append(elem)
		else :
			if self.min_cont[-1] >= elem : self.min_cont.append(elem)

	def pop(self) :
		if len(self.container) == 0 : return None

		top = self.container.pop()
		if self.min_cont[-1] == top : self.min_cont.pop()

		return top

	def size(self) :
		return len(self.container)

	def empty(self) :
		return int(not self.container)

	def top(self) :
		if self.size() == 0 : return None
		return self.container[-1]

	def min(self) :
		if len(self.container) == 0 : return None
		return self.min_cont[-1]
```

## 나선
### [문제 - 백준 Siver3](https://www.acmicpc.net/problem/1491)

세준이는 밑면이 N*M크기인 궁전에 산다. 세준이는 자신을 남에게 보이는 것을 싫어해서 사람들이 궁전에 자신을 보러 올 때, 되도록 많이 걷게 만들고 싶어한다. 세준이의 보안 담당 은진이는 나선을 설치하는 것을 제안했다.<br><br>

방문자들은 가장 남쪽이면서 서쪽인 곳으로 들어온다. 그래서 가장 동쪽으로 계속해서 나아간다. 만약 방문자들이 벽을 만나거나 자기가 이미 지났던 칸을 만난다면 왼쪽으로 돌아서 앞으로 계속 간다.<br><br>

세준이는 이 나선이 끝나는 곳에 머물고 싶어한다. 나선이 끝나는 곳의 위치를 출력하는 프로그램을 작성하시오.<br><br>

N과 M이 주어졌을 때, 남서쪽 모서리는 (0,0) 남동쪽 모서리는 (N-1,0), 북동쪽 모서리는 (N-1,M-1)이다.<br><br>

**입력**<br>
첫째 줄에 N과 M이 주어진다. N과 M은 5,000보다 작거나 같은 자연수이다.<br><br>

**출력**<br>
첫째 줄에 정답을 출력한다.<br><br>

1. 답안예시 (python -> 구현)

```python
x, y = map(int, input().split())
dx = [1, 0, -1, 0]
dy = [0, 1, 0, -1]
rotate = 0

now = [-1, 0]
while x != 0 and y != 0 :
	now[0] += x * dx[rotate % 4]; now[1] += y * dy[rotate % 4];
	rotate += 1
	x -= 1 * abs(dx[rotate % 4]); y -= 1 * abs(dy[rotate % 4]);
print(now[0], now[1])
```

2. 답안예시 (python -> 수학)

```python
w, h = map(int, input().split())
short = min(w, h)
x = y = 0
cycle = short // 2

if short % 2:
    x = cycle + w - h if w >= h else cycle
    y = cycle if w >= h else cycle + h - w

else:
    x = cycle - 1
    y = cycle
print(x, y)
```