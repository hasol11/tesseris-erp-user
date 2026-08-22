# 📱 TESSERIS — User Frontend

> **Team Project · Personal Fork**

TESSERIS의 일반 사용자·사업자·가맹점이 사용하는 React 기반 User Frontend입니다.

저는 **알림 기능을 중심으로 공지사항, 마이페이지, PIN 변경 등의 화면 구현과 Backend API 연동**을 담당했습니다.

---

## 🙋‍♀️ My Contribution

### 🔔 Notification

[Alert Backend](https://github.com/hasol11/tesseris-erp-alert)와 연결해  
사용자가 알림을 조회하고 확인하는 사용자 흐름을 구현했습니다.

- 알림 내역 조회 및 화면 표시
- 읽지 않은 알림 개수 표시
- Header의 Unread Badge 처리
- 알림 확인 시 읽음 API 호출
- 알림 목록과 Badge 상태 동기화
- 유형별 알림 수신 설정 UI

<pre>
Alert Backend
      ↓
알림 목록 조회
      ↓
Unread Badge 표시
      ↓
사용자 알림 확인
      ↓
읽음 API
      ↓
목록 / Badge 갱신
</pre>

알림 페이지 하나만 구현하는 것이 아니라  
**같은 알림 상태가 Header와 목록에서 일관되게 보이도록 연결**했습니다.

---

### 📢 Notice

- 공지사항 목록 화면
- 공지사항 상세 화면
- [Main Backend](https://github.com/hasol11/tesseris-erp-backend) 공지 API 연동

---

### 👤 My Page

- 사용자 정보 조회
- Role에 따른 마이페이지 메뉴 구성
- 일반 사용자 / 사업자 / 가맹점별 화면 분기
- Backend 사용자 데이터 연동

---

### 🔐 PIN Change

현재 비밀번호 확인부터 새로운 PIN 적용까지 이어지는 단계별 사용자 Flow를 구현했습니다.

<pre>
PIN 변경 요청
    ↓
현재 비밀번호 확인
    ↓
새 PIN 입력
    ↓
PIN 재확인
    ↓
Backend API
</pre>

---

## 🛠 Tech Stack

- React
- React Router
- Material UI
- Zustand
- Axios
- STOMP / SockJS

---

## 🔗 TESSERIS Repositories

| Repository | 역할 |
| --- | --- |
| [Main Backend](https://github.com/hasol11/tesseris-erp-backend) | ERP/PMS Main Backend |
| [Alert Backend](https://github.com/hasol11/tesseris-erp-alert) | Notification Backend |
| [User Frontend](https://github.com/hasol11/tesseris-erp-user) | User Web Service |
| [Admin Frontend](https://github.com/hasol11/tesseris-erp-admin) | Admin Web Service |

**Original Repository**  
https://github.com/7GUYZ/ERP-Tesseris-react

---

## 👥 Team Project

본 Repository는 TESSERIS 팀 프로젝트의 User Frontend 개인 Fork입니다.

본 README에서는 프로젝트 전체 사용자 기능이 아닌  
**제가 직접 구현하거나 Backend와 연결한 영역을 중심으로 정리했습니다.**
