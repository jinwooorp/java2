# 202430132 진현우


#### 0605

##### 어뎁터 클래스

- 리스너의 모든 메소드를 단순 리턴하기 위해 만든 클래스

##### 유니 코드 키

- 국제 산업 표준
- 전 세계의 문자를 컴퓨터에서 일관되게 표현하기 위한 코드 체계
- 문자가 아닌 키 경우에는 표준화된 키 코드 값이 없다


##### mouse 이벤트

- 프레스: 마우스를 누름
- 클릭: 프레스 + 릴리즈
- 릴리즈: 어디서 때던 상관없다

#### 0529

#### 이벤트 기반 프로그래밍
- 이벤트의 발생에 의해 프로그램 흐름이 결정됨
- 이벤트가 발생 -> 이벤트를 처리(이벤트 리스너)
- 반대 개념: 배치실행, 프로그램의 개발자가 흐름을 결정

##### 이벤트 종류

- 사용자 입력: 마우스 드래그, 마우스 클릭, 키보드 입력등
- 센서로부터의 입력,네트워크로 부터 데이터 송수신

##### 이벤트 객체
- 발생한 이벤트에 관한 정보를 가진 객체
- 이벤트 리스너에 전송됨
- : 이벤트 리스너 코드가 발생한 이벤트에 대한 상황을 파악할 수 있게 함

##### 이벤트 객체가 포함하는 정보
- 이벤트 종류와 소스
- 이벤트가 발생한 화면 좌표 및 컴포넌트 내 좌표
- 이벤트가 발생한 버튼이나 메뉴 아이템의 문자열
- 클릭된 마우스 버튼 번호 및 클릿 횟수
- 등등

##### 이벤트 리스너 작성
- 독립 클래스로 작성
- 완전한 클래스로 작성
- 여러 곳에서 사용할 때 적합
- 내부 클래스로 작성

- 익명 클래스로 작성

##### swing 프레임

- 모든 스윙 컴포넌트를 담는 최상위 컨테이너
- jframe을 상속받아 구현
- 컴포넌트들은 화면에 보이려면 스윙 프레임에 부착되어야함
- 프레임을 닫으면 프레임에 부착된 모든 컴포넌트가 보이지 않게된다.
- 프레임의 크기를 반드시 지정해야하며 setSize()를 호출한다.
- 화면에 출력하는 코드는 또한 필요하며 setVisible(true)로 호출

#### 0522

##### swing

- awt 기술을 기반으로 작성된 라이브러리
- 모든 awt 기능 + 추가된 풍부하고 화려한 고급 컴포넌트이다.
- 순수 자바 언어로 구현됨
- 현재 자바의 gui 표준으로 사용됨

##### hashmap

- key 와 value의 쌍으로 구성되는 요소를 다루는 컬렉션
- 값을 검색할려면 key가 필요함
- c++ map이랑 비슷하다
- 삽입할 때 put() 

##### 박싱/언박싱

- 1.5 버전 이전에느느 기본 타입 데이터를 wrapper 객체로 만들어 삽입
- 1.5 이후 부터 자동 박싱/언박싱이 작동되며 기본 타입 값 삽입 가능
- 허나 매개변수를 기본타입으로 구체화 안됨

##### vector

- 맨뒤나 앞에 삽입가능
- 삭제는 임의의 위치에서 가능


#### 0515

##### 스트링 리터널

- jvm 내부에서 리터널 테이블에 저장되고 관리된다.
- 예) String s = "Hello"

- new String으로 객체를 생성할 때 스트링 객체는 힙에 생성됨
- 스트링은 공유되지 않음

- 수정이 불가하다

- 스트링 비교를 할 때 equals()를 사용해서 비교하자
- compareTo 는 문자열이 같을 경우 0을 리턴
- 기준값과 비교값이 다른 경우 중간부터 같은 문자일 경우 각각의 문자열에서 가장 낮은 아스키 코드의 차이를 리턴한다.
##### 박싱과 언박싱

- 기본 타입의 값을 wrapper 객체로 변환시킴 -> 박싱
- wrapper 객체에 들어있는 기본 타입을 뺴내는 것 -> 언박싱

##### wrapper 클래스

- 자바의 기본 타입을 클래스화 한 8개 클래스를 총칭한다.
- 객체만 사용할 수 있는 컬렉션 등에 기본타입의 값을 사용하기 위해 wrapper 클래스로 만들어서 사용한다.
- 기본 타입과 차이점은 대문자로 시작한다.

##### 자바 플랫폼의 모듈화

- jdk와 jre을 지칭함
- 자바 api 모든 클래스가 여러 개의 모듈로 재구성됨
- 모듈 파일은 jdk의 jmod 디렉토리에 저장됨

##### 자바 모듈화의 목적

- 자바 컴포넌트들을 필요에 따라 조립하기 위해 사용힌다.
- 컴퓨터 시스템에 불필요한 부담을 감소시킨다.

#### 0508

##### 패키지 만들기

- 클래스나 인터페이스가 컴파일 되면 클래스 파일(.class) 생성
- 클래스 파일은 패키지로 선언된 디렉토리에 저장
- 선언은 소스파일 맨 앞에 컴파일 후 저장될 패키지 지정 -> package 패키지명;

##### 패키지란

- 서로 관련된 클래스와 인터페이스를 컴파일한 클래스 파일을 묶어놓은 디렉토리

- 하나의 응용프로그래밍은 한 개 이상의 패키로 작성
##### 모듈

- 여러 패키지와 이미지등의 자원을 모아놓은 컨테이너
- 하나의 모듈을 하나의 .jmod 파일에 저장

