# springboot-study
Learning Spring Boot 3 and Java Backend Development

# Spring Boot Study

『코딩 자율학습 스프링 부트 3 자바 백엔드 개발 입문』을 기반으로 Spring Boot와 Java 백엔드 개발을 학습하고 정리하는 저장소입니다.

## 학습 환경

- Java 17
- Spring Boot 3
- Gradle
- Mustache

## 학습 내용

### Chapter 01. 스프링 부트 시작하기

- Spring Boot의 개념과 특징
- JDK 및 개발 환경 설정
- Spring Boot 프로젝트 구조
- 클라이언트-서버 구조와 HTTP 요청·응답
- 정적 웹 페이지의 동작 원리

### Chapter 02. MVC 패턴 이해와 실습

- 뷰 템플릿과 Mustache
- MVC(Model-View-Controller) 패턴
- `@Controller`와 `@GetMapping`을 이용한 URL 매핑
- `Model`을 통한 데이터 전달
- MVC 패턴의 실행 흐름
- Header/Footer 레이아웃 구성

## 핵심 개념

| 개념 | 설명 |
|---|---|
| Spring Boot | 자바 웹 애플리케이션 개발을 간소화하는 프레임워크 |
| MVC | Model, View, Controller의 역할을 분리하는 설계 패턴 |
| Controller | 클라이언트 요청을 처리하고 뷰를 결정 |
| Model | 뷰에 필요한 데이터 전달 |
| View | 사용자에게 보여줄 화면 생성 |
| Mustache | 동적 HTML 생성을 위한 뷰 템플릿 엔진 |

## 학습 자료

- 교재: 『코딩 자율학습 스프링 부트 3 자바 백엔드 개발 입문』
- [Spring Boot 공식 문서](https://docs.spring.io/spring-boot/index.html)

## 학습 기록

| Chapter | 주제 | 상태 |
|---|---|---|
| 01 | 스프링 부트 시작하기 | 학습 내용 정리 |
| 02 | MVC 패턴 이해와 실습 | 학습 내용 정리 |


### Chapter 03. 게시판 만들고 새 글 작성하기: Create

- HTML Form을 활용한 사용자 입력 데이터 전송
- DTO(Data Transfer Object)를 통한 데이터 전달
- JPA와 Entity를 활용한 객체-데이터베이스 매핑
- Repository의 `save()`를 이용한 데이터 저장
- `@Autowired`를 활용한 의존성 주입(DI)
- H2 Database 및 SQL을 활용한 데이터 확인

**데이터 생성 흐름**

```text
Form → Controller → DTO → Entity → Repository → DB
```

### Chapter 04. 롬복과 리팩터링

- Lombok을 활용한 반복 코드 최소화
- DTO 및 Entity 리팩터링
- 생성자와 `toString()` 메서드 자동 생성
- `@Slf4j`를 활용한 로깅

| 어노테이션 | 역할 |
|---|---|
| `@AllArgsConstructor` | 전체 필드 생성자 생성 |
| `@NoArgsConstructor` | 기본 생성자 생성 |
| `@ToString` | 객체의 문자열 표현 생성 |
| `@Slf4j` | 로그 객체 생성 |

### Chapter 05. 게시글 읽기: Read

- `@PathVariable`을 활용한 URL 경로 변수 추출
- `findById()`를 이용한 단일 데이터 조회
- `findAll()`을 이용한 전체 데이터 조회
- Model을 통한 조회 데이터 전달
- Mustache를 활용한 게시글 및 목록 출력

**데이터 조회 흐름**

```text
Client → Controller → Repository → DB
DB → Repository → Controller → Model → View → Client
```

### Create와 Read 비교

| 구분 | Create | Read |
|---|---|---|
| 기능 | 데이터 생성 | 데이터 조회 |
| HTTP Method | POST | GET |
| JPA 메서드 | `save()` | `findById()`, `findAll()` |
| SQL | INSERT | SELECT |
