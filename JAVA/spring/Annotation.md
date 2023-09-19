# Annotation

## Spring Annotation종류
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
* @Bean과 다르게 @Component는 name이 아닌 value를 이용해 Bean의 이름을 저장한다

### @Bean
>개발자가 직적 제어 불가능한 외부 라이브러리를 Bean으로 만들 때 사용하는 어노테이션이다
```
@Configuration
public class ApplicationConfig {    
    @Bean
    public ArrayList<String> array(){
        return new ArrayList<String>();
    }   
}
```

### @Autowired
>field, setter, construct에 사용하면 type에 따라서 Bean을 주입시켜 준다
* 무조건 적인 객체에 대한 의존성을 주입시킨다
