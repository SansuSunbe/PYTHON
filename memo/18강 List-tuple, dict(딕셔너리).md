# 18강 List-tuple, dict(딕셔너리)

# List과 Tuple의 차이

## List

### mutable(변할 수 있는) : list

```python
#%% mutable
dataList1 = [1, 2, 3]
dataList2 = dataList1

dataList2.append(4)

print(dataList1)

# 결과
# [1, 2, 3, 4]
```

## Tuple

### immutable(변할 수 없는) : tuple

```python
#%% immutable
# dataTuple1 = (1, 2, 3)
dataTuple1 = 1, 2, 3
# print(type(dataTuple1))
dataTuple2 = dataTuple1

dataTuple2 += 4, 5

print(dataTuple1)
# dataTuple1[0] = 10 : 튜플의 값은 수정할 수 없음
print(dataTuple1[0])
```

# dict

- 한 쌍으로 저장되어 관리한다.
- len()를 사용하면 한 쌍을 1로 카운트한다.
- 키 값은 중복이 될 수 없으며, 값은 중복이 가능하다.
- 키 값을 주면 그 키의 짝꿍 값을 가지고 온다.

## 문법

```python
dict명 = {키 : 값, 키 :값...}
```

# dict 사용 예시

## 추가(키 값이 없을 때)

```python
dict명[키] = 값
```

## 수정(키 값이 있을 때)

```python
dict명[키] = 값
```

## 삭제(한 쌍이 삭제됨)

```python
del dict명[키]
```

## 검색

### 키 값이 있으면 참

```python
키 in dict명 
```

### 키 값이 없으면 참

```python
키 not in dict명 
```

## Key 분리

```python
list(dict명.keys())
```

## value 분리

```python
dict명.values()
```

# dict 실습

```python
#%% dict 테스트
chinaFood = {"짜장면" : 1500, "짬뽕" : 2000}

print(len(chinaFood))
print(chinaFood["짜장면"])

if "짜장면" in chinaFood : 
    chinaFood["짜장면"] = 2000

print(chinaFood)

if "탕수육" not in chinaFood : 
    chinaFood["탕수육"] = 10000
    
print(chinaFood)

# del chinaFood["짬뽕"]
# print(chinaFood)

print()

for i in chinaFood.keys() : 
    print(i)
    
for i in range(len(chinaFood)) : 
    print(str(i + 1) + ". " + list(chinaFood.keys())[i])
    
total = 0
for i in chinaFood.values() :
    total += i

avg = total / len(chinaFood)
# print("평균 가격 : " + str(avg) + "원")
print("평균 가격 : %.1f원" %avg)

#%% dict task
# 등급을 입력받아서 학점을 출력하는 프로그램
# ex) 2 입력 시 B학점 출력
# 1 ~ 5등급, A ~ F학점(E학점)

scoreDict = {}
# 0 1 2 3 4
# A B C D F
for i in range(5) :
    scoreDict[i + 1] = chr(i + 66)if i == 4 else chr(i + 65)

# print(scoreDict)

rating = int(input("등급 : "))

for i in range(5) : 
    if rating == i + 1 : 
        print("학점 : " + scoreDict[rating])
        break
```