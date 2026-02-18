# 📱 TESSERIS 사용자 프론트엔드 (User Frontend)

> TESSERIS 서비스를 이용하는 일반 사용자, 사업자, 가맹점을 위한 React 기반 웹 애플리케이션입니다. 사용자 친화적인 UI/UX를 통해 간편한 결제, 수당 확인, 가맹점 신청 등 다양한 기능을 제공합니다.

### 🏛️ TESSERIS 전체 프로젝트 구조
- [Main Server (ERP-PMS)](https://github.com/hasol11/tesseris-erp-backend)
- [Alert Server](https://github.com/hasol11/tesseris-erp-alert)
- **[User Frontend](https://github.com/hasol11/tesseris-erp-user) (👈 현재 레포지토리)**
- [Admin Frontend](https://github.com/hasol11/tesseris-erp-admin)

<br>
<!--
## 🚀 Live Demo
**[https://kschost.ddns.net/react](https://kschost.ddns.net/react)**

<br> 
-->

## ✨ 주요 기능
- **사용자 맞춤형 대시보드**: 일반, 사업자, 가맹점 등 사용자의 역할에 따라 동적으로 다른 메뉴와 기능을 제공합니다.
- **포인트(TS) 관리**: 포인트 충전, 결제, 선물하기 등 포인트와 관련된 모든 기능을 제공합니다.
- **가맹점 및 이벤트**: 주변 가맹점을 검색하고, 진행 중인 쿠폰 이벤트를 확인하고 참여할 수 있습니다.

<br>

## 🙋‍♀️ My Contribution
사용자 경험 향상을 목표로 다음과 같은 핵심 페이지 및 기능을 개발했습니다.

- **알림 시스템 (`/alert`)**
  - 실시간으로 수신된 알림을 처리하여, 읽지 않은 알림 개수를 **헤더의 배지에 표시**하고 알림 페이지와 **상태를 동기화**하는 로직을 개발했습니다.
  - 사용자가 알림을 클릭했을 때 **'읽음'으로 상태를 변경**하는 기능을 구현했습니다.
  - 사용자가 공지, 쿠폰 등 유형별로 알림 수신 여부를 설정하는 페이지를 구현했습니다.

- **콘텐츠 및 정보 페이지**
  - **공지사항 시스템 (`/notice`)**: 공지사항 목록과 상세 보기 페이지를 개발했습니다.
  - **약관 및 이용동의 (`/terms`)**: 여러 종류의 약관을 사용자가 확인하고 동의할 수 있는 페이지를 구현했습니다.

- **마이페이지 및 보안 기능 (`/mypage`, `/pin-change`)**
  - 일반/사업자/가맹점 등 역할에 따라 다른 메뉴가 보이는 마이페이지의 분기 처리 로직을 개발했습니다.
  - 보안 강화를 위해 현재 비밀번호 확인을 포함한 4단계의 PIN 번호 변경 프로세스를 구현했습니다.

<br>

## 🛠️ 기술 스택
- **Library**: `React`, `React Router`
- **UI Framework**: `Material-UI (MUI)`
- **State Management**: `Zustand`
- **HTTP Client**: `Axios`
- **Real-time Communication**: `@stomp/stompjs`, `sockjs-client`
- **Payment**: `@tosspayments/payment-sdk`

<br>

## 🚀 실행 방법 (Getting Started)

### 사전 요구사항
- Node.js: 16.0.0 이상
- npm: 8.0.0 이상

### 1. 프로젝트 클론
```bash
git clone https://github.com/hasol11/tesseris-erp-user.git
cd tesseris-erp-user
```

### 2. 의존성 패키지 설치
`package.json`에 명시된 모든 라이브러리를 한 번에 설치합니다.
```bash
npm install
```

### 3. 로컬 개발 서버 실행
```bash
npm start
```
개발 서버가 실행되면 브라우저에서 `http://localhost:3000`으로 접속할 수 있습니다.

### 4. 환경 변수 설정
프로젝트 루트 경로에 `.env` 파일을 생성하고 아래 내용을 추가해야 합니다.
```
# API 서버 URL
REACT_APP_API_BASE_URL=http://localhost:8080
REACT_APP_ALERT_API_URL=http://localhost:8081

# 결제 시스템 설정
REACT_APP_TOSSPAYMENTS_CLIENT_KEY=your_toss_client_key

# WebSocket 설정
REACT_APP_WEBSOCKET_URL=ws://localhost:8080/ws
```

<br>

## 📂 폴더 구조 (Directory Structure)
```
ERP-Tesseris-react/
└── src/
    ├── api/          # API 통신 모듈
    ├── components/   # 재사용 가능한 컴포넌트
    ├── context/      # React Context
    ├── pages/        # 페이지 컴포넌트
    ├── routes/       # 라우팅 설정
    ├── store/        # 상태 관리 (Zustand)
    ├── styles/       # CSS 스타일
    └── utils/        # 유틸리티 함수
