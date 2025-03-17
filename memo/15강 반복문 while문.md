# 15강 반복문 while문

# While문

- 조건식이 참이면 반복
- 반복 횟수를 모를 때 사용하는 목적
- 무한 반복일 경우, 특정 조건에 break를 사용해서 탈출

## for문과의 차이

- for문은 반복 횟수를 알 때 사용
- while문은 반복 횟수를 모를 때 사용

## 문법

```python
while 조건식 : 
					반복할 문장
```

# 예시 1

```python
#%% while Test
# 이름 10번 출력
# cnt = 0
# while cnt != 10 : 
#     print("{}.whileTest".format(cnt))
#     cnt += 1
```

# 예시 2

```python
#%% while Task
qMsg = ("MBTI 유형별 성격\n"
        + "1.I\n2.E\n3.J\n4.P\n5.나가기\n")

answer_1 = "소심"
answer_2 = "적극"
answer_3 = "계획"
answer_4 = "무계획"
errMsg = "종료"

while True : 
    choice = int(input(qMsg))
    result = ""
    
    if choice == 1 : 
        result = answer_1
    elif choice == 2 :
        result = answer_2
    elif choice == 3 :
        result = answer_3
    elif choice == 4 :
        result = answer_4
    elif choice == 5 :
        break
    else : 
        result = errMsg
        
        print(result)
```

# 예시 3

```python
#%% while Task 2
qMsg = "다음 중 프로그래밍 언어가 아닌 것은?"
choiceMsg = "1.JAVA\n2.파이썬\n3.C Language\n4.엄준식\n"
choice = int(input(qMsg + "\n" + choiceMsg))
result = ""

answer = 4     

while result != "정답" : 
    if choice == answer : 
        result = "정답"
    elif choice >= 1 and choice <= 4 : 
        result = "오답"
    else : 
        result = "잘못된 입력"
    print(result)
    break
```