# Fragment

## Fragment란?
>화면이 넓어지면서 액티비티 하나로 이벤트 처리하기에는 너무 복잡하고 코드가 길어져서
>나온 대안이 View클래스지만 View클래스는 오직 화면 출력만을 위해 설계된 클래스여서 액티비티의 생명주기를 이용할 수 없어 나온 클래스가 Frangment이다

## Fragment 특징
* 독립적일 수 없다(무조건 액티비티 혹은 Fragment에게 종속되어야 한다)
* 자체적인 생명주기를 가진다
* 재사용 가능하다
* 액티비티 내에서 추가,삭제,교체 등이 가능하다

## FragmentManager
![image](https://github.com/oheunchan07/TIL/assets/131967057/112546f9-83a7-4d4b-89f9-29c5d6782a68)
>FragmentManager는 Fragment를 관리하는 클래스이다  
>이 클래스를 통해 액티비티와 Fragment가 상호작용 할 수 있다

## FragmentTransaction
>FragmentTransaction은 Fragment를 추가,삭제,교체 등에 작업을 한다  
>위에 것 말고도 백스텍 관리, Fragment 전환 시의 애니메이션 설정을 해준다

## Fragment Lifecycle
![image](https://github.com/oheunchan07/TIL/assets/131967057/898d6be5-cf43-4373-b75d-bbd202d0c889)

### onAttach
* Fragment가 액티비티에 포함되는 순간 호출 된다

### onCreate
* Fragment가 호출 되었지만 Fragment View에는 포함되지 않은 상태이다
* View관련 상태 세팅을 여기서 진행하면 안정성을 보장받지 못한다

### onCreateView
* Fragment UI를 위하여 호출된다
* Fragment View 생명주기가 생성된다

### onViewCreated
* onCreateView를 통해 객체를 전달 받는다
* 여기서 View의 초기 세팅을 하면 안전하다

### onResume
* Fragment와 상호작용 가능한 상태이다

### onDestroyView
* Fragment View의 생명주기를 없앤다
* 백스터 처리를 했다면 onDestroy로 가지 않는다

### onDetach
* Fragment가 액티비티에서 완전히 제거되었을 때 호출된다