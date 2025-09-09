# CodingStudy 프로젝트 목차
1. [프로젝트 소개](#프로젝트-소개)
2. [시스템 아키텍처](#시스템-아키텍처)
3. [기술 스택](#기술-스택)
4. [프로젝트 구조](#프로젝트-구조)
5. [기능 소개](#기능-소개)
6. [팀 소개](#팀-소개)

## 프로젝트 소개
<div align="center">
<img width="300" height="330" alt="logo" src="https://github.com/user-attachments/assets/5bfc05e5-17da-49e0-bd79-d389154e7a2c"/>
</div>

- **프로젝트 이름**: Coding Study
- **목적**: 사용자 간 정보 공유와 소통을 위한 웹 기반 커뮤니티 서비스 제공
- **특징**:
  - Vue.js 기반의 반응형 UI
  - Spring Boot 기반 REST API 서버
  - MySQL을 통한 안정적인 데이터 관리
  - JWT 기반 사용자 인증 및 소셜 로그인 지원
  - 게시글, 댓글, 좋아요 등 기본 커뮤니티 기능 제공

- Repository : <a href="https://github.com/CodingMate24/FrontEnd">FrontEnd</a>
/ <a href="https://github.com/CodingMate24/BackEnd">BackEnd</a>
<br/>

## 시스템 아키텍처


### **화면정의서(피그마)**
<br/>
- 링크 : <a href="https://www.figma.com/design/eENJw2mjaQki965WLZnx6p/Codingmate?m=auto&t=OXfojBZl9ezKh3rD-6">화면정의서</a>
<img width="940" height="763" alt="image" src="https://github.com/user-attachments/assets/3b5ac8e1-da7e-433a-8d0f-d9b56fec57eb" />

## 기술 스택

| 구분        | 기술명                                          |
|-----------|---------------------------------------------|
| 프론트엔드    | Vue.js 3, Vue Router 4, Bootstrap 5, Vite |
| 백엔드      | Java 17, Spring Boot 3.2.3, Spring Security, Spring Data JPA, MyBatis, Redis, ModelMapper |
| 데이터베이스   | MySQL 8.2.0                                 |
| 인증/보안    | JWT, OAuth 2.0 (Google/Naver/Kakao)         |
| 메일 서비스   | Spring Boot Mail                           |
| 개발 툴     | IntelliJ, VSCode, GitHub                    |


# 개발 환경 아키텍처
  
```
┌──────────────────────────────────────────────┐
│                  Client                      │
│  ────────────────────────────────────────    │
│ │  Browser                                │  │
│ │ ┌─────────────────────────────────┐     │  │
│ │ │  Frontend (Vue.js + Vite)       │     │  │
│ │ │  - Vue 3, Vue Router            │     │  │
│ │ │  - Bootstrap, JS, CSS3          │     │  │
│ │ └─────────────────────────────────┘     │  │
│  ────────────────────────────────────────    │
└─────────────────────┬────────────────────────┘
                      │  HTTP (REST API)
                      ▼
┌──────────────────────────────────────────────┐
│                Backend (Spring Boot)         │
│ ───────────────────────────────────────────  │
││  Application Layer                        │ │
││ ┌─────────────────────────────────────┐   │ │
││ │ Controllers (REST API)              │   │ │
││ │ Security (JWT, Spring Security)     │   │ │
││ │ Validation                          │   │ │
││ │ ModelMapper                         │   │ │
││ │ Email Service                       │   │ │
││ │ Actuator (Monitoring)               │   │ │
││ │ Devtools (Development only)         │   │ │
││ └─────────────────────────────────────┘   │ │
││  Persistence Layer                        │ │
││ ┌─────────────────────────────────────┐   │ │
││ │ JPA (Hibernate)                     │   │ │
││ │ MyBatis (SQL Mapper)                │   │ │
││ │ Spring Data Redis                   │   │ │
││ └─────────────────────────────────────┘   │ │
││  Log4jdbc (SQL logging)                   │ │
│ ───────────────────────────────────────────  │
││  Dependency Management                    │ │
││  - Spring Dependency Management Plugin    │ │
│ ───────────────────────────────────────────  │
││  Test/Annotation Processing               │ │
││  - JUnit, Spring Test, Security Test      │ │
││  - Lombok                                 │ │
│ ───────────────────────────────────────────  │
└─────────────┬────────────────────────────────┘
              │
              ▼
       ┌────────────┐
       │   MySQL    │
       │ Database   │
       └────────────┘
              │
              ▼
       ┌────────────┐
       │   Redis    │
       │  (Cache)   │
       └────────────┘
```


## 아키텍쳐 설명

**Frontend**  
- Vue.js 기반 SPA  
- Vite로 빌드  
- Bootstrap, JS, CSS3 사용  
- Vue Router로 라우팅  
- 브라우저에서 동작

**Backend**  
- Spring Boot 3.2.3, Java 17  
- REST API (컨트롤러)  
- JWT 인증/인가, Spring Security  
- Validation, ModelMapper  
- 이메일 서비스, 모니터링(Actuator), 개발 편의(Devtools)  
- JPA(Hibernate), MyBatis  
- MySQL 지원 (JDBC 클라이언트 포함)  
- SQL 로그(Log4jdbc), Redis 캐시  
- 테스트/어노테이션 처리(Lombok, JUnit 등)  
- 의존성 관리(Spring Dependency Management)

**DB/Cache**  
- MySQL (비즈니스/사용자 데이터 저장)  
- Redis (캐싱, 세션 등)


<br/>

## 프로젝트 구조

- Frontend

```plaintext
project/
├── public/
│   └── favicon.ico          # 아이콘 파일
├── src/
│   ├── assets/              # 이미지, 폰트 등 정적 파일
│   ├── components/          # 재사용 가능한 UI 컴포넌트
│   ├── layout/              # 페이지 Header,Footer 레이아웃 파일
│   ├── pages/               # 각 페이지별 컴포넌트
│   ├── router/              # 각 페이지별 라우터 설정 파일
│   ├── static/              # 공통 Util, Transaction js 파일
│   ├── App.vue              # 메인 애플리케이션 컴포넌트
│   ├── main.js              # 전역 js 파일
│   └── index.css            # 전역 css 파일
├── .gitignore               # Git 무시 파일 목록
└── README.md                # 프로젝트 개요 및 사용법
```

<br/>
- Backend

```plaintext
project/
├── gradle/wrapper/
│   ├── gradle-wrapper.jar                 # Gradle Wrapper jar 파일
│   └── gradle-wrapper.properties          # Gradle Wrapper 설정 파일
├── src/
│   ├── main/
│   |   ├── java/com/prj/codingstudy       # 메인 소스 폴더
│   |   |   ├── config/                    # 공통 설정 파일 폴더
│   |   |   ├── core/                      # 주요 기능 폴더
│   |   |   ├── util/                      # 공통 유틸 파일 폴더
│   |   |   └── CodingStudyApplication.java  # 프로그램 실행 파일
│   |   ├── resource/                # 리소스 설정 폴더
│   |   |   ├── mapper/              # xml mapper 쿼리 폴더
│   |   |   ├── application.yml                # application.yml
│   |   |   └── log4jdbc.log4j2.properties     # log4j 설정 파일  
│   └── test/                # 테스트 소스 폴더
├── build.gradle             # build.gradle 라이브러리 레파지토리 설정 파일
├── gradlew                  # Gradlew
├── gradlew.bat              # Gradlew Bat 파일
├── .gitignore               # Git 무시 파일 목록
└── README.md                # 프로젝트 개요 및 사용법
```

<br/>
- ERD
  <img width="100%" alt="erd" src="https://github.com/user-attachments/assets/b31ad6d1-a6c2-4991-afaa-da36ed9f9b8b" />

<br/>

## 기능 소개

- **사용자 인증**:
  - 이메일/비밀번호 회원가입 및 로그인
  - Google, Naver, Kakao 소셜 로그인 지원
  - 비밀번호 찾기 및 이메일 인증 기능 제공
  - JWT 기반 인증 토큰 발급 및 권한 관리

- **게시글 관리**:
  - 게시글 작성, 수정, 삭제 기능
  - 이미지 첨부 기능
  - 게시글 상세 페이지 제공 (내용, 작성자, 좋아요, 댓글 표시)

- **댓글 관리**:
  - 게시글에 댓글 작성/삭제 가능
  - 실시간 댓글 반영

- **좋아요 기능**:
  - 게시글 좋아요/취소 기능
  - 사용자별 좋아요 목록 확인 가능

- **검색**:
  - 키워드 검색 기능 제공
  - 검색 결과 필터링 기능

- **마이페이지**:
  - 사용자 프로필 확인/수정
  - 내가 작성한 게시글 및 좋아요한 게시글 목록 확인

<br/>
<br/>

## 팀 소개
|  |  |  |
|-----------------|-----------------|-----------------|
| 이승호   |  <img src="https://github.com/user-attachments/assets/c1c2b1e3-656d-4712-98ab-a15e91efa2da" alt="이승호" width="100"> | <ul><li>프로젝트 계획 및 관리</li><li>메인 피드/검색 페이지 개발</li><li>기타 개발</li></ul>     |
| 최윥정   |  <img src="https://github.com/user-attachments/assets/78ec4937-81bb-4637-975d-631eb3c4601e" alt="최윤정" width="100">| <ul><li>프로젝트 계획 및 관리</li><li>로그인/회원가입 페이지 개발</li><li>기타 개발</li></ul> |
