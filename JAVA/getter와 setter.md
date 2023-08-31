# getter와 setter

## getter와 setter의 역할: private를 관리하는 메소드
<br>

## getter란?
* private에서 값을 빼내는 메소드
## setter란?
* private에 값을 넣는 메소드
<br>

## 선언 방법
```
private 타입 fieldName;

//Getter
public 리턴타입 getFieldName() {
    return fieldName;
}

//Setter
public void setFieldName(타입 fieldName) {
    trhis.fieldName = fieldName;
}
```
