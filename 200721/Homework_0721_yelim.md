# Homework

## Python 02. 데이터 & 제어문

### 1. Mutable & Immutable

> 주어진 컨테이너들을 각각 변경 가능한 것(mutable)과 변경 불가능한 것(immutable)으로
> 분류하시오.

```python
String. List, Tuple, Range, Set, Dictionary
```

- immutable : String, Range, Tuple

- mutable : List, Set, Dictionary



### 2. 홀수만 담기

> range와 slicing을 활용하여 1부터 50까지의 숫자 중, 홀수로만 이루어진 리스트를
> 만드시오.

```python
#답안 1
numbers = list(range(1, 51, 2))
print(numbers)
```

```python
# 답안 2
numbers = list(range(1, 51))
print(numbers[0:51:2])
```

```python
#답안 3
numbers = list(range(1, 51))
print(numbers[0:len(numbers):2])

print(numbers[::2]) # 이것도 가능 !
```



### 3. Dictionary 만들기

> 반 학생들의 정보를 이용하여 key는 이름, value는 나이인 dictionary를 만드시오.

```python
#답안
{'기예림':'25', '이민정:'27', '이송영':'25', '박예린':'25, '이호창':'27'}
```



### 4. 반복문으로 네모 출력

> 두 개의 정수 n과 m이 주어졌을 때, 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를
> 별(*) 문자를 이용하여 출력하시오. 단, 반복문을 사용하여 작성하시오

```python
n = 5
m = 9
```

```python
#답안
n = 5
m = 9
space = ''

for i in range(m):
    for i in range(n):
        space += '*'
    space += '\n'

print(space)
```

```python
n = 5
m = 9
space = ''

for i in range(m):		# 별 다섯개 출력 
    print()				# 한줄 띄기 
    for i in range(5):
        print('*', end = '')
```



### 5. 조건 표현식

> 주어진 코드의 조건문을 조건 표현식으로 바꾸어 작성하시오.

```python
temp = 36.5
if temp >= 37.5:
    print('입실 불가')
else:
    print('입실 가능')
```

```python
#답안
temp = 36.5
print('입실 불가') if temp >= 37.5 else print('입실 가능')
```



### 6. 평균 구하기

> 주어진 list에 담긴 숫자들의 평균값을 출력하시오.

```python
scores = [80, 89, 99, 83]
```

```python
#답안 1
scores = [80, 89, 99, 83]
averge = sum(scores, 0)/len(scores)
print(averge)
# 결과값: 87.75
```

```python
#답안 2
scores = [80, 89, 99, 83]
result = 0 
for i in range(len(scores)):
    result += scores[i]
print(result / len(scores))
```

