# 1. Project Overview (프로젝트 개요)
- 프로젝트 이름: Fit-Mate
- 프로젝트 설명: 트레이너와 구독자가 1:1로 소통하며 맞춤형 피드백을 제공하는 플랫폼

<br/>
<br/>

# 2. Team Members (팀원 및 팀 소개)
| 박미진 | 윤영서 | 이준우 |
|:------:|:------:|:------:|
| <img src="https://github.com/user-attachments/assets/c1c2b1e3-656d-4712-98ab-a15e91efa2da" alt="박미진" width="150"> | <img src="https://github.com/user-attachments/assets/78ec4937-81bb-4637-975d-631eb3c4601e" alt="윤영서" width="150"> | <img src="https://github.com/user-attachments/assets/78ce1062-80a0-4edb-bf6b-5efac9dd992e" alt="이준우" width="150"> 
| [GitHub](https://github.com/mijinn0) | [GitHub](https://github.com/bbang-2) | [GitHub](https://github.com/) | 

<br/>
<br/>

# 3. Key Features (주요 기능)
- **회원가입**:
  - 회원가입 시 DB에 유저정보가 등록됩니다.

- **로그인**:
  - 사용자 인증 정보를 통해 로그인합니다.

- **내 동아리 일정관리**:
  - 캘린더 UI를 통해 동아리 관련 일정 추가&삭제가 가능합니다.
  - 체크박스를 통해 종료되거나 이미 수행한 일정을 표시할 수 있습니다.

- **동아리 찾기**:
  - 대학 내 동아리를 검색할 수 있습니다.
  - 검색 시 해당 동아리가 업로드한 홍보글이 보여집니다.

- **동아리 홍보**:
  - 홍보글 등록을 통해 동아리를 홍보할 수 있습니다.

- **동아리 만들기**:
  - 새로운 동아리를 만들어 관리할 수 있습니다.

- **동아리 프로필**:
  - 동아리 홍보글에서 동아리 이름(링크)를 클릭하면 해당 동아리 프로필로 이동합니다.
  - 동아리 프로필에서는 동아리 소개, 동아리 활동사진 갤러리, 동아리 홍보글 기록관 등을 볼 수 있습니다.

<br/>
<br/>

# 4. Tasks & Responsibilities (작업 및 역할 분담)
|  |  |  |
|-----------------|-----------------|-----------------|
| 박미진    |  <img src="https://github.com/user-attachments/assets/c1c2b1e3-656d-4712-98ab-a15e91efa2da" alt="박미진" width="100"> | <ul><li>회원가입 / 로그인 / 로그아웃</li><li>이메일 인증</li><li>사용자 정보 수정 및 탈퇴</li><li>트레이너 승인 / 재신청</li><li>뷰테이블 기반 페이지네이션</li><li>프로필 이미지 및 단건 파일 관리</li><li>게시판 댓글  CRUD</li></ul>     |
| 윤영서   |  <img src="https://github.com/user-attachments/assets/78ec4937-81bb-4637-975d-631eb3c4601e" alt="윤영서" width="100">| <ul><li>트레이너 정보 관리</li><li>경력 및 자격증 관리</li><li>체험권 발급 및 상태별 처리</li><li>멀티 파일 업로드 / 삭제</li><li>트레이너 위치 시각화 (카카오맵, 주소 기반 마커 표시)</li><li>1 : 1 게시판 CRUD</li></ul> |
| 이준우   |  <img src="https://github.com/user-attachments/assets/78ce1062-80a0-4edb-bf6b-5efac9dd992e" alt="이준우" width="100">    |<ul><li>쪽지</li><li>쿠폰 발급 및 상태별 처리</li><li>회원 폼 생성 및 조회</li><li>매칭 대기 리스트 처리</li><li>커스텀훅 개발</li><li>매칭 리스트 처리</li><li>구독 결제 처리 (카카오페이 API)</li></ul>  |


<br/>
<br/>

# 5. Technology Stack (기술 스택)

| Category | Stack | Version |
|-----------------|-----------------|-----------------|
| Language    |  Java    | 17    |
| Frameworks    |  Spring Boot    | 3.5.3    |
| Build Tools     |  Gradle    |     |
| Tool     |  intelliJ    |  2025.1   |
| Version Control     |  GitHub    |     |
| Version Control     |  Git    |     |
| Application Server     |  Tomcat    |   10.1.41  |
| Database     |  MySQL    |  8   |
| Libraries     |  Spring Data JPA    |     |
| Libraries     |  Spring Security    |     |
| Libraries     |  Spring Web MVC    |     |
| Libraries     |  Hibernate    |  8.0.0   |
| Libraries     |  Lombok    |     |
| API and JSON Handling     |  Jackson    |  2.19.0   |

<br/>

# 6. Project Structure (프로젝트 구조)
```text
backend/
└── src/
    ├── main/
    │   ├── java/com/bcl/fitmate/
    │   │   ├── common/              # 공통 유틸 클래스 및 상수 정의
    │   │   ├── config/              # 보안 및 메일 환경 설정
    │   │   ├── controller/          # REST API 엔드포인트
    │   │   ├── dto/                 # Request/Response 객체
    │   │   ├── entity/              # 엔티티 클래스
    │   │   ├── exception/           # 예외 처리 및 공통 응답 포맷
    │   │   ├── filter/              # JWT 인증 필터 등 시큐리티 관련 필터
    │   │   ├── provider/            # 인증 관련 토큰 발급/검증 등 프로바이더
    │   │   ├── repository/          # JPA 인터페이스
    │   │   └── service/             # 비즈니스 로직 응답
    │   └── resources/
    │       └── application.properties
    └── test/
        └── java/com/bcl/fitmate/
```

<br/>
<br/>

# 7. Development Workflow (개발 워크플로우)
## 브랜치 전략 (Branch Strategy)
Git-flow 전략을 기반으로 Main, Develop 브랜치와 Feat 브랜치를 운용했습니다.

- Main Branch
  - 배포 가능한 상태의 코드를 유지합니다.
  - 모든 배포는 이 브랜치에서 이루어집니다.

- Develop Branch
  - 개발 단계에서 master 역할을 합니다.
  - 기능 합병은 이 브랜치에서 이루어집니다.
  
- Feat Branch
  - 기능 단위로 독립적인 개발 환경을 위하여 사용합니다.
  - 모든 기능 개발은 이 브랜치에서 이루어집니다.
  - merge 후 각 브랜치를 삭제해 주었습니다.

<br/>
<br/>

# 8. Coding Convention
## 문장 종료
* 문장 마지막에 세미콜론(;) 사용
``` java
System.out.println("Hello Fit-Mate!");
```

<br/>


## 명명 규칙
* 상수 : 영문 대문자 + 스네이크 케이스
``` java
public static final String TOKEN_PREFIX = "Bearer ";
public static final int MAX_TICKET_COUNT = 3;
```
* 변수 & 함수 : 카멜 케이스
``` java
private boolean isLoggedIn;
private String trainerName;
private List<Member> members;
```
* 클래스 & 인터페이스 : 파스칼 케이스
``` java
TrainerService
MemberController
TrainerInfoResponseDto
```

<br/>

## 블록 구문
* 한 줄짜리 블록일 경우라도 {}를 생략하지 않고, 명확히 줄 바꿈 하여 사용
``` java
// good
if(true) {
  return 'hello'
}

// bad
if(true) return 'hello'
```

<br/>

## 패키지 및 디렉토리
* 카멜 케이스를 기본으로 하며, 점(.)으로 구분
``` java
com.bcl.fitmate.backend.controller
com.bcl.fitmate.backend.service
com.bcl.fitmate.backend.repository
```

<br/>

## 파일 네이밍
* 클래스명과 동일한 이름으로 .java 확장자 사용
```
TrainerService.java
MemberController.java
```

<br/>
<br/>

# 9. 커밋 컨벤션
## 기본 구조
```
type : subject
```

<br/>

## type 종류

| 타입 | 설명 |
|-----------------|-----------------|
| feat    |  새로운 기능 추가    |
| fix    |  버그 수정    |
| refactor     |  리팩토링    |
| style     |  코드 스타일 변경    |
| docs     |  문서 수정    |
| test     |  테스트 코드 추가 또는 수정    |
| chore     |  빌드 / 설정 관련 작업, 패키지 매니저 설정 등    |
| design     |  프론트엔드 UI 작업 또는 스타일링 수정    |
| ci     |  CI / CD 관련 설정 작업    |

<br/>


## 커밋 예시
```
feat: 회원가입 API 구현

fix: 로그인시 비밀번호 검증 오류 수정

refactor: 게시판 조회 로직 리팩토링

docs: README에 API 명세 추가

style: 코드 포맷팅 및 들여쓰기 수정

test: 댓글 서비스 단위 테스트 추가

chore: ESLint 설정 및 Prettier 적용

design: 반응형 네비게이션 바 구현

ci: GitHub Actions 배포 파이프라인 설정
```