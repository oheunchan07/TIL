# View Binding

## View Binding이란?
>안드로이드 아키텍쳐중 하나로 뷰와 상호작용하는 코드를 쉽게 짤 수 있게 해준다    
>한마디로 findViewById()를 대신해준다

## View Binding 사용법
>build.gradle에 아래 코드를 추가해준다
```
android {
    buildFeatures {
        viewBinding true
    }
}
```

### Activity
```
binding = ActivityMainBinding.inflate(getLayoutInflater());
setContentView(binding.getRoot());
```