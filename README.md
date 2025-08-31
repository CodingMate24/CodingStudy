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

- 프로젝트 이름: Coding Study
- 프로젝트 설명: 코딩 공부를 위한 간단한 커뮤니티 사이트

- Repository : <a href="https://github.com/CodingMate24/FrontEnd">FrontEnd</a>
/ <a href="https://github.com/CodingMate24/BackEnd">BackEnd</a>
<br/>

## 시스템 아키텍처


### **화면정의서(피그마)**
<br/>
- 링크 : <a href="https://www.figma.com/design/eENJw2mjaQki965WLZnx6p/Codingmate?m=auto&t=OXfojBZl9ezKh3rD-6">화면정의서</a>
<img width="940" height="763" alt="image" src="https://github.com/user-attachments/assets/3b5ac8e1-da7e-433a-8d0f-d9b56fec57eb" />

## 기술 스택

## **Language**
|  |  |
|-----------------|-----------------|
| CSS3    |   <img src="https://github.com/user-attachments/assets/c531b03d-55a3-40bf-9195-9ff8c4688f13" alt="CSS3" width="100">|
| Javascript    |  <img src="https://github.com/user-attachments/assets/4a7d7074-8c71-48b4-8652-7431477669d1" alt="Javascript" width="100"> | 

<br/>

## **Frotend**
|  |  |  |
|-----------------|-----------------|-----------------|
| Vue.js    |  <img alt="vue" src="https://github.com/user-attachments/assets/c1b35bfc-7eca-4bb9-ba26-fa4beb2047e4" width="100"> |    |

<br/>

## **Backend/Database**
|  |  |  |
|-----------------|-----------------|-----------------|
| Java    | <img width="172" height="294" alt="java" src="https://github.com/user-attachments/assets/300fdd06-128c-4965-982e-53b659c6ab2a" /> | 17.0    |
| SpringBoot    | <img width="100" alt="Springboot" src="https://github.com/user-attachments/assets/aa01b481-34da-4e7a-a051-6a703d8fd944" />    | 3.2.3    |
| MySQL    | <img width="100" alt="mysql" src="https://github.com/user-attachments/assets/ac01f19a-6ded-4262-a782-6408dd2af9d7" />   | 8.5    |

<br/>


## **Cooperation**
|  |  |
|-----------------|-----------------|
| Git    |  <img src="https://github.com/user-attachments/assets/483abc38-ed4d-487c-b43a-3963b33430e6" alt="git" width="100">    |
| Figma    |  <img src="https://github.com/user-attachments/assets/f8e654ac-69ad-4d1d-97c2-9e877a4b7b61" alt="git kraken" width="100">    |

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

- **회원가입**:
  - 회원가입 시 DB에 유저정보가 등록됩니다.

- **로그인**:
  - 사용자 인증 정보를 통해 로그인합니다.

- **패스워드 재설정**:
  - 이메일 인증을 통해 패스워드를 재설정 합니다.

- **메인 피드**:
  - 검색 시 해당 동아리가 업로드한 홍보글이 보여집니다.

- **검색 페이지**:
  - 검색 시 해당 동아리가 업로드한 홍보글이 보여집니다.

- **프로필**:
  - 새로운 동아리를 만들어 관리할 수 있습니다.

- **글 작성/ 수정**:
  - 글 등록을 할 수 있습니다.
  - 동아리 프로필에서는 동아리 소개, 동아리 활동사진 갤러리, 동아리 홍보글 기록관 등을 볼 수 있습니다.

<br/>
<br/>

## 팀 소개
|  |  |  |
|-----------------|-----------------|-----------------|
| 이승호   |  <img src="https://github.com/user-attachments/assets/c1c2b1e3-656d-4712-98ab-a15e91efa2da" alt="이승호" width="100"> | <ul><li>프로젝트 계획 및 관리</li><li>메인 피드/검색 페이지 개발</li><li>기타 개발</li></ul>     |
| 최윥정   |  <img src="https://github.com/user-attachments/assets/78ec4937-81bb-4637-975d-631eb3c4601e" alt="최윤정" width="100">| <ul><li>프로젝트 계획 및 관리</li><li>로그인/회원가입 페이지 개발</li><li>기타 개발</li></ul> |
