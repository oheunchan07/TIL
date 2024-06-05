# MVVM

## MVVM?
> MVVM패턴은 Model, View, ViewModel을 분리해 뷰와 모덴갈의 의존성을 줄여준다.  
> 여기서 ViewModel은 View와 Model 사이에서 뷰에 이벤트에 따라 모델이 데이터를 저장이나 반환하도록 통시해주는 역활이다.
> 이런 구조를 갖게 된다면 View와 Model을 분리시켜 로직을 작성하고 ViewModel을 통해 데이터와 통신 할 수 있다.

![image](https://github.com/oheunchan07/TIL/assets/131967057/7e588672-648e-4309-8a4c-e9b48479c268)

## MVVM의 자세한 역활
### View
* Ativity/Fragment 역활을 한다.
* 사용자의 Action을 받는다.
* ViewModel의 데이터를 반아 UI 갱신한다.

### ViewModel
* View가 요청한 데이터를 Model로 요청한다.
* Model로부터 데이터를 받는다.

### Model
* ViewModel이 요청한 데이터를 반환한다.

## MVVM VS MVC
> MVC를 사용한다면 아래의 문제점이 생긴다
* 앱 동작이 많아질 수록 Activity 자체가 무거워진다.
* View 와 Model 간의 의존성이 높아져 코드가 복잡해진다.
* 규모가 커질수록 유지보수가 어려워진다.