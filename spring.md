# 스프링
### 스프링 프레임워크
 - 자바 플렛폼을 위한 오픈소스 어플리케이션 프레임워크
 - 경량급 프레임워크를 활용하여 어플리케이션의 개발을 편리하게 해주는 것
 - 경량컨테이너로 자바 객체를 직접관리
 - 생성 소멸 라이프사이클을 관리하여 스프링으로부터 필요한 객체를 얻음
 - IoC : 컨트롤의 제어권이 사용자가 아닌 컨테이너에 있어 필요에 따라 스프링에서 코드를 호출
 - DI : 객체들간의 의존성을 줄이기 위해 사용되는 Spring IoC의 컨테이너 구체적인 구현방식, 팩토리 패턴처럼 객체의 생성과, 데이터를 주입만 담당하는 factory에 해당하는 별도의 공간에서 객체를 생성하고 데이터간의 의존성을 주입해 개발코드는 이를 가져다씀으로 의존성을줄임 즉, 유연한 확장아 가능하게한다.
 - Aop : 관점지향프로그래밍, 트랜잭션, 로깅 등 공통적인 기능과 핵심기능을 분리하여 관리한다.

### IoC & DI
 - IoC: 스프링에서 오브젝트의 생성과 관계설정, 사용, 제거등 어플리케이션의 코드등은 스프링 컨테이너가 담당한다. 이를 컨테이너가 코드대신 제어권을 갖고있다해서 IoC라 불린다.
 - 스프링 컨테이너는 ApplicationContext를 구현한 것을 말한다.
 - DI: 자신이 사용할 오브젝트에 대한 선택과, 생성 제어권을 외부로 넘기고, 주입받은 외부객체를 사용한다
   - 장점: 코드에는 런티암 클래스에 대한 관계가 나타나지 않음
   - 인터페이스를 통해 낮은 결합도
   - 다른 책임을 가진 객체가 수정되더라도 자신은 영향을 받지않음
   - 변경을 통한 확장이 자유롭다.


### POJO
 - 각자 기능에 충실하게 독립된 클래스, 결합도를 낮추고 유연한 관계를 가질수있도록 인터페이스를 연결해준다.
 
### 스프링 부트
 - 간편한 설정, 편리한 의존성관리 & 자동 권장버전 관리, 내장서버로 인한 간단한 배포 서버 구축
 - 라이브러리 관리 자동화 : 기존 스프링 프로젝트에서 라이브러리 의존성 관리를함, 부트에서는 start라는 것을 이용하여 특정 기능에 필요한 라이브러리 의존성을 간단히 처리
 - 설정 자동화 : 추가된 라이브러리 기반으로 환경을 자동으로 설정
 - 라이브러리 버전 자동관리 : 개발에만 집중할 수 있도록 환경을 제공
 - 내장 톰켓, 테스트 환경 : Junit을 비롯한 테스트 관련 라이브러리들이 기본적으로 포함, main() 메소드를 가진 클래스를 실행하느 방식으로 실행결과를 빠르게 확인할 수 있음
 - 독립적으로 실행 가능한 JAR : 기존에는 WAR로 페키징해야했지만 부트는 JAR로 패키징하여 사용할 수 있음
 - 어노테이션 : @Configuration

 ### JAR vs WAR
  - JAVA Archive, Web Application Archive
  - JAR는 자바 환경위에서 동작할 수 있는것 .class 설정 파일들일 모여있음
  - War는 Jsp, WAs 컨테이너 위에서 동작하게끔 빌드된 형태 web.xml 설정들을 불러옴
  - jar 파일안에 was가 내장되어 jar로 빌드가 가능 -> 스프링부트

### 필터 vs 인터셉터
 - 실행시점의 차이
 - 필터는 wep application에 등록, 인터셉터는 spring context 등록
 - 필터는 dispatherServlet 앞단에서 정보처리, DispatcherServlet에 controller로 가기전에 정보처리
 - 필터는 주로 인코딩, 보안 관련같은 전역적으로 처리해야할 때, 클라이언트로 들어오는 디테일한 처리를 인터셉터(인증, 권한)

 ### 스프링 MVC 구조처리과정
 - DispathcerServlet 컨트롤러 앞 단에서 요청을 가로챔
 - DispathcerServlet이 handlerMapping에게 처리할 컨트롤러를 요청하고
 - controller가 비지니스로직을 수행 후 모델에 데이터를 담고 뷰와함께 DispathcerServlet에게 전달
 - DispathcerServlet는 뷰 리졸버에게 해당 뷰를 찾아달라고 요청
 - 뷰 리졸버는 해당 뷰를 DispathcerServlet에게 전달
 
### 객체 주입방법
 - 생성자 주입 : 생서자 호출 시점에 1회 호출을 보장하며 주입받은 객체가 변하지 않거나, 반드시 주입해야하는 경우에 해당한다. 생상자 주입을 통행 불변성보장( 컴파일시점에 객체를 주입받아 테스트코드를 작성하며, 주입하는 객체가 컴파일 시점에 누라된 경우 확인 가능)
 - 세터 주입 : 주입받은 객체가 변경할 가능성이 있을 때 
 - 필드 주입 : 외부에서 변경 불가능, 테스트 코드 작성시 테스트 코드를 작성할 수가 없음

 ### 스프링 시큐리티 과정
 - 사용자가 로그인을 하면 AuthenticationFilter가 userpasswordAuthenticationToken을 생성
 - AuthenticationManager에게 토큰 전달하여 등록된 AuthenticationProvider를 조회하여 인증요구
 - Provider는 UserDetailService를 통해 입력받은 사용자 아이디를 DB에서 조회함
 - 입력받은 비밀번호를 암호화하여 DB의 비밀번호와 매칭하고 성공되면 token을 manager에게 반환
 - manager는 그것을 다시 filter로 전달
 - 필터는 전달받은 token을 LoginSuccessHandler에게 전송하고 SecurityContextHolder에 저장
 