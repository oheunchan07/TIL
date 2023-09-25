# spring 3대 요소

## IOC(Inversion of Control): 제어의 역전
>IOC자체에서 객체를 생성해주고 관리하고 책임지고 의존성을 관리하는 컨테이너
* DI(Dependency Injection): 의존성 주입
* 각 클래스간의 의존관계를 Bean을 바탕으로 컨테이너가 자동 연결해준다

## AOP(Aspect Oriented Programming): 관점 지향 프로그래밍
>AOP는 애플리케이션에 공통적으로 나타나는 부가적인 기능들을 독립적으로 모듈화 시켜놓은 프로그래밍 모델이다<br>
>예로 `@Transactional`이 있다
* 기존의 코드에 첨삼 없이 메소드의 호출 이전이나 이후에 필요한 로직을 수행하는 방법을 제공

## PSA(Portable Service Abstraction): 일관성 있는 서비스 추상화
>추상화 계층을 사용하여 어떤 기술은 내부에 숨기고 개발자에게 편의성을 제공해주는 것을 서비스 추상화라고 한다
>spring web MVC Transaction등이 있다
>한 마디로 정리하면 아주 잘 만든 인터페이스라고 한다 -백기선-
