# 05강 format과 형변환

# 서식 문자

1. %
2. “”.format()

# 형변환

1. 자동 형변환
    - 정수 + 정수 = 정수
    - 정수 + 실수 = 실수
    - 3 + 0.0 = 3.0
2. 강제 형변환
    - 자료형(값)
    - int(10.98) == 10

# 아스키 코드

- 컴퓨터가 문자를 기억하고 있는 정수 값
- ex)
    - A : 65
    - a : 97

# 예시 1

```python
#%% format test
data = 10
data2 = "%d" %100
print("data : %d" %data)
print(type(data2))
print(data2)

# 결과 : 
# data : 10
# <class 'str'>
# 100
```

# 예시 2

```python
#%% foramt test2
# 문자열값.format
# A.B : A안에 B
data1 = 10
data2 = 10.4231
data3 = 'A'
data4 = "ABC"
print("data1 : {}".format(data1))
print("data1 : {}\ndata2 : {}".format(data1, data2))
print("data3 : %s" %data3)
print("data3 : %c" %data3)
# print("data4 : %c" %data4)
print("data : %c" %65)
print("data : %c" %66)
print("data : %c" %67)

# 아스키 코드
print("아스키코드 a : %c" %97)

# 결과 : 
# data1 : 10
# data1 : 10
# data2 : 10.4231
# data3 : A
# data3 : A
# data : A
# data : B
# data : C
# 아스키코드 a : a

```

# 자동 형변환 예시

```python
#%% 자동 형변환
# // : 몫 연산자
print(10/3)
print(10//3.0)

# 결과 :
# 3.3333333333333335
# 3.0 
```

# 강제 형변환 예시

```python
#%% 강제 형변환
print(float(10)//3) 

# 결과 : 
# 3.0
```