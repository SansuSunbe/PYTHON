# 24강 상속(inheritance)

# 상속(inheritance)

1. 기존에 사용 중인 클래스의 필드 중 새롭게 만들 클래스에서 필요한 것들이 있     다면 상속을 받아서 그대로 사용함
2. 여러 클래스를 선언할 때 중복되는 기능들이 존재한다면 공통 기능들을 담아놓을 클래스를 선언한다. 

## 상속 문법

```python
Class A : 
					A필드
					
Class B(A, C, D) : 
					A, B필드
```

## 다중 상속

- 자식 클래스가 상속받는 클래스가 한 개가 아닌 여러 개 상속 받는 것
- 상속을 해주는 부모 클래스가 여러 개인 것

## 모호성

- 여러 부모의 필드 중 같은 이름의 필드를 자식 클래스에서 사용한다면,
어느 부모의 필드인지 알 수가 없기 때문에 이러한 성질을 ‘모호성’이라고 한다.

# 생성자

- 부모 클래스에 생성자가 선언되어 있고,
자식 클래스에는 기본 생성자가 있다면 부모 클래스 생성자를
자동으로 호출해준다.
하지만 자식 클래스에서 생성자를 직접 선언하면 부모 생성자를 자식 생성자에서 
직접 호출해 주어야 한다.

## 자식 클래스에 생성자가 있을 때

- 부모에 있는 필드와 자식에서 필요한 필드가 있을 때
부모 생성자를 호출하여 부모 필드를 초기화 해주고
추가된 자식 필드를 추가로 초기화 해주어야 한다.

## 자식 클래스에 생성자가 없을 때

- 부모의 필드 외에 추가적인 필드가 없을 때, 부모 생성자를 그대로 사용한다.

# 다형성(polymorphism)

## 재정의

- 부모 필드에서 수정하고 싶은 메서드는 자식 필드에서 같은 이름으로 재선언 할 수 있다.
- 항상 부모 생성자가 먼저 호출되어 부모 필드가 메모리에 할당된다.
먼저 할당된 부모 필드에 a라는 메서드가 있다면, 나중에 할당되는 자식 필드의 a메서드의 기능
(소스 코드의 주소값)으로 덮어 씌워 진다.

# 예시

```python
#%% inheritance test2
class Car : 
    wheel = 4
    
    def __init__(self, brand, color, price) : 
        self.brand = brand
        self.color = color
        self.price = price
        
    def enginStart(self) : 
        print(self.brand + "enginStart")
    
    def enginShutDown(self) : 
        print(self.brand + "enginShutDown")
        
class SuperCar(Car) : 
    def __init__(self, brand, color, price, mode) : 
        super().__init__(brand, color, price)
        self.mode = mode
    
    #Overriding
    def enginStart(self) : 
        print(self.brand + "useVoiceEnginStart")
        
    def openRoof(self) : 
        print("openRoof")
        
    def closeRoof(self) : 
        print("closeRoof")
        
ferrari = SuperCar("ferrari", "red", 500000000, "sport")

ferrari.enginStart()
ferrari.enginShutDown()
ferrari.openRoof()
ferrari.closeRoof()

#%% class variable

class A : 
    seq = 0
    
    def __init__(self) : 
        A.seq += 1
        self.num = A.seq
        
    def test(self) : 
        self.seq = 10
        
obj1 = A()
obj2 = A()
obj3 = A()
obj4 = A()

obj1.test()
print(obj1.num)
print(obj1.seq)
print(obj2.num)
print(obj3.num)
```