##### 인터페이스
- 클래스가 구현해야할 메소드 표시

##### 구성 요소들

- 상수는 public만 허용 , public, static, final 생략
- 추상 메소드: public, abstract 가능

##### 추상클래스

- 추상 메소드를 가지며 , abstract로 선언한다
- 추상 메소드 없이, abstract로 선언한 클래스

#### 0418

##### final 

- 상수를 실행할 때 사용
- 상수 필드는 선언 시 초기값을 지정해야함
- 실행 중 수정불가

##### 상속의 필요성

- 중복된 멤버들을 상속을 이용해서 코드관리가 편리해진다
- 상속을 할 때 extends를 사용한다.

##### 자바 상속 특징

- 하나의 클래스에게만 상속 받을 수 있다. -> 다중 상속 X
- 허나 interface에서 다중 상속을 지원함 

##### 서브 클래스와 슈퍼 클래스의 생성자 선택

- 둘 다 각각의 생성자 작성 가능
- 서브 클래스의 객체가 생성될 때 수퍼 클래스 생성자 1개와 서브 클래스 생성자 1개가 생김

##### 업캐스팅

- 서브 클래스의 래퍼런스를 슈퍼 클래스 레퍼런스에 대입
- 슈퍼 클래스 레퍼런스로 서브 클래스 객체를 가르키게 되는 현상

##### 업캐스팅 레퍼런스로 객체 구별
- 업캐스트된 레퍼런스는 객체의 실제 타입을 구분하기 어렵다.
- 그래서 instanceof를 사용한다.

##### 메소드 오버라이딩
- 서브 클래스에서 슈퍼 클래스의 메소드 중복
- 오버라이딩으로 다향성을 실현
- 하나의 인터페이스에서 서로 다른 구현이 가능
- 수퍼 클래스의 메소드를 서브 클래스에서 각각 목적에 맞게 구현 가능

#### 0417

##### static

- static 멤버는 클래스당 하나만 생성
- static 멤버는 클래스 이름으로 접근 가능
- 객체의 멤버로 접근 가능
- 허나 non static 멤버는 클래스로 접근이 안된다.
- 전역변수를 만들 때 사용한다.
- static 메소드는 오직 static 멤버만 접근 가능
- static 메소드는 non static 멤버를 사용 불가

##### 객체 소멸
- new로 할당받은 객체와 메모리를 jvm이 되돌려 주는 것
- 자바는 free() 처럼 객체 소멸 연산자가 없다
- 객체 소멸은 jvm의 고유한 역할


##### 배열생성

``` Circle[] c = new Circle[5]; ```

#### 메소드
- c/c++에서 함수와 비슷함
- java의 모든 메소드는 반드시 클래스 안에 있어야함
- 기본타입으로 선언 되었을 때, 호출자가 건네는 값이 매개변수에 복사되서 전달됨


##### this
- 자기자신을 지칭한다

#### 0410
##### 클래스
- 자바의 객체 지향 특성: 캡슐화
- 캡슐화란 객체들을 캡슐로 싸서 내부를 볼수없게 하는 것
- 객체의 가장 본질적인 특징
- 외부의 접근으로 부터 보호

###### 클래스와 객체
- 객체란 클래스의 툴로 찍어낸 실체
- 클래스는 class 키워드로 선언

###### 상속
- 하위 객체가 상위 객체의 모든 속성을 가짐

###### 객체지향 언어의 목적
- 소프트웨어 생명주기 단축
- 빠른 속도로 생산할 필요성 증대

###### 생성자
- 객체가 생성될 때 초기화 목적으로 실행되는 메소드

#### 0403
- while,do while, for문 등 반복문 사용법 등을 알아보았다.
- 헝가리안 로테이션에 대해 배웠다.

#### 0327

###### var 
- 타입을 생략하고 번수 선언 가능

- 초기값을 안 주면 컴파일 할 때 오류 발생

###### 메모리 구조
- 힙 영역은 프로그래머가 직접 할당, 해제하는 공간이며
java의 경우 JVM이 담당

- 스택영역은 프로그램이 자동으로 사용하는 임시 메모리 영역

- 힙이 스택을 침범하는 경우 힙 오버 플로우, 반대 상황일 경우 스택 오버 플로우라고 한다.

###### 참조 자료형을 쓰는 이유
- 포인터를 사용하면 특정 메모리 주소를 직접 조작할 수 있기에

###### 데이터 타입
- 기본 자료형은 대체로 같음
- 클래스에 대한 레퍼런스
- 인터페이스에 대한 레퍼런스
- 배열에 대한 레퍼런스

###### 식별자 명명규칙
- 식별자란? 클래스,변수,상수,메소드 등에 붙이는 이름
- 특수문자,공백 또는 탭 사용 불가 (' _ ', '$' 은 사용가능)
- 유니코드 문자 사용가능(한글사용 가능)
- 식별자의 첫 번째 문자로 숫자 X
- 자바의 키워드 사용불가
- 길이 제한 없음
- 대소문자 구별

#### 0320
- 기본적인 깃 사용법
- JDK 안에 많은 실행 파일들이 있다.
  그 중 javac와 java 가 있다
  javac는 자바 파일을 바이트 코드로 컴파일 하며,
  컴파일 된 파일을 .class 파일로 저장한다.
  또한 java로 javac로 컴파일한 .class 파일을 실행할 수 있다.

- 묘듈화 방식은 생산성을 높이는 방법이다.
- 자바는 운영체제의 도움없이 멀티스레드를 지원한다.
##### java 네이밍 방식
-버전 1.6 부터 java SE 뒤에 숫자를 붙이는 방식이다.



