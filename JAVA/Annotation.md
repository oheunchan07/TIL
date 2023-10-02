# Annotation

## JAVA 내장Annotation종류
### @Override
>메소드를 오버라이드 할 때에 사용된다  
>오버라이딩을 올바르게 했는지 컴파일러가 체크하게 한다
```
@Override
public void getInfo() {
  System.out.println("test");
}
```
* 만약 상속받은 부모 클래스 또는 구현해야할 인터페이스에 해당 메소드가 없다면 컴파일 오류를 발생시킨다

### @Deprecated
>앞으로는 사용하지 않을 필드나 메서드에 붙힌다  
>이 클래스를 사용하지 않는다 해서 삭제하면 호환성에 문제를 줄 수 있어 삭제하지 않고 호환성을 위한 어노테이션이다

### @SuppressWarnings
>경고를 제거하는 어노테이션이다  
>개발자가 의도를 가지고 설계했는데 컴파일러가 알아차리고 경고를 띄우는 것을 막는 어노테이션이다

### @SafeVarargs
>제너릭 같은 가변인자 매개변수들을 사용할 때의 경고를 무시

### @FunctionalInterface
>함수형 인터페이스를 지정하는 어노테이션이다
