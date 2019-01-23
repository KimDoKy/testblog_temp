---
layout: post
section-type: post
title: algorithm - 기초. 피보나치 수열 구하기
category: algorithm
tags: [ 'algorithm' ]
---

> 피보나치 수열 : 앞의 두 수의 합이 뒤의 수가 되는 것  
첫 번째와 두 번째의 숫자의 합이 세 번째 숫자가 됨

### 풀이
1. 사용자로부터 출력하고 싶은 값의 개수를 입력받고 변수에 저장합니다.
2. 피보나치 수열은 0과 1부터 시작하기 때문에 피보나치 수열을 저장할 리스트를 생성해서 미리 0와 1을 넣어둡니다.
3. fibo 리스트에 0과 1이 이미 들어있기 때문에 range함수의 시작을 2로 합니다. 0과 1을 더한 값을 시작으로 피보나치 수열을 구합니다.
4. 구해진 피보나치 수열이 저장된 리스트를 출력합니다.

```python
>>> num = int(input("몇 개의 피보나치 수열 항을 출력할까요?: "))
몇 개의 피보나치 수열 항을 출력할까요?: 17
>>>
>>> fibo = [0,1]
>>> for i in range(2,num):
...     f1 = fibo[i-2]
...     f2 = fibo[i-1]
...     fibo.append(f1 + f2)
...
>>> for f in fibo:
...     print(f)
...
0
1
1
2
3
5
8
13
21
34
55
89
144
233
377
610
987
>>>
````