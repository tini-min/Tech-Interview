# 손코딩 문제

**개인적으로 기술 면접을 대비하면서 손코딩 문제 및 예상 답안입니다.**
> 대부분의 문제는 백준 브론즈~실버3 수준입니다.

## Min_Stack 구현
> 최솟값을 O(1) 연산으로 도출하는 Stack을 파이썬으로 구현

<details>
<summary><strong> 답안예시 (python) </strong></summary>
<div class="colorscripter-code" style="color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#fafafa;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #e5e5e5"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#666;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div><div style="line-height:130%">8</div><div style="line-height:130%">9</div><div style="line-height:130%">10</div><div style="line-height:130%">11</div><div style="line-height:130%">12</div><div style="line-height:130%">13</div><div style="line-height:130%">14</div><div style="line-height:130%">15</div><div style="line-height:130%">16</div><div style="line-height:130%">17</div><div style="line-height:130%">18</div><div style="line-height:130%">19</div><div style="line-height:130%">20</div><div style="line-height:130%">21</div><div style="line-height:130%">22</div><div style="line-height:130%">23</div><div style="line-height:130%">24</div><div style="line-height:130%">25</div><div style="line-height:130%">26</div><div style="line-height:130%">27</div><div style="line-height:130%">28</div><div style="line-height:130%">29</div><div style="line-height:130%">30</div><div style="line-height:130%">31</div><div style="line-height:130%">32</div><div style="line-height:130%">33</div><div style="line-height:130%">34</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#a71d5d">class</span>&nbsp;Stack&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;__init__(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#066de2">self</span>.container&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;[]</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#066de2">self</span>.min_cont&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;[]</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;push(<span style="color:#066de2">self</span>,&nbsp;elem)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#066de2">self</span>.container.append(elem)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#a71d5d">not</span>&nbsp;<span style="color:#066de2">self</span>.min_cont&nbsp;:&nbsp;<span style="color:#066de2">self</span>.min_cont.append(elem)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">else</span>&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#066de2">self</span>.min_cont[<span style="color:#0086b3"></span><span style="color:#a71d5d">-</span><span style="color:#0099cc">1</span>]&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">&gt;</span><span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;elem&nbsp;:&nbsp;<span style="color:#066de2">self</span>.min_cont.append(elem)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;pop(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#066de2">len</span>(<span style="color:#066de2">self</span>.container)&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span><span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;<span style="color:#0099cc">0</span>&nbsp;:&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">None</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;top&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;<span style="color:#066de2">self</span>.container.pop()</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#066de2">self</span>.min_cont[<span style="color:#0086b3"></span><span style="color:#a71d5d">-</span><span style="color:#0099cc">1</span>]&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span><span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;top&nbsp;:&nbsp;<span style="color:#066de2">self</span>.min_cont.pop()</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">return</span>&nbsp;top</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;size(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">len</span>(<span style="color:#066de2">self</span>.container)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;empty(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">int</span>(<span style="color:#a71d5d">not</span>&nbsp;<span style="color:#066de2">self</span>.container)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;top(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#066de2">self</span>.size()&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span><span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;<span style="color:#0099cc">0</span>&nbsp;:&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">None</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">self</span>.container[<span style="color:#0086b3"></span><span style="color:#a71d5d">-</span><span style="color:#0099cc">1</span>]</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">def</span>&nbsp;min(<span style="color:#066de2">self</span>)&nbsp;:</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">if</span>&nbsp;<span style="color:#066de2">len</span>(<span style="color:#066de2">self</span>.container)&nbsp;<span style="color:#0086b3"></span><span style="color:#a71d5d">=</span><span style="color:#0086b3"></span><span style="color:#a71d5d">=</span>&nbsp;<span style="color:#0099cc">0</span>&nbsp;:&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">None</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#a71d5d">return</span>&nbsp;<span style="color:#066de2">self</span>.min_cont[<span style="color:#0086b3"></span><span style="color:#a71d5d">-</span><span style="color:#0099cc">1</span>]</div></div><div style="text-align:right;margin-top:-13px;margin-right:5px;font-size:9px;font-style:italic"><a href="http://colorscripter.com/info#e" target="_blank" style="color:#e5e5e5text-decoration:none">Colored by Color Scripter</a></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#e5e5e5;color:white;border-radius:10px;padding:1px">cs</span></a></td></tr></table></div>
</details>

