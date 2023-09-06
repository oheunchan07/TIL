# mysql연동

## 1. build.gradle에 있는 dependencies에 아래 코드 추가
```
implementation 'mysql:mysql-connector-java:8.0.32'
implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
```
## 2. 스키마 생성
## 3. application.yml에 아래 코드 추가
```
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/[스키마 이름]
    username: [이름]
    password: [비밀번호]
    driver-class-name: com.mysql.cj.jdbc.Driver

  jpa:
    hibernate:
      ddl-auto: create
    show-sql: true
    properties:
      hibernate:
        format_sql: true
```
