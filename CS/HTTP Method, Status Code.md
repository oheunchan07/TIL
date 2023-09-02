
# CS기초단어

## HTTP Method
### HTTP Method는 크게 GET, POST, PUT, DELETE가 대표적이다

### HTTP Method의 종류
* GET: 서버로 부터 데이터를 취득
* POST: 서버에 데이터를 추가, 작성
* PUT: 서버의 데이터를 갱신, 작성
* DELETE: 서버의 데이터를 삭제
* HEAD: 서버 리소스의 헤더
* OPTION: 리소스가 지원하고 있는 데이터를 메소드의 취득
* PATCH: 리소스의 일부를 취득
* CONNECT: 프록시 동작의 터널 접속을 변경

## Status Code
### Status Code란? 클라이언트가 서버에 요청을 보낼 때 그 결과가 어떻게 되었는지를 알려주어 요청이 성공적인지 에러가 발생했는지를 알 수 있다

### 1XX: Information response
* 서버가 요청을 받았으며 서버에 연결된 클라이언트는 계속 잡업을 하라는 뜻이다

### 2XX: Successful responese
* 서버의 요청이 성공하면 2XX대에 Status Code를 받게 된다

### 3XX: Redirection message
* 클라이언트는 request를 마치기 전에 추가 동작을 해야 할 경우 3XX대에 Status Code를 받게 된다

### 4XX: Client error response
* request에 오류가 있을을 알려주는 Status Code를 받게 된다

### 5XX: Server errrors
* 서버 오류가 발생항 경우에 5XX대에 Status Code를 받게 된다
