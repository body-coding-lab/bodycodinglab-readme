# 1. Project Overview (프로젝트 개요)
- **프로젝트 이름**: Fit-Mate
- **프로젝트 설명**: 트레이너와 구독자가 1:1로 소통하며 맞춤형 피드백을 제공하는 플랫폼

<br/>
<br/>

# 2. Team Members (팀원 및 역할 분담)
<table>
  <tr>
    <th>박미진</th>
    <th>윤영서</th>
    <th>이준우</th>
  </tr>
  <tr align="center">
    <td><img src="https://em-content.zobj.net/source/microsoft-3D-fluent/406/ghost_1f47b.png" width="150"></td>
    <td><img src="https://avatars.githubusercontent.com/u/201715606?v=4" width="150"></td>
    <td><img src="https://github.com/user-attachments/assets/78ce1062-80a0-4edb-bf6b-5efac9dd992e" width="150"></td>
  </tr>
  <tr align="center">
    <td><a href="https://github.com/mijinn0">GitHub</a></td>
    <td><a href="https://github.com/bbang-2">GitHub</a></td>
    <td><a href="https://github.com/">GitHub</a></td>
  </tr>
  <tr>
    <td align="left" width="250px">
      <ul>
        <li>회원가입 / 로그인 / 로그아웃</li>
        <li>이메일 인증</li>
        <li>사용자 정보 수정 및 탈퇴</li>
        <li>트레이너 승인 / 재신청</li>
        <li>뷰테이블 기반 페이지네이션</li>
        <li>프로필 이미지 및 단건 파일 관리</li>
        <li>게시판 댓글 CRUD</li>
      </ul>
    </td>
    <td align="left" width="250px">
      <ul>
        <li>트레이너 정보 관리</li>
        <li>경력 및 자격증 관리</li>
        <li>체험권 발급 및 상태별 처리</li>
        <li>멀티 파일 업로드 / 삭제</li>
        <li>트레이너 위치 시각화</li>
        <li>1 : 1 게시판 CRUD</li>
      </ul>
    </td>
    <td align="left" width="250px">
      <ul>
        <li>쪽지</li>
        <li>쿠폰 발급 및 상태별 처리</li>
        <li>회원 폼 생성 및 조회</li>
        <li>매칭 대기 리스트 처리</li>
        <li>매칭 리스트 처리</li>
        <li>구독 결제 처리 (카카오페이 API)</li>
      </ul>
    </td>
  </tr>
</table>

<br/>
<br/>

# 3. Key Features (주요 기능)
| 기능              | 설명             |
|:---------------------|:---------------------|
| **회원가입** | • 회원 정보 입력 데이터의 유효성을 검증하고 프로필 이미지를 업로드할 수 있습니다.<br/>• 가입이 완료되면 사용자 정보가 DB에 저장됩니다.           |
| **로그인** | • 아이디와 비밀번호를 검증한 후, JWT 토큰을 발급합니다.<br/>• 상황에 따라 다른 응답을 반환해 UI 로직을 구분합니다. |
| **비밀번호 재설정** | • 이메일 인증을 통해 본인 여부를 확인한 후, 비밀번호를 재설정할 수 있습니다.<br/>• 토큰 유효 시간을 적용해 보안을 강화했습니다. |
| **이름 · 근무지 기반 트레이너 검색** | • 사용자가 입력한 키워드로 트레이너를 검색합니다.<br/>• 검색 결과는 목록과 지도 마커로 함께 표시됩니다. |
| **멀티 파일 관리** | • 트레이너 상세 정보에 이미지 파일을 다중 업로드할 수 있습니다.<br/>• 업로드된 이미지는 개별 이미지 삭제 및 조회가 가능합니다. |
| **트레이너 정보 · 경력 · 자격증 관리** | • 트레이너는 자신의 프로필, 경력, 자격증 정보를 등록하고 수정할 수 있습니다.<br/>• 관리자는 트레이너 정보 목록을 확인하고 검토할 수 있습니다. |
| **구독 결제 및 매칭 신청** | • 사용자가 구독 결제를 통해 트레이너에게 매칭을 신청할 수 있습니다.<br/>• 매칭이 성사되면 1:1 게시판이 자동 생성됩니다. |
| **1:1 게시판 (트레이너 - 회원 간)** | • 매칭된 회원과 트레이너는 비공개 게시판을 통해 맞춤형 피드백을 주고받을 수 있습니다.<br/>• 게시판 글 작성, 이미지 첨부, 수정 및 삭제가 가능합니다. |
| **쪽지** | • 회원과 트레이너가 1:1로 쪽지를 주고받을 수 있습니다.<br/>• 읽음 여부와 발신 · 수신 이력을 관리합니다. |
| **체험권 발급 및 상태 관리** | • 회원은 트레이너에게 체험권을 신청할 수 있고, 트레이너는 이를 승인, 거절, 사용 처리할 수 있습니다.<br/>• 사용자는 상태별 체험권 목록 조회가 가능합니다. |
| **쿠폰 발급 및 상태 관리** | • 체험권이 사용 처리되면 자동으로 쿠폰이 발급됩니다.<br/>• 트레이너는 이를 사용 처리할 수 있고, 사용자는 상태별 쿠폰 목록 조회가 가능합니다. |

<br/>
<br/>

# 4. Technology Stack (기술 스택)

