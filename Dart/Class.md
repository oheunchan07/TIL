# Class

## Class의 형태
```
class 클래스명{
  변수
  함수
}
```

## Constructor
> 클래스에는 생성자가 있어야한다.  
> 객체가 생성될 때 호출된다.

### Named Consturtor
> 생성자에 이름을 부여한다.
> 하나의 클래스에 생성자를 많이 생성할 경우 사용한다.
```
class Person{
  Person.init(){}
}
```

### Constant Constructor
> 생성자를 상수처럼 만들어준다.
> 인스턴스 변수에 모두 ```final```이 붙어야한다.
> 생성자 앞에는 ```const```를 붙여야한다.
```
class Person{
  final String name;
  final int age;
  
  const Person(this.name, this.age);
}
```