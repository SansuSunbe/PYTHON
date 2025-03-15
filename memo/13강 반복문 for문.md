# 13강 반복문 for문

# for문 문법

```python
for 변수명 in range(초기값, 끝 값, 증감값) :
					반복할 문장
```

# for문 예시 문제

```python
#%% for test
    for i in range(0, 10, 1) :
        print("%d. for문법" %(i + 1))
        
    for i in range(10, 0, -1) :
        print("%d. for문법" %i)
    
#%% 0부터 1씩 증가시키는 for문을 작성(10번 반복)
# 단, 10 ~ 1까지 출력    
    for i in range(0, 10, 1) :
        print(10 - i)
    
# n + 0 = 10
# 1. n = 10
# 2. 10 - 0

#%% 1번
# 1 ~ 100까지 출력
    for i in range(0, 100, 1) :
        print((i + 1));
#%% 2번 
# 100 ~ 1까지 출력
    for i in range(100, 0, -1) :
        print(i)
#%% 3번
# 1 ~ 100까지 중 짝수만 출력
    for i in range(0, 50, 1):
        print((i + 1) * 2);
#%% 4번
# A ~ F까지 출력
# start가 0일 때에는 생략이 가능하다.
# step이 1일 때에는 생략이 가능하다.
# for i in range(0, 6, 1) :
    for i in range(0, 6, 1) : 
        print(chr(i + 65))
#%% 5번
# A ~ F까지 중 C 제외하고 출력
    # for i in range(5) :
    #     # 0 1 2 3 4 5
    #     # A B C D E F
    #     if i > 1 :
    #         i += 1
    #        
    #     print(chr(65 + i))
     
    temp = 0
    for i in range(5) : 
        # i 값을 직접 변경하지 않고
        # temp라는 변수에 담고 temp를 변경한다.
        # temp는 임시저장공간이고, i는 값
        temp = i
        temp = temp + 1 if i > 1 else temp
        print(chr(65 + temp))
        
#%% 6번
# aBcDeFgHiJkLmNoPqRsTuVwXyZ 출력
# 97 66 99
    for i in range(26) : 
        # ??? % 2 == 0 짝수
        # ??? % 2 == 0 홀수
        
        print(chr(97 + i if i % 2 == 0 else 65 + i), end = "")
```