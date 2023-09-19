# Annotation

## spring annotation종류
### @Component
>개발자가 직접 작성한 Class를 Bean으로 등록하기 위한 어노테이션이다
```
@Component
public class Student {
    public Student() {
        System.out.println("hi");
    }
}
```
* Component에 대한 추가 정보가 없으면 cameCase로 Bean id로 사용된다
