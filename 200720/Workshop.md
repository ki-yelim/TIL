# Workshop
### 1. 세로로 출력하기

> 자연수 number를 입력 받아, 1부터 number까지의 수를 세로로 한줄씩 출력하시오

```python
# 아래에 코드를 작성하시오.
number = int(input('숫자를 입력해주세요 : '))
cnt = 1
while cnt <= number:
    print(cnt)
    cnt += 1
```



### 2.  가로로 출력하기

> 자연수 number를 입력 받아, 1부터 number까지의 수를 가로로 한칸씩 띄어 출력하시오.

```python
# 아래에 코드를 작성하시오.
number = int(input('숫자를 입력해주세요 : '))
for i in range(1, number+1):
    print(i, end=" ")
```



### 3. 거꾸로 세로로 출력하기

> 자연수 number를 입력 받아, number부터 1까지의 수를 세로로 한줄씩 출력하시오.

```python
# 아래에 코드를 작성하시오.
number = int(input('숫자를 입력해주세요 : '))
cnt = 1
while cnt <= number:
    print(number)
    number-=1
```



### 4. 거꾸로 출력해 보아요 (SWEA #1545)

>자연수 number를 입력 받아, number부터 0까지의 수를 가로로 한칸씩 띄어 출력하시오.

```python
# 아래에 코드를 작성하시오.
number = int(input('숫자를 입력해주세요 : '))
for i in range(0, number+1):
    print(number, end=" ")
    number -=1
```



### 5. N줄 덧셈 (SWEA #2025)

>입력으로 자연수 number가 주어질 때, 1부터 주어진 자연수 number까지를 모두 더한 값을 출력하시오. 단, 주어지는 숫자는 10000을 넘지 않는다. 예를 들어, 주어진 숫자가 10일 경우 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 = 55이므로, 출력해야 할 값은 55이다.

```python
# 아래에 코드를 작성하시오.
number = int(input('숫자를 입력해주세요 : '))
cnt = 0
Plus = 0
while cnt <= number:
    Plus = Plus + number
    number-=1
print(Plus)

```