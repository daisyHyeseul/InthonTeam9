# 나의 조각집

**나의 조각집**은 사용자가 "조각글"을 작성하고, 다른 사용자의 조각글에 예술의 메시지를 전하며 서로의 조각들을 모아 **조각집**을 만들어가는 프로젝트입니다.

---

## 📜 프로젝트 개요

- **사용자 정보 입력**: 사용자 전화번호, 닉네임, 조각글을 작성하고 전송합니다.
- **유사 조각글 매칭**: 전송 후, 응답 페이지에서 자신의 조각글과 비슷한 다른 사용자의 조각글을 확인합니다.
- **답장 기능**: 다른 사용자의 조각글에 답장을 작성할 수 있습니다.
- **보관함 기능**: 자신의 조각글에 대한 답장을 보관함에서 확인할 수 있습니다.
- **예술작품 추천**: 작성한 조각글과 유사한 예술작품을 추천받습니다.

---

## 🎯 주요 기능

- **사용자 등록**  
  사용자는 전화번호와 비밀번호를 통해 간편하게 가입할 수 있습니다. CoolSMS를 통해 인증번호를 전송하여 보안성을 강화합니다.

- **조각글 작성 및 공유**  
  사용자는 짧은 글을 작성하여 게시할 수 있으며, 이를 통해 다른 사용자와 공유하거나 피드백을 받을 수 있습니다.

- **조각글 답변 기능**  
  작성된 조각글에 대해 댓글로 답장을 남길 수 있으며, 이를 통해 사용자 간의 소통이 가능합니다.

- **자동 응답 생성**  
  **GPT4o-mini**를 이용하여 조각글에 대한 관련 예술작품을 자동으로 추천받아 감성을 더해줍니다.

- **데이터 저장 및 관리**  
  **MongoDB Atlas**를 통해 사용자 정보, 조각글, 답장 등의 데이터를 안전하게 저장하고 관리합니다.

---

## 🛠 기술 스택

| 기술               | 설명                                                                                 |
|--------------------|--------------------------------------------------------------------------------------|
| **React**         | 프론트엔드 UI 구축, 컴포넌트 기반 구조로 화면 및 입력 폼 구성                        |
| **Redux**         | 전역 상태 관리, 사용자 데이터와 입력 값을 일관성 있게 유지                            |
| **Vercel**        | 프론트엔드 배포, 애플리케이션을 웹에 쉽게 배포하여 사용자에게 제공                    |
| **Spring**        | 백엔드 API 구축, 데이터 처리 및 클라이언트와의 통신 관리                             |
| **MongoDB Atlas** | 클라우드 기반 데이터베이스, 사용자 정보와 조각글 데이터를 안전하게 관리               |
| **CoolSMS**       | SMS 전송 API, 비밀번호 및 알림 전송에 활용                                           |
| **GPT4o-mini**    | 조각글에 대한 예술작품 추천 생성에 활용                                             |

---

---

## 📂 프로젝트 구조

```plaintext
.
├── client/                 # 프론트엔드 코드 (React)
│   ├── src/
│   │   ├── components/     # UI 컴포넌트 모음 (예: 입력 폼, 버튼 등)
│   │   ├── pages/          # 각 페이지 컴포넌트 (예: Send, Submitted 등)
│   │   ├── assets/         # 이미지, 아이콘 등 정적 파일
│   │   ├── App.js          # 최상위 App 컴포넌트
│   │   ├── index.js        # 엔트리 포인트
│   │   └── ...             # 기타 폴더 및 파일
│   └── public/             # 정적 파일 (favicon, HTML 템플릿 등)
│
├── server/                 # 백엔드 코드 (Spring Boot)
│   ├── src/main/java/      # Java 소스 파일
│   │   ├── com/example/    # 주요 패키지
│   │   │   ├── controller/ # API 엔드포인트 컨트롤러 (예: 조각글, 답변 등록 API)
│   │   │   ├── service/    # 서비스 로직
│   │   │   └── repository/ # 데이터베이스 인터페이스
│   ├── resources/          # 설정 파일 (application.yml 등)
│   └── build.gradle        # Gradle 빌드 설정
│
├── .env                    # 환경 변수 파일 (API URL, API 키 등)
├── .gitignore              # Git에서 제외할 파일 목록
├── README.md               # 프로젝트 설명 파일
└── LICENSE                 # 라이선스 파일
