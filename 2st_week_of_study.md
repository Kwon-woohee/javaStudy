# 목표
자바의 프리미티브 타입, 변수 그리고 배열을 사용하는 방법을 익힙니다.

## 학습
### 프리미티브 타입과 레퍼런스 타입
1. Primitive Type
  * 8가지의 Data Type만이 존재한다.
  * primitive type만이 연산이 가능하다.
  * 실제 값을 저장하는 공간으로 Stack메모리에 저장된다.
  * 기본값이 존재한다.
2. Reference Type
  * primitive type을 제외한 모든 타입은 reference type이다.
  * 실제 값을 저장하는 것이 아닌 저장되어있는 장소의 주소 값을  저장하는 공간으로  Heap메모리에 저장된다.
  * 기본값이 없기때문에 null로 표현한다.

### 프리미티브 타입 종류와 값의 범위 그리고 기본 값
1. 프리미티브 타입의 종류
- 논리형 : boolean
- 정수형 : byte, short, int, long
- 실수형 : float, double
- 문자형 : char

2. 값의 범위
- 논리형
  * boolean : true, false
- 정수형
  - byte : -128 ~ 127
  - short : -32,768 ~ 32,767
  - int : -2,147,483,648 ~ 2,147,483,647
  - long : -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807
- 실수형
  - float : (3.4 X 10-38) ~ (3.4 X 1038) 의 근사값
  - double : (1.7 X 10-308) ~ (1.7 X 10308) 의 근사값
- 문자형
  - char : 0 ~ 65,535

3. 기본 값
 - 논리형
   * boolean : false
 - 정수형
   - byte : 0
   - short : 0
   - int : 0
   - long : 0
 - 실수형 
   - float : 0
   - double : 0
 - 문자형
   - char : 0
### 리터럴
* 값을 의미한다.
* `int a = 5;` 에서 리터럴은 5에 해당한다.

### * 변수 선언 및 초기화하는 방법
* 변수 선언
    - 데이터타입 데이터이름;
      ex) `int a;`
      ex) `Date d = Date();`

* 초기화하는 방법
    1. 선언과 동시에 초기화
      - 데이터타입 데이터이름 = 데이터값;
      ex) `int a = 0;`
    2. 선언한 후 초기화
      - 데이터타입 데이터이름;
      ex) `int a;`
      - 데이터이름 = 데이터값;
      ex) `a = 0;`

### * 변수의 스코프와 라이프타임
* 변수의 스코프(영역)
    * 변수에 접근하거나 접근 할 수 있는 유효 범위/영역을 말한다.
    * 일반적으로 변수가 선언된 블록({})내에서만 엑세스 할 수 있다.     
* 라이프 타임
    * 객체가 메모리에 살아있는 기간을 말한다.

* Instacne Variables에서의 scope와 LifeTime(life cycle)
 정의 : 클래스 내부와 모든 메소드 및 블록 외부에서 선언된 변수
 scope : 정적 메서드를 제외한 클래스 전체
 라이프타임 : 객체가 메모리에 남아있을 때까지.
 ex) x와 y의 scope
`
class Sample {
    int x, y; //인스턴스 변수
    static int result;
    void add(int a, int b) {
        x = a;
        y = b;
        int sum = x + y;
        System.out.println("Sum = " + sum);
    }

    pubilc static void main(String[] args) {
        Sample obj = new Sample();
        obj.add(10, 20);
    }
}
`

* Class Variables
 정의 : 클래스 내부, 모든 블록 외부에서 선언되고 static으로 표시된 변수
 scope : 클래스 전체
 라이프타임 : 프로그램이 끝날때까지 또는 클래스가 메모리에 로드 되는 동안
 예시 : result(class variable)의 scope


* Local Variables
 정의 : 인스턴스 및 클래스 변수가 아닌 모든 변수
 scope : 선언된 블록 내에 있음
 라이프타임 : 컨트롤이 선언 된 블록을 떠날때까지
 예시 : a, b (local variable)의 scope

### * 타입 변환, 캐스팅 그리고 타입 프로모션
* 타입 변환
* 캐스팅
* 타입 프로모션

### * 1차 및 2차 배열 선언하기
* 1차 배열 선언하기
* 2차 배열 선언하기

### * 타입 추론, var
* 타입추론
* var