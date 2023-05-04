# HTML

## HTML이란?
#### HTML이란 Hyper Text Markup Language의 약자로 웹페이지를 만드는 언어를 뜻한다
- - -
## HTML 문법
* ### TAG
```
<strong></strong>
```
#### `<strong></strong>` : 사이에 있는 텍스트를 강조 표시
<br><br>

```
<u></u>
```
#### `<u></u>` : 사이에 있는 텍스트 아래에 밑줄
<br><br>

```
<h1></h1>
```
#### `<h1></h1>` : 중요도에 따라 뒤에 숫자를 바꿔서 테스트의 크기를 바꿈
<br><br>

```
<br> ,<p></p>
```
#### `<br>` : 줄바꿈 <br>※무엇인가를 설명하지 않는 태그들은 감싸야 하는 텍스트가 없어 태그를 닫지 않는다
#### `<p></p>` : 사이에 있는 텍스트를 그룹핑 시킴
<br><br>

```
<img src="이미지 파일.jpg">
```
#### `<img>` : 이미지 파일을 출력
#### ※width를 통해 크기를 조종 할 수 도 있음 
<br><br>

```
<ul>,<ol>
  <li></li>
</ul>,</ol>
```
#### `<li></li>` : 목차를 정해준다
#### `<ul></ul>` : 목차를 나눠준다
#### `<ol></ol>` : 목차를 숫자로 표현해 나눠준다
<br><br>

```
<meta charset="utf-8">
```
#### `<meta charset="utf-8">` : 영어가 아닌 다를 문자들을 꺠지지 않게 해준다
<br><br>

```
<title></title>
```
#### `<title></title>` : 웹페이지의 이름을 바꿔준다
<br><br>

```
<!doctype html>
```
#### `<!doctype html>` : 이 웹페이지가 HTML로 만들어졌다는 것을 표현하기 위해 문서의 시작에 아래와 같은 코드를 추가한다
<br><br>

```
<html>
<head>
  
</head>
<body>

</body>
</html>
```
#### `<html></html>` : body태그와 html태그를 감싸주는 하나의 태그 
#### `<head></head>` : 본문 태그
#### `<body></body>` : 본문을 설명하는 태그
<br><br>

```
<a href="링크 파일">
```
#### `<a href="링크 파일">` : 링크를 걸어준다
#### ※`target="_blank"`를 추가해주면 새창에서 페이지가 열린다