| Category              | Stack             | Version |
|:---------------------:|:-----------------:|:-----------------:|
| Language              | `Java`            | 17 |
| Frameworks            | `Spring Boot`     | 3.5.3 |
| Build Tools           | `Gradle`          | - |
| Tool                  | `intelliJ`        | 2025.1 |
| Version Control       | `GitHub`          | - |
| Version Control       | `Git`             | - |
| Application Server    | `Tomcat`          | 10.1.41 |
| Database              | `MySQL`           | 8 |
| Libraries             | `Spring Data JPA` | - |
| Libraries             | `Spring Security` | - |
| Libraries             | `Spring Web MVC`  | - |
| Libraries             | `Hibernate`       | 8.0.0 |
| Libraries             | `Lombok`          | - |
| API and JSON Handling | `Jackson`         | 2.19.0 |

<br/>
<br/>

# 5. Project Structure (프로젝트 구조)
```text
backend/
└── src/
    ├── main/
    │   ├── java/com/bcl/fitmate/
    │   │   ├── common/              # 공통 유틸 클래스 및 상수 정의
    │   │   ├── config/              # 보안 및 메일 설정
    │   │   ├── controller/          # REST API 요청 처리 컨트롤러
    │   │   ├── dto/                 # Request/Response 객체
    │   │   ├── entity/              # 엔티티 클래스
    │   │   ├── exception/           # 예외 처리 및 공통 응답 포맷
    │   │   ├── filter/              # JWT 토큰 인증 필터 보안 필터
    │   │   ├── provider/            # 인증 관련 토큰 발급/검증 모듈
    │   │   ├── repository/          # JPA 인터페이스
    │   │   └── service/             # 비즈니스 로직 구현
    │   └── resources/
    │       └── application.properties
    └── test/
        └── java/com/bcl/fitmate/
```

<br/>
<br/>

# 6. Development Workflow (개발 워크플로우)
## 브랜치 전략 (Branch Strategy)
Git-flow 전략을 기반으로 main, develop 브랜치와 작업 브랜치를 운용했습니다.

- main 브랜치
  - 배포 가능한 상태의 코드를 유지합니다.
  - 모든 배포는 이 브랜치에서 이루어집니다.

- develop 브랜치
  - 개발 단계의 통합 브랜치입니다.
  - 각 작업 브랜치의 기능이 이 브랜치에서 병합됩니다.
  
- 작업 브랜치
  - 기능 단위로 독립적인 개발 환경을 위해 생성합니다.
  - 모든 기능 개발은 이 브랜치에서 이루어집니다.
  - 기능이 완료되면 `develop` 에 후 해당 브랜치를 삭제합니다.

<br/>

## 작업 브랜치 네이밍 규칙 (Feature Branch Naming Convention)
작업 브랜치는 다음과 같은 형식으로 생성합니다.
- 소문자 사용
- 단어는 `-` (하이픈)으로 구분
- 작업 내용은 구체적으로 작성

<br/>

### ✅ 작업 브랜치 Prefix 종류
| Prefix      | 설명                         | 예시 |
|:------------|:----------------------------|:-----------------|
| `feature/`  | 새로운 기능 추가              | `feature/login-api` |
| `fix/`      | 버그 수정                    | `fix/signup-validation-error` |
| `refactor/` | 코드 리팩토링 (기능 변경 없음) | `refactor/user-service` |
| `hotfix/`   | 운영 중 긴급 수정             | `hotfix/token-expiration-error` |
| `docs/`     | 문서 작업 및 README 수정      | `docs/readme-update` |
| `test/`     | 테스트 코드 추가 또는 수정    | `test/user-service-unit-test` |
| `chore/`    | 기타 설정 파일 수정 등        | `chore/package-update` |
| `design/`   | UI · UX 관련 작업 (CSS 포함) | `design/header-layout-update` |

<br/>
<br/>

# 7. 코딩 컨벤션 (Coding Convention)
## 문장 종료
- 문장 마지막에 세미콜론(;) 사용
``` java
System.out.println("Hello Fit-Mate!");
```

<br/>

## 명명 규칙
- **상수**: 영문 대문자 + 스네이크 케이스
``` java
public static final String TOKEN_PREFIX = "Bearer ";
public static final int MAX_TICKET_COUNT = 3;
```

- **변수 & 함수**: 카멜 케이스
``` java
private boolean isLoggedIn;
private String trainerName;
private List<Member> members;
```

- **클래스 & 인터페이스**: 파스칼 케이스
```
TrainerService
MemberController
TrainerInfoResponseDto
```

<br/>

## 블록 구문
- 한 줄짜리 블록일 경우라도 중괄호({ })를 생략하지 않고, 명확히 줄 바꿈 하여 사용
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
- 카멜 케이스를 기본으로 하며, 점(.)으로 구분
```
com.bcl.fitmate.backend.controller
com.bcl.fitmate.backend.service
com.bcl.fitmate.backend.repository
```

<br/>

## 파일 네이밍
- 클래스명과 동일한 이름으로 `.java` 확장자 사용
```
TrainerService.java
MemberController.java
```

<br/>
<br/>

# 8. 커밋 메시지 컨벤션 (Commit Message Convention)
## 기본 구조
```
type : subject
```

<br/>

## 커밋 타입 종류

| 타입       | 설명 |
|:-----------|:-----------------|
| `feat`     | 새로운 기능 추가 |
| `fix`      | 버그 수정 |
| `refactor` | 리팩토링 |
| `style`    | 코드 스타일 변경 |
| `docs`     | 문서 수정 |
| `test`     | 테스트 코드 추가 또는 수정 |
| `chore`    | 빌드 / 설정 관련 작업, 패키지 매니저 설정 등 |
| `design`   | 프론트엔드 UI 작업 또는 스타일링 수정 |
| `ci`       | CI · CD 관련 설정 작업 |

<br/>


## 커밋 메시지 예시
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