# Acticity Lifecycle(생명주기)

## Activity Lifecycle이란?
>안드로이드 앱이 생성되고 종료되기 까지의 과정

![image](https://github.com/oheunchan07/TIL/assets/131967057/f227ed0f-89b3-4649-9ef7-ec9fae9096e8)

## Lifecycle 메서드
|메서드|설명|
|---|------------------|
|onCreate()|액티비티 생성 시 가장 빠르게 실행|
|onStart()|화면의 표시|
|onResume()|일시 정지 되었다가 돌아옴|
|onPause()|방해되는 이벤트 실행시 일시정지|
|onStop()|액티비티가 사용자에게 완전히 보이지 않음|
|onRestart()|다른 액티비티나 홈 화면에서 돌아옴|
|onDestroy()|앱을 종료|

## LIfecycle 메서드 특징
### onCreate
* 액티비티 생성 시 가장 먼저 호출한다
* 생명 주기동안 한번만 호출한다
* 화면 레이아웃 정의, 뷰 설정, 데이터 바인딩 등을 여기서 한다 

### onStart
* 화면에 표시되기 직전에 호출
* 화면에 진입 할 때 마다 실행되야 할 코드들을 쓴다

### onResume
* 일시 정지 됐다가 돌아오는 경우 호출한다
* 액티비티가 돌아오게 되었을 때의 실행해야 코드들을 쓴다
* onResume에서 초기화 작업을 했다면 onPause에서 리소스를 해제 하거나 종료해야 한다

### onPause
* 방해되는 이벤트 발생시 호출된다
* 액티비티가 사용자 눈 밖으로 나간 상태이다
* 다른 액티비티가 호출 되기 전에 실행되야 하기 때문에 가벼워야 한다
* 영구적이 데이터는 여기에다가 저장한다

### onStop
* 액티비티가 다른 액티비티때문에 완전히 가려진 상태이다
* 이 상태에서 액티비티 호출 시 onStart로 돌아간다
* 무거운 작업은 여기서 해야 된다

### onDestroy
* 액티비가 완전히 종료되었을 때 호출되는 메소드이다
* 메모리 부족이 되면 스킵 될 수 있다

### onRestart
* onStop이 호출된 후에 다시 돌아올 때 호출되는 메소드












