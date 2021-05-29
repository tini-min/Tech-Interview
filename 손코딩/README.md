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
### [문제 - 백준 Silver3](https://www.acmicpc.net/problem/1491)

세준이는 밑면이 N*M크기인 궁전에 산다. 세준이는 자신을 남에게 보이는 것을 싫어해서 사람들이 궁전에 자신을 보러 올 때, 되도록 많이 걷게 만들고 싶어한다. 세준이의 보안 담당 은진이는 나선을 설치하는 것을 제안했다.<br><br>

방문자들은 가장 남쪽이면서 서쪽인 곳으로 들어온다. 그래서 가장 동쪽으로 계속해서 나아간다. 만약 방문자들이 벽을 만나거나 자기가 이미 지났던 칸을 만난다면 왼쪽으로 돌아서 앞으로 계속 간다.<br><br>

세준이는 이 나선이 끝나는 곳에 머물고 싶어한다. 나선이 끝나는 곳의 위치를 출력하는 프로그램을 작성하시오.<br><br>

N과 M이 주어졌을 때, 남서쪽 모서리는 (0,0) 남동쪽 모서리는 (N-1,0), 북동쪽 모서리는 (N-1,M-1)이다.<br><br>

**입력**<br>
첫째 줄에 N과 M이 주어진다. N과 M은 5,000보다 작거나 같은 자연수이다.<br><br>

**출력**<br>
첫째 줄에 정답을 출력한다.<br><br>

#### 1. 답안예시 (python -> 구현)

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

2. ** 답안예시 (python -> 수학) **

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

## 달팽이
### [문제 - 백준 Silver](https://www.acmicpc.net/problem/1913)

홀수인 자연수 N이 주어지면, 다음과 같이 1부터 N^2까지의 자연수를 달팽이 모양으로 N×N의 표에 채울 수 있다.<br>

(예시1) N = 3

|9|2|3|
|:---:|:---:|:---:|
|8|1|4|
|7|6|5|

(예시2) N = 5

|25|10|11|12|13|
|:---:|:---:|:---:|:---:|:---:|
|24|9|2|3|14|
|23|8|1|4|15|
|22|7|6|5|16|
|21|20|19|18|17|

N이 주어졌을 때, 이러한 표를 출력하는 프로그램을 작성하시오. 또한 N^2 이하의 자연수가 하나 주어졌을 때, 그 좌표도 함께 출력하시오. 예를 들어 N=5인 경우 6의 좌표는 (4,3)이다.<br>

**입력**
첫째 줄에 홀수인 자연수 N(3 ≤ N ≤ 999)이 주어진다. 둘째 줄에는 위치를 찾고자 하는 N^2 이하의 자연수가 하나 주어진다.<br>

**출력**
N개의 줄에 걸쳐 표를 출력한다. 각 줄에 N개의 자연수를 한 칸씩 띄어서 출력하면 되며, 자릿수를 맞출 필요가 없다. N+1번째 줄에는 입력받은 자연수의 좌표를 나타내는 두 정수를 한 칸 띄어서 출력한다.

#### 답안예시 (python)

```
n = int(input())
target = int(input())

graph = [[0] * n for _ in range(n)]

now = [0, 0] if n % 2 == 1 else [n - 1, n - 1]
dx = [-1, 0, 1, 0]
dy = [0, -1, 0, 1]
rot = 2 * (n % 2)

answer = [0, 0]

for i in range(n * n, 0, -1) :
	x, y = now[0], now[1]
	graph[x][y] = i
	if i == target : answer = [x + 1, y + 1]
	nx, ny = x + dx[rot], y +  dy[rot]
	if (0 <= nx < n) and  (0 <= ny < n) :
		if graph[nx][ny] != 0 : rot = (rot + 1) % 4
	else : rot = (rot + 1) % 4

	now = [x + dx[rot], y +  dy[rot]]

for x in range(n) :
	for y in range(n) :
		print(graph[x][y], end = ' ')
	print()

print(answer[0], answer[1])
```