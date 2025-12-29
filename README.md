# 🚀 통합 플랫폼 웹사이트 구축 프로젝트

본 프로젝트는 **코딩 테스트**, **게임 스토어**, 그리고 **웹 게임 서비스 연동**을 하나로 통합한 고성능 플랫폼을 구축하고 운영하는 것을 목표로 합니다.

## 1. 주요 개발 예정
1. **코딩 테스트 및 기타 게임 플랫폼 필요 모듈**: 응시자 실시간 모니터링 및 코드 컴파일/실행 환경 제공 (30%)
2. **게임 스토어**: Windows 애플리케이션 기반 게임 등록, 자동 업데이트 및 웹 게임 플랫폼 서비스 연동. (0%)
3. **모바일**: 예정 ( 0% )

---

## 2. 기술 스택 (Tech Stack)

### 🎨 Frontend
- **Framework**: `React.js (v18)`, `Next.js` 
- **State Management**: `Redux`, `Recoil` 

### ⚙️ Backend
- **Languages**: `Go`, `Spring Boot` , `Node.js`
- **Infrastructure**: `Nginx`
- **Communication**: `RESTful API`, `WebSocket`
- **Messaging**: `Apache Kafka`

### 📦 Database & DevOps
- **Database**: `MySQL` (도입 예정), `H2` (로컬 테스트용)
- **Deployment**: `Docker`, `Kubernetes (K8s)` (3개 노드 운영 기준)
- **CI/CD**: 도입 및 자동화 검토 중

---

## 3. 프로젝트 구성

현재 플랫폼은 마이크로서비스 아키텍처 MSA 전환 할 수 있도록 개발을 지향하며 각 모듈은 다음과 같이 구성됩니다. 
 - MSA 전환 시 프로젝트 명 예시 : api-server(PP), api-server(FI) 

| 모듈명 | 상태 | 주요 역할 |
| :--- | :--- | :--- |
| **web-front** | 구축 완료 (고도화 필요) | React 기반 사용자 웹 서비스 화면 |
| **API-gateway** | **완료** | 인증 필터 및 시그니처 검증 (Go 기반) |
| **API-server** | 구축 완료 (고도화 필요) | 핵심 비즈니스 로직 처리 및 API 제공 |
| **Signal-server** | 구축 완료 (고도화 필요) | P2P 통신 매개 및 SFU 서버 사용자 정보 전달 |
| **SFU-server** | 개발 중 | 실시간 미디어 스트리밍(Streaming) 주체 서버 |
| **game-server** | 개발 중 | Protobuf 기반 IOCP 실시간 통신 성능 극대화 서버 |
| **coding-test-server**| 개발 중 | 코딩 테스트 답안 검증 및 결과 처리 서버 |
| **oauth2-server** | 도입 예정 | 통합 로그인(SSO) 지원을 위한 인증 서버 |
| **kubernetes-setting**| 자료 폴더 | K8s 클러스터 자동화 Shell Script (3 Nodes) |
| **Infra-setting**| 자료 폴더 | Kafka, Redis 등등 인프라 관련 내용 기입 |


---

## 4. 최종 목표 (Key Milestones)
1. **성능 극대화**: 로드 밸런싱 등 최신 기술을 적용하여 서버 효율성 최적화.
2. **통합 플랫폼 구축**: 웹 기반의 유기적인 서비스 생태계 조성.
3. **멀티 OS 지원**: macOS 및 Windows 환경의 전용 클라이언트 구축.
4. **자체 게임 개발**: 플랫폼에 최적화된 웹 사용자와 게임 사용자의 계정 정보를 연동하여  런칭.

---

## 5. 설치 및 실행 환경 (Prerequisites)
- **Runtime**: `Node.js v18`, `Go 1.22`, `JDK 17`
- **Compiler**: `gcc`
