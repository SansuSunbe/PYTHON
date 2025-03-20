# 16강 Collection(컬렉션)-List

# List

- 기존 변수는 일일이 이름을 지정하고 하나의 변수에 하나의 값만 저장이 가능했지만
List는 하나의 저장공간과 이름에 여러 개의 값을 저장이 가능하며 값은 주소값과 방번호(index)로 저장된다.
- index는 항상 0부터 값이 채워진다.
- 규칙성이 없는 값에 규칙성을 부여하기 위해 사용한다.

## List 문법

### 저장 공간 크기 지정

```python
list명 = [값 1, 값2, ...]
```

```python
list명 = [값] * 칸 수
```

### 정해진 저장 공간 크기 없음

```python
list 명 = []
```

### list 길이 확인

```python
len(list 명)
```

## 알고리즘

- 문제를 해결하기 위한 순서 또는 절차

## 자료 구조

- 의미 없는 데이터가 자료 구조를 통과하는 순간 하나의 정보가 된다.

# List 사용 예시

- 삭제와 검색 그리고 수정 시 중복된 값이 있다면 좌에서 우 방향으로 가장 먼저 만난 값의 인덱스 번호를 리턴한다.
- 인덱스 번호는 0부터 시작한다.

### 초기화

```python
dataList = [1, 2, 3]
```

## 값 넣기

### 추가

```python
dataList.append(4)
```

### 결과

```python
dataList = [1, 2, 3, 4]
```

### 삽입

```python
dataList.insert(인덱스 번호, 값)
```

```python
dataList.insert(1, 1.5)
```

### 결과

```python
dataList = [1, 1.5, 2, 3]
```

## 값 삭제

```python
dataList.remove(값)
```

### 인덱스 번호로 삭제

```python
del dataList[인덱스 번호]
```

### 모든 값 삭제

```python
dataList.clear()
```

## 값 검색

### 인덱스 번호로 검색

```python
dataList.index(값)
```

## 값 수정

```python
dataList[인덱스 번호] = 새로운 값
```

# for문 인용

```python
0, ?, 1 --> ?로 사용 가능
```

```python
for in range(len)(list명)) : 
				list명[i] # 리스트의 각 요소
```

# 향상된 for문(빠른 for문, forEach문) 인용

```python
for i in list명 : 
				i # 리스트이 각 요소
```

# 값의 유무 확인

```python
값 in list명 : 조건식(참 or 거짓의 값) list안에 값이 있으면 참
값 not in list명 : list안에 값이 없으면 참
```