## 싱글톤 패턴(Singleton Pattern)

### 객체(Object)

 - 객체: 속성과 기능을 갖춘 것
 - 클래스: 속성과 기능을 정의한 것
 - 인스턴스: 속성과 기능을 가진 것 중 실제 하는 것

### 싱글톤 패턴
 - 객체의 인스턴스를 **하나만** 생성하기 위한 패턴

![image](https://user-images.githubusercontent.com/50781066/209508210-68a299a7-2431-408d-85fe-54c155a58c25.png)

#### 사용하는 이유

 1. **메모리 측면**에서 남비를 방지할 수 있다.
 2. **데이터 공유가 쉽다.**
 3. 이 외에도 인스턴스가 한 개만 존재하는 것을 보증하고 싶은 경우 사용한다.

#### 문제점

 1. 싱글톤 패턴을 구현하는 **코드 자체가 많이 필요**하다.
    - 객체 생성을 확인하는 코드와 생성자를 호출하는 경우 멀티 스레드 환경에서 발생할 수 있는 동시성 문제 해결을 위해 Synchronized 키워드를 사용해야 한다.
 2. 자원을 공유하고 있기 때문에 **테스트하기 어렵다.**
    - 매번 인스턴스의 상태를 초기화시켜주어야 한다.
 3. new 키워드를 직접 사용하여 객체를 생성하기 때문에 **의존관계상 클라이언트가 구체 클래스에 의존**하게 된다.
    - SOLID 원칙 중 DIP를 위반하고, OCP 원칙 또한 위반할 가능성이 있다. 

- 생성(Creational) 패턴
    + 객체 생성에 관련된 패턴
    + 객체의 생성과 조합을 캡슐화해 특정 객체가 생성되거나 변경되어도 프로그램 구조에 영향을 크게 받지 않도록 유연성을 제공한다.