# 신인규 (Shin In-Gyu)

강남대학교 재학 중인 백엔드 지향 개발자입니다. API 설계부터 모바일 앱, 배포와 운영까지 한 서비스의 전 구간을 직접 다루는 것을 선호합니다.

inkyu102077@gmail.com

---

## 기술 스택

| 영역 | 사용 기술 |
| :--- | :--- |
| Backend | Python, FastAPI, SQLAlchemy (async), Java, Spring Boot, Spring Security |
| Database | PostgreSQL, SQLite |
| App | TypeScript, React Native, Expo, TanStack Query, Zustand |
| Infra | Docker, GitHub Actions, Oracle Cloud |

---

## 프로젝트

### 강림이 (kangrimi) — 강남대학교 공지 알림 앱

학교 홈페이지 26개 게시판에 흩어진 공지를 한 앱에 모으고, 구독한 키워드의 공지가 올라오면 푸시로 알려줍니다.
2인 팀으로 기획부터 함께 했고, 백엔드 전체와 배포·운영을 맡았습니다. App Store와 Google Play에 출시해 누적 다운로드 약 800회입니다.

[App Store](https://apps.apple.com/us/app/%EA%B0%95%EB%A6%BC%EC%9D%B4-%EA%B0%95%EB%82%A8%EB%8C%80%ED%95%99%EA%B5%90-%EA%B3%B5%EC%A7%80%EC%95%B1/id6758569535) · [Google Play](https://play.google.com/store/apps/details?id=com.campusnotice.fe)

**구조**

- 26개 게시판을 30분마다 크롤링해 본문, 표, 이미지, 첨부를 앱에서 읽기 좋은 형태로 변환
- 키워드 구독 푸시(Expo Push). 전송에 실패한 알림은 다음 주기에 24시간 안에서 재전송
- 캠퍼스맵, 달구지 셔틀 시간표, 날짜·카테고리·학과 기준 고급 검색, 스크랩
- `main` 푸시 시 Docker 이미지 빌드 후 Oracle Cloud로 자동 배포

**개선 결과**

| 항목 | 전 | 후 |
| :--- | :--- | :--- |
| 공지 상세 서버 처리 시간 | 평균 832ms | 평균 5~11ms |
| 게시판 목록 1페이지 응답 크기 (중앙값) | 30.8KB | 8.1KB |
| 가장 무거운 게시판의 목록 1페이지 | 2.2MB | 6.7KB |
| 푸시 발송 대상 게시판 | 5 / 26개 | 26 / 26개 |

**기술적으로 다룬 문제**

- **공지 이미지가 안드로이드에서 열리지 않던 문제.** 학교 서버가 중간 인증서를 보내지 않는 것이 원인이었습니다. 서버 측 이미지 프록시로 우회하고, 도메인 화이트리스트와 리다이렉트 hop별 검사로 SSRF를 막았으며, 프록시 URL에는 HMAC 서명을 붙였습니다.
- **상세 응답 지연.** 요청마다 학교 사이트를 긁던 구조를 DB 우선 반환과 백그라운드 갱신(URL당 10분 간격)으로 바꿨습니다.
- **동시 크롤링 충돌.** 정기·초기·수동 크롤링이 겹치면 유니크 제약 위반으로 신규 공지 배치 전체가 롤백되었습니다. 크롤링 진입점을 하나로 모으고 공용 락으로 직렬화했습니다.
- **목록 응답 경량화.** 일부 과거 공지에 base64 이미지가 그대로 저장되어 행 하나가 1MB를 넘었습니다. 목록은 필요한 필드만 응답하고 본문·이미지·첨부는 지연 로딩하도록 바꿨습니다.

`FastAPI` `SQLAlchemy` `APScheduler` `React Native` `Expo` `Docker` `GitHub Actions` `Oracle Cloud`

---

### 코드 한입 (CodeBite) — CS 개념 퀴즈 학습 앱

4지선다, OX, 단답, 매칭 퀴즈로 CS 개념을 매일 조금씩 익히는 학습 앱입니다.

- Kakao, GitHub, Google OAuth2 소셜 로그인 백엔드 구현과 앱 연동
- 팔로우, 유저 검색, 랭킹 API. 검색 결과의 팔로우 여부 조회에서 N+1 쿼리를 제거
- 상점·아이템·배너, 북마크, 푸시 알림을 백엔드부터 앱 화면까지 개발

`Spring Boot 3` `Java 21` `Spring Security` `JWT` `JPA` `PostgreSQL` `Expo`

[Frontend 저장소](https://github.com/CodeBiteApp/frontend)
