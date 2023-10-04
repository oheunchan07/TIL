# Annotation

## Lombok Annotation종류
### @Getter/@Setter
>getter/setter를 생성해준다
```
@Getter
@Setter
public class User {
    private String name;
    private Integer age;
}
```
>이 어노테이션을 쓰지 않는다면 아래 코드처럼 길어진다
```
public class User {
    private String name;
    private Integer age;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setAge(Integer age) {
        this.age = age;
    }

    public Integer getAge() {
        return age;
    }
}
```

### @Notnull
>필드에 지정해주면 null-check를 해준다  
>null값이 들어왔을 경우에는 NPE를 발생시킨다

### @ToString
>Class에 있는 맴버 변수들을 문자열로 변환하여 return하는 ToString메소드를 생성한다

### @RequiredArgsConstructor
>final필드와 @NotNull로 마크되어 있는 필드들한테 생성자를 자동으로 생성시켜준다

### @Data
>이 어노테이션들을 한 번에 설정해준다
* @Getter / @Setter
* @RequiredArgsConstructor
* @ToString
* @EqualsAndHashCode
