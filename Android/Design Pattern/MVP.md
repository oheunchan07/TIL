# MVP

## MVP?
> MVP패턴은 Model, View, Presenter를 분리해 뷰와 모덴갈의 의존성을 줄여준다.  
> View에서는 Model을 직접적으로 호출하지 못하고 Presenter를 이용해 호출하게 되고 모델 또한 마찬가지이다.  
> 

![image](https://github.com/oheunchan07/TIL/assets/131967057/f64abe4e-3287-4ea5-946b-8995a8494165)

## MVVM VS MVP
> 얼핏보면 MVVM과 다른게 없어보이지만 자세히 보면 차이가 있다.  
* Presenter: View와 Model에 대한 참조를 가지고 있기 때문에 View가 Presenter에 의존적이다.
* ViewModel: Model에 대한 참조만 가지고 있기 때문에 View가 ViewModel에 의존적이지 않다.