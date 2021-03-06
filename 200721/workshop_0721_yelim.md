# workshop

## Python 02. 데이터 & 제어문

### 1. 간단한 N의 약수 (SWEA #1933)

> 입력으로 1개의 정수 N이 주어진다. 정수 N의 약수를 오름차순으로 출력하는 프로그램
> 을 작성하시오.

```python
[제약 사항]
N은 1이상 1,000이하의 정수이다. (1 ≤ N ≤ 1,000)
[입력]
입력으로 정수 N이 주어진다.

[출력]
정수 N의 모든 약수를 오름차순으로 출력한다.

[입력 예시]
10

[출력 예시]
1 2 5 10
```

```python

N = int(input('정수를 입력해주세요 : '))
# 정수는 1부터 1000까지 
for i in range(1, N+1):
    if N % i == 0:
        print(i, end=" ")

```





### 2. 중간값 찾기 (SWEA #2063 변형)

>중간값은 통계 집단의 수치를 크기 순으로 배열 했을 때 전체의 중앙에 위치하는 수치를
>뜻한다. 리스트 numbers에 입력된 숫자에서 중간값을 출력하라.

```python
[출력 예시]
64

numbers = [
    85, 72, 38, 80, 69, 65, 68, 96, 22, 49, 67, 51,61, 63, 
    87, 66, 24, 80, 83, 71, 60, 64, 52, 90, 60, 49, 31, 23, 
    99, 94, 11, 25, 24
]

```

```python
import statistics
numbers = [
    85, 72, 38, 80, 69, 65, 68, 96, 22, 49, 67, 51,61, 63, 
    87, 66, 24, 80, 83, 71, 60, 64, 52, 90, 60, 49, 31, 23, 
    99, 94, 11, 25, 24
]
print(statistics.median(numbers))
```

```python
numbers = [
    85, 72, 38, 80, 69, 65, 68, 96, 22, 49, 67, 51,61, 63, 
    87, 66, 24, 80, 83, 71, 60, 64, 52, 90, 60, 49, 31, 23, 
    99, 94, 11, 25, 24
]
sorted_num = sorted(numbers)
center = len(numbers) // 2

print(sorted_num[center])
```



### 3. 계단 만들기

> 자연수 number를 입력 받아, 아래와 같이 높이가 number인 내려가는 계단을 출력하시오.

```python
[입력 예시]
4

[출력 예시]
1
1 2
1 2 3
1 2 3 4
```

```python
num = int(input('자연수를 입력해주세요 : '))

for i in range(1,num+1):
    space = ''
    for j in range(1,i+1):
        space = space + str(j) + ' '
    print(space)
```





### 4. 구구단을 외자, 구구단을 외자 2 X 1 ?!

> 2단부터 9단까지 for문을 사용하여 아래와 같은 구구단을 출력하시오.

```python
[출력 예시]
------- [2 단] -------
2 X 1 = 2
2 X 2 = 4
2 X 3 = 6
2 X 4 = 8
2 X 5 = 10
2 X 6 = 12
...

------- [3 단] -------
...
```

```python
for n in range(1, 10):
    for m in range(1,10):
        print(f'{n} X {m} = {n * m}')
        
    print(f'--------- [{n} 단] ---------')
```

