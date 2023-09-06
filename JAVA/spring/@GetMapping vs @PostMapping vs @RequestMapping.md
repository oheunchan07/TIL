# @GetMapping VS @PostMapping VS @RequestMapping

## @GetMapping
* URL에 변수를 포함시켜 요청
* URL에 데이터가 노출되어 보안 취약
* 캐싱O

## @PostMapping
* URL에 변수를 포함하지 않고 요청
* URL에 데이터가 노출 되지 않기 떄문에 보안 굳
* 캐싱X
### 캐싱: 똑같은 요청을 할때 빠르게 전급하기 위해 레지스터에 데이터를 저장하는 것

## @RequestMapping을 안쓰는 이유
* URL을 중복 사용할 수 없다
* @GetMapping과@PostMapping에 코드 간소화
* @RequestMapping의 코드 길이가 길어져 무슨 역할을 하는지 한눈에 파악 불가
