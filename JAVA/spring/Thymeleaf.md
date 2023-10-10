# Thymeleaf

## Thymeleaf란?
>Thymeleaf란 템플릿 엔진의 일종으로 컨트롤러가 전달하는 데이터를 이용해 동적으로 화면을 만들어주는 역할을 하는 뷰 템플릿 엔진이다

## 특징
* 네츄럴 템플릿(nature template)
>타임리프는 순수 HTML이다  
>그렇기 때문에 확장자도 .html이고 웹브라우저에서도 파일을 열어 내용 확인이 가능하다

*서버 사이드 HTML랜더링 
>백엔드 서버에서는 HTML을 동적으로 랜더링하는 용도로 사용된다

## Thymeleaf를 사용하기 전에 설정
* Build.gradle
```
implementation 'org.springframework.boot:spring-boot-starter-thymeleaf' 
```

* pom.xml
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```
>위 설정을 하고 빌드하면 application.properties에 자동으로 추가된다