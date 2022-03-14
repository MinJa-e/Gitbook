# @Controller와 @RestController 차이(+@ResponseBody)

개발/스프링

#### \[ Spring ] @Controller와 @RestController 차이(+@ResponseBody)

_민자이 ( ja-e )_ 2022. 2. 23. 21:22

#### **@Controller란?**

> \- 주로 view(시각적으로 보이는 페이지 결과)를 반환할 때 사용\
> \- @Component가 구체화된 형태이며, 해당 클래스는 빈(Bean)객체로 등록\
> \- 하위 메소드에 @ResponseBody를 같이 쓰면, 리턴 값을 JSON 형태의 객체 데이터로 받을 수 있음

#### **@Restcontroller란?**

> \- @Controller에 @ResponsBody가 결합된 역할을 함으로써, 객체 데이터를 JSON으로 반환할 때 사용\
> \- 하위 메소드들에 @ResponseBody를 자동으로 추가\
> ( @Controller의 하위 메소드에 일일이 @ResponseBody를 추가하는 것보다 효율적인 작업 가능 )

#### **@ResponseBody란?**

> \- @Controller의 하위 메소드에 사용함으로써, 반환 값을 JSON 형태의 객체 데이터로 받을 수 있음