## 나선
### [문제 - 백준 Silver3](https://www.acmicpc.net/problem/1491)

세준이는 밑면이 N*M크기인 궁전에 산다. 세준이는 자신을 남에게 보이는 것을 싫어해서 사람들이 궁전에 자신을 보러 올 때, 되도록 많이 걷게 만들고 싶어한다. 세준이의 보안 담당 은진이는 나선을 설치하는 것을 제안했다.<br>

방문자들은 가장 남쪽이면서 서쪽인 곳으로 들어온다. 그래서 가장 동쪽으로 계속해서 나아간다. 만약 방문자들이 벽을 만나거나 자기가 이미 지났던 칸을 만난다면 왼쪽으로 돌아서 앞으로 계속 간다.<br>

세준이는 이 나선이 끝나는 곳에 머물고 싶어한다. 나선이 끝나는 곳의 위치를 출력하는 프로그램을 작성하시오.<br>

N과 M이 주어졌을 때, 남서쪽 모서리는 (0,0) 남동쪽 모서리는 (N-1,0), 북동쪽 모서리는 (N-1,M-1)이다.<br>

**입력**<br>
첫째 줄에 N과 M이 주어진다. N과 M은 5,000보다 작거나 같은 자연수이다.<br>

**출력**<br>
첫째 줄에 정답을 출력한다.<br>

<details>
<summary style = "font-weight:bold"> 답안예시 1 (python -> 구현) </summary>
<pre><code class = 'python'>
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
</code></pre>
</details>

<details>
<summary style = "font-weight:bold"> 답안예시 2 (python -> 수학) </summary>
<pre><code class = 'python'>
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
</code></pre>
</details>

## 달팽이
### [문제 - 백준 Silver3](https://www.acmicpc.net/problem/1913)

홀수인 자연수 N이 주어지면, 다음과 같이 1부터 N<sup>2</sup>까지의 자연수를 달팽이 모양으로 N×N의 표에 채울 수 있다.<br>

**(예시1) N = 3**

|9|2|3|
|:---:|:---:|:---:|
|8|1|4|
|7|6|5|

**(예시2) N = 5**

|25|10|11|12|13|
|:---:|:---:|:---:|:---:|:---:|
|24|9|2|3|14|
|23|8|1|4|15|
|22|7|6|5|16|
|21|20|19|18|17|

<br>N이 주어졌을 때, 이러한 표를 출력하는 프로그램을 작성하시오. 또한 N<sup>2</sup> 이하의 자연수가 하나 주어졌을 때, 그 좌표도 함께 출력하시오. 예를 들어 N=5인 경우 6의 좌표는 (4,3)이다.<br>

**입력**<br>
첫째 줄에 홀수인 자연수 N(3 ≤ N ≤ 999)이 주어진다. 둘째 줄에는 위치를 찾고자 하는 N<sup>2</sup> 이하의 자연수가 하나 주어진다.<br>

**출력**<br>
N개의 줄에 걸쳐 표를 출력한다. 각 줄에 N개의 자연수를 한 칸씩 띄어서 출력하면 되며, 자릿수를 맞출 필요가 없다. N+1번째 줄에는 입력받은 자연수의 좌표를 나타내는 두 정수를 한 칸 띄어서 출력한다.

<details>
<summary style = "font-weight:bold"> 답안예시 (python) </summary>
<div markdown="1">
```python
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
</div>
</details>

## 두 수의 합
### [문제 - 백준 Silver4](https://www.acmicpc.net/problem/3273)

n개의 서로 다른 양의 정수 a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>으로 이루어진 수열이 있다. a<sub>i</sub>의 값은 1보다 크거나 같고, 1000000보다 작거나 같은 자연수이다. 자연수 x가 주어졌을 때, a<sub>i</sub> + a<sub>j</sub> = x (1 ≤ i < j ≤ n)을 만족하는 (a<sub>i</sub>, a<sub>j</sub>)쌍의 수를 구하는 프로그램을 작성하시오.<br>

**입력**<br>
첫째 줄에 수열의 크기 n이 주어진다. 다음 줄에는 수열에 포함되는 수가 주어진다. 셋째 줄에는 x가 주어진다. (1 ≤ n ≤ 100000, 1 ≤ x ≤ 2000000)<br>

**출력**<br>
문제의 조건을 만족하는 쌍의 개수를 출력한다.<br>

<details>
<summary style = "font-weight:bold"> 답안예시 1 (python -> dictionary) </summary>
<div markdown="1">
```python
from bisect import bisect_left

