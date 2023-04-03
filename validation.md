# Validate
Spring Boot @Validated 에 대해 알아보자


## Validation 이란 무엇인가?
예를 들어 회원 가입시에는 
이름, 휴대폰번호, 이메일 등의 몇몇 기본 양식이 존재한다.
이러한 데이터들의 유효성검증을 하기위해 사용되는 것이라 보면 된다.

> ### :exclamation: <strong> @Valid, @Validated 차이</strong>  
> @Valid는 JAVA에서 지원해주는 annotation 이고 @Validated는 Spring에서 지원해주는 annotation 입니다.  
> @Validated가 @Valid의 기능을 포함하고 있다.

### :hammer: Spring Boot Validation 적용
1. Spring Boot 2.3 version 이상부터는 spring-boot-starter-web 의존성 내부에 있던 validation이 사라졌기 때문에, 의존성을 따로 추가.
- Gradle 의존성 추가.
```
implementation group: 'org.springframework.boot', name: 'spring-boot-starter-validation', version: '2.5.6'
```
- Maven 의존성추가
```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
    <version>2.5.6</version>
</dependency>
```
- 기본 조건
  - 휴대폰 번호의 경우 숫자만 입력
  - 이메일이 정상적으로 입력되어 있는지 체크.
  - 이름이 공백일수는 없다.

