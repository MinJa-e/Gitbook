# 간단메모

* KotlinPracticeApplicationKt has been compiled by a more recent version of the Java Runtime (class file version 61.0), this version of the Java Runtime only recognizes class file versions up to 52.0과 같은 에러발생하면 프로젝트 설정에서 자바 버전을 바꿔주면됨
*   build.gradle의 dependency에 아래 의존성이 없으면 localhost:8080으로 실행해도 안 뜸

    ```
    implementation("org.springframework.boot:spring-boot-starter-web")
    ```
* 스프링은 기본적으로 resources/static/index.html을 기본 시작파일로 바라보며, 다른 경로를 설정하려면 별도의 코딩이 필요하다 ( 참고 : [https://bottom-to-top.tistory.com/38](https://bottom-to-top.tistory.com/38) )
* 스프링 공식 문서 [http://docs.spring.io/](http://docs.spring.io/)
