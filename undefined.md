# 간단메모

* KotlinPracticeApplicationKt has been compiled by a more recent version of the Java Runtime (class file version 61.0), this version of the Java Runtime only recognizes class file versions up to 52.0과 같은 에러발생하면 프로젝트 설정에서 자바 버전을 바꿔주면됨
*   build.gradle의 dependency에 아래 의존성이 없으면 localhost:8080으로 실행해도 안 뜸

    ```
    implementation("org.springframework.boot:spring-boot-starter-web")
    ```
