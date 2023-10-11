# Extend vs Inplements

## Extend
>Extend는 상속의 대표적인 형태이다  
>부모의 메서드를 그대로 사용가능 하며 오버라이딩 할 필요 없이 부모에 구현되있는 것을 직접 사용 가능하다
```
class Vehicle {
  protected int speed = 3;
  
  public int getSpeed(){
    return speed;
  }
  public void setSpeed(int speed){
    this.speed = speed;
  }
}

class Car extends Vehicle{
  public void printspd(){
    System.out.println(speed);
  }
}

public class ExtendsSample {
  public static main (String[] args){
    Car A = new Car();
    System.out.println(A.getSpeed());
    A.printspd();
  }
}
```
* 자바는 다중 상속을 지원해주 않는다

# Implements
>Implements는 Extend처럼 상속을 받지만 부모의 메소드를 다시 오버라이딩 해야 한다  
>그리고 Implements는 다중상속을 지원해준다
```
interface TestInterface{
  public static int num = 8;
  public void fun1();
  public void fun2();
}

class InterfaceExam implements TestInterface{
  @Override
  public void fun1(){
    System.out.println(num);
  }
  
  @Override
  public void fun2() {
    
  }
}

public class InterfaceSample{
  public static void main(String args[]){
    InterfaceExam exam = new InterfaceExam();
    exam.fun1();
  }
}
```