n = int(input())
arr = list(map(int, input().split()))
arr.sort()
x = int(input())

dic = {}
for i in arr :
	dic[i] = x - i

answer = 0
for i in arr :
	ind = bisect_left(arr, dic[i])
	if ind == n : continue
	if arr[ind] == dic[i] : answer += 1
print(answer // 2)
```
</div>
</details>

<details>
<summary style = "font-weight:bold"> 답안예시 2 (python -> two pointer)  </summary>
<div markdown="1">
```python
n = int(input())
arr = list(map(int, input().split()))
arr.sort()
x = int(input()) 

answer = 0
start, end = 0, n - 1 

while start < end : 
	if arr[start] + arr[end] == x:
		answer += 1
		start += 1
		end -= 1
	elif arr[start] + arr[end] > x:
		end -= 1
	else:
		 start += 1 

print(answer)
```
</div>
</details>

## 삼각형으로 자르기
### [문제 - 백준 Silver3](https://www.acmicpc.net/problem/1198)

볼록 다각형이 있고, 3개의 연속된 점을 선택해서 삼각형을 만든다. 그 다음이 만든 삼각형을 다각형에서 제외한다. 원래 다각형이 N개의 점이 있었다면, 이제 N-1개의 점으로 구성된 볼록 다각형이 된다.<br>

위의 과정은 남은 다각형이 삼각형이 될 때까지 반복한다.<br>

볼록 다각형의 점이 시계 방향순으로 주어진다. 마지막에 남은 삼각형은 여러 가지가 있을 수 있다. 이때, 가능한 넓이의 최댓값을 구하는 프로그램을 작성하시오.<br>

**입력**<br>
첫째 줄에 볼록 다각형 점의 수 N (3 ≤ N ≤ 35)이 주어진다. 둘째 줄부터 N개의 줄에는 점이 시계 방향 순서대로 주어진다. 좌표는 10,000보다 작거나 같은 자연수이다.<br>

**출력**<br>
첫째 줄에 문제의 정답을 출력한다. 절대/상대 오차는 10<sup>-9</sup>까지 허용한다.<br>

<details>
<summary style = "font-weight:bold"> 답안예시 (python) </summary>
<div markdown="1">
```python
from itertools import combinations

n = int(input())
points = []
answer = 0

for _ in range(n) :
	a, b = map(int, input().split())
	points.append((a, b))

for tri in combinations(points, 3) :
	surf = 0
	for i in range(3) :
		surf += tri[i][0] * tri[(i + 1) % 3][1]
		surf -= tri[i][1] * tri[(i + 1) % 3][0]

	answer = max(answer, abs(surf) / 2)

print(answer)
```
</div>
</details>

## 정렬 알고리즘 작성

시간복잡도가 최악인 경우 O(n log n)인 정렬 알고리즘을 작성하시오

<details>
<summary style = "font-weight:bold"> 답안예시 1 (python : Merge Sort) </summary>
<div markdown="1">
```python
def merge(arr1, arr2) :
	sorted_arr = []
	while arr1 :
		if not arr2 :
			sorted_arr.reverse()
			return arr1 + sorted_arr
		elif arr1[-1] >arr2[-1] :
			sorted_arr.append(arr1.pop())
		else :
			sorted_arr.append(arr2.pop())

	sorted_arr.reverse()
	return arr2 + sorted_arr

def mergeSort(arr) :
	if len(arr) <= 1 : return arr

	mid = len(arr) // 2
	arr1 = mergeSort(arr[:mid])
	arr2 = mergeSort(arr[mid:])

	return merge(arr1, arr2)
```
</div>
</details>

<details>
<summary style = "font-weight:bold"> 답안예시 2 (python : Heap Sort) </summary>
<div markdown="1">
```python
import heapq

def heapSort(arr) :
	heapq.heapify(arr)
	sorted_arr = []

	while arr :
		sorted_arr.append(heapq.heappop(arr))

	return sorted_arr
```
</div>
</details>

<details>
<summary style = "font-weight:bold"> (보충) Heap 구현 </summary>
<div markdown="1">
```python
def heapSort(arr) :
	for i in range(1, len(arr)) :
		now = i
		while now != 0 :
			par = (now - 1) // 2
			if arr[par] < arr[now] :
				arr[par], arr[now] = arr[now], arr[par]
			now = par

	for i in range(len(arr) - 1, -1, -1) :
		arr[0], arr[i] = arr[i], arr[0]
		par = 0
		now = 1

		while now < i :
			now = 2 * par + 1
			if now < i - 1 and arr[now] < arr[now + 1] :
				now += 1

			if now < i and arr[par] < arr[now] :
				arr[par], arr[now] = arr[now], arr[par]
			par = now

	return arr
```
</div>
</details>

<details>
<summary> (번외) Quick Sort는 평균적인 시간 복잡도는 O(n log n)이지만 최악의 경우 O(n^2)이 된다. </summary>
<div markdown="1">
```python
def quickSort(arr) :
	if len(arr) <= 1 : return arr

	pivot = arr[0]
	tail = arr[1:]
	left_side = [x for x in tail if x <= pivot]
	right_side = [x for x in tail if x > pivot]

	return quickSort(left_side) + [pivot] + quickSort(right_side)
```
</div>
</details>

### 좌표 압축
#### [문제 - 백준 Silver2](https://www.acmicpc.net/problem/18870)

수직선 위에 N개의 좌표 X1, X2, ..., XN이 있다. 이 좌표에 좌표 압축을 적용하려고 한다.<br>

X<sub>i</sub>를 좌표 압축한 결과 X'<sub>i</sub>의 값은 X<sub>i</sub> > X<sub>j</sub>를 만족하는 서로 다른 좌표의 개수와 같아야 한다.<br>

X<sub>1</sub>, X<sub>2</sub>, ..., X<sub>N</sub>에 좌표 압축을 적용한 결과 X'<sub>1</sub>, X'<sub>2</sub>, ..., X'<sub>N</sub>를 출력해보자.<br>

**입력**<br>
첫째 줄에 N이 주어진다.<br>

둘째 줄에는 공백 한 칸으로 구분된 X<sub>1</sub>, X<sub>2</sub>, ..., X<sub>N</sub>이 주어진다.<br>

**출력**<br>
첫째 줄에 X'<sub>1</sub>, X'<sub>2</sub>, ..., X'<sub>N</sub>을 공백 한 칸으로 구분해서 출력한다.<br>

**제한**<br>
1 ≤ N ≤ 1,000,000<br>
-10<sup>9</sup> ≤ X<sub>i</sub> ≤ 10<sup>9</sup><br>

<details>
<summary style = "font-weight:bold"> 답안예시 (python) </summary>
<div markdown="1">
```python
from bisect import bisect_left

n = int(input())
arr = list(map(int, input().split()))

sorted_arr = sorted(list(set(arr)))
for i in arr :
	print(bisect_left(sorted_arr, i), end = ' ')
```
</div>
</details>

## 최소공배수
### [문제 - 백준 Silver5](https://www.acmicpc.net/problem/1934)

두 자연수 A와 B에 대해서, A의 배수이면서 B의 배수인 자연수를 A와 B의 공배수라고 한다. 이런 공배수 중에서 가장 작은 수를 최소공배수라고 한다. 예를 들어, 6과 15의 공배수는 30, 60, 90등이 있으며, 최소 공배수는 30이다.<br>

두 자연수 A와 B가 주어졌을 때, A와 B의 최소공배수를 구하는 프로그램을 작성하시오.<br>

**입력**<br>
첫째 줄에 테스트 케이스의 개수 T(1 ≤ T ≤ 1,000)가 주어진다. 둘째 줄부터 T개의 줄에 걸쳐서 A와 B가 주어진다. (1 ≤ A, B ≤ 45,000)<br>

**출력**<br>
첫째 줄부터 T개의 줄에 A와 B의 최소공배수를 입력받은 순서대로 한 줄에 하나씩 출력한다.<br>

<details>
<summary style = "font-weight:bold"> 답안예시 1 (python -> math 모듈) </summary>
<div markdown="1">
```python
import math

t = int(input())
for tc in range(t) :
	x, y = map(int, input().split())
	gcd = math.gcd(x, y)
	print(x * (y // gcd))
```
</div>
</details>

<details>
<summary style = "font-weight:bold"> 답안예시 2 (python -> 수학) </summary>
<div markdown="1">
```python
t = int(input())
for tc in range(t) :
	x, y = map(int, input().split())
	x, y = (x, y) if x >= y else (y, x)

	arr = [x, y]
	while arr[-2] % arr[-1] != 0 :
		arr.append(arr[-2] % arr[-1])

	gcd = arr[-1]
	print(x * (y // gcd))
```
</div>
</details>

## 피보나치 함수
### [문제 - Silver3](https://www.acmicpc.net/problem/1003)

다음 소스는 N번째 피보나치 수를 구하는 C++ 함수이다.<br>

```cpp
int fibonacci(int n) {
    if (n == 0) {
        printf("0");
        return 0;
    } else if (n == 1) {
        printf("1");
        return 1;
    } else {
        return fibonacci(n‐1) + fibonacci(n‐2);
    }
}
```

fibonacci(3)을 호출하면 다음과 같은 일이 일어난다.<br>

fibonacci(3)은 fibonacci(2)와 fibonacci(1) (첫 번째 호출)을 호출한다.<br>
fibonacci(2)는 fibonacci(1) (두 번째 호출)과 fibonacci(0)을 호출한다.<br>
두 번째 호출한 fibonacci(1)은 1을 출력하고 1을 리턴한다.<br>
fibonacci(0)은 0을 출력하고, 0을 리턴한다.<br>
fibonacci(2)는 fibonacci(1)과 fibonacci(0)의 결과를 얻고, 1을 리턴한다.<br>
첫 번째 호출한 fibonacci(1)은 1을 출력하고, 1을 리턴한다.<br>
fibonacci(3)은 fibonacci(2)와 fibonacci(1)의 결과를 얻고, 2를 리턴한다.<br>
1은 2번 출력되고, 0은 1번 출력된다. N이 주어졌을 때, fibonacci(N)을 호출했을 때, 0과 1이 각각 몇 번 출력되는지 구하는 프로그램을 작성하시오.<br>

**입력**<br>
첫째 줄에 테스트 케이스의 개수 T가 주어진다.<br>

각 테스트 케이스는 한 줄로 이루어져 있고, N이 주어진다. N은 40보다 작거나 같은 자연수 또는 0이다.<br>

**출력**<br>
각 테스트 케이스마다 0이 출력되는 횟수와 1이 출력되는 횟수를 공백으로 구분해서 출력한다.<br>

<details>
<summary style = "font-weight:bold"> 답안예시 1 (python -> 시간복잡도 각 테스트 케이스별 O(n)) </summary>
<div markdown="1">
```python
t = int(input())
d = [[0, 0] for _ in range(41)]
d[0] = [1, 0]; d[1] = [0, 1];
for i in range(2, 41) :
	d[i][0] = d[i - 1][0] + d[i - 2][0]
	d[i][1] = d[i - 1][1] + d[i - 2][1]

for tc in range(t) :
	n = int(input())
	print(d[n][0], d[n][1])
```
</div>
</details>

<details>
<summary style = "font-weight:bold"> 답안예시 2 (python -> 시간복잡도 각 테스트 케이스 별 O(2^n)) </summary>
<div markdown="1">
>백준 채점 시 시간 초과 발생

```python
def fibonacci(n, cnt) :
	if n == 0 :
		cnt[0] += 1
		return cnt
	if n == 1 : 
		cnt[1] += 1
		return cnt
	else : 
		prev, pprev = fibonacci(n - 1, cnt), fibonacci(n - 2, cnt)
		cnt[0] += prev[0] + pprev[0]; cnt[1] += prev[1] + pprev[1];
		return cnt

t = int(input())
for tc in range(t) :
	n = int(input())
	cnt = fibonacci(n, [0, 0])
	print(cnt[0], cnt[1])
```
</div>
</details>