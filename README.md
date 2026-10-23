<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4F46E5,100:06B6D4&height=180&section=header&text=Shin%20In-Gyu&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=Backend%20%26%20App%20Developer&descAlignY=58&descSize=18" width="100%" />

<img src="https://readme-typing-svg.demolab.com?font=Pretendard&weight=600&size=20&pause=1200&color=4F46E5&center=true&vCenter=true&width=520&lines=%EC%95%88%EB%85%95%ED%95%98%EC%84%B8%EC%9A%94%2C+%EC%8B%A0%EC%9D%B8%EA%B7%9C%EC%9E%85%EB%8B%88%EB%8B%A4+%F0%9F%91%8B;%ED%95%99%EA%B5%90+%EC%83%9D%ED%99%9C%EC%9D%84+%ED%8E%B8%ED%95%98%EA%B2%8C+%EB%A7%8C%EB%93%9C%EB%8A%94+%EC%95%B1%EC%9D%84+%EB%A7%8C%EB%93%AD%EB%8B%88%EB%8B%A4" />

</div>

## 🙋 About Me

- 🏫 강남대학교 재학 중
- 🔔 강남대 공지 알림 앱 **강림이(kangrimi)** 를 팀원과 둘이 만들어 출시하고, 백엔드와 운영을 맡고 있습니다 (누적 다운로드 약 800회)
- 🛠️ 백엔드 API부터 React Native 앱, Docker 배포까지 직접 다룹니다
- 📫 inkyu102077@gmail.com

## 🧰 Tech Stack

**Backend**

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" /> <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white" /> <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white" /> <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" /> <img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />

**App**

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" /> <img src="https://img.shields.io/badge/React%20Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" /> <img src="https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white" /> <img src="https://img.shields.io/badge/TanStack%20Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white" /> <img src="https://img.shields.io/badge/Zustand-443E38?style=for-the-badge&logo=react&logoColor=white" />

**Infra**

<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" /> <img src="https://img.shields.io/badge/Oracle%20Cloud-F80000?style=for-the-badge&logo=oracle&logoColor=white" /> <img src="https://img.shields.io/badge/Firebase-DD2C00?style=for-the-badge&logo=firebase&logoColor=white" />

## 🚀 Projects

### 🔔 강림이 (kangrimi) — 강남대학교 공지 알림 앱

> 학교 홈페이지 26개 게시판에 흩어진 학사·장학·학과 공지를 한 앱에 모으고, 관심 키워드 공지가 올라오면 푸시로 알려줍니다.

**2인 팀 프로젝트로, 기획부터 함께 했고 백엔드 전체와 배포·운영을 맡았습니다.** 앱에서는 고급 검색, 공지 이미지 뷰어·저장, iOS 대응 등을 개발했습니다.
📱 **App Store · Google Play 출시, 누적 다운로드 약 800회**

<p>
  <a href="https://apps.apple.com/us/app/%EA%B0%95%EB%A6%BC%EC%9D%B4-%EA%B0%95%EB%82%A8%EB%8C%80%ED%95%99%EA%B5%90-%EA%B3%B5%EC%A7%80%EC%95%B1/id6758569535"><img src="https://img.shields.io/badge/App%20Store-0D96F6?style=for-the-badge&logo=appstore&logoColor=white" /></a>
  <a href="https://play.google.com/store/apps/details?id=com.campusnotice.fe"><img src="https://img.shields.io/badge/Google%20Play-414141?style=for-the-badge&logo=googleplay&logoColor=white" /></a>
</p>

`FastAPI` `SQLAlchemy(async)` `APScheduler` `React Native` `Expo` `Docker` `GitHub Actions` `Oracle Cloud`

**주요 기능**
- 26개 게시판을 30분마다 크롤링해 본문·표·이미지·첨부를 앱에서 읽기 좋은 형태로 변환
- 키워드 구독 푸시 알림 (Expo Push, 실패한 알림은 다음 주기에 자동 재전송)
- 날짜·카테고리·학과 고급 검색, 스크랩, 공지 이미지 뷰어·저장
- 캠퍼스맵(건물·층·호실), 달구지 셔틀 시간표

**해결한 문제**
- **안드로이드에서 공지 이미지가 안 뜨는 문제**: 원인이 학교 서버의 중간 인증서 누락임을 찾아내 서버 측 이미지 프록시로 해결하고, 프록시에 도메인 화이트리스트로 SSRF 방어 적용
- **공지 상세 응답 지연**: 매번 학교 사이트를 긁던 구조를 DB 우선 반환 + 백그라운드 갱신(URL당 10분 간격)으로 바꿔 즉시 응답
- **동시 크롤링 충돌**: 정기·초기·수동 크롤링이 겹치면 유니크 제약 위반으로 배치 전체가 롤백되던 문제를 공용 락으로 직렬화
- **셔틀 시간표 갱신**: 원본 이미지를 해시로 변경 감지해 바뀔 때만 요일별로 분할하고, 콘텐츠 해시 파일명으로 캐시 효율 확보
- **배포 자동화**: `main` 푸시 → Docker 이미지 빌드 → Oracle Cloud 서버 자동 배포

### 🧠 코드 한입 (CodeBite) — CS 개념 퀴즈 학습 앱

> 4지선다·OX·단답·매칭 퀴즈로 CS 개념을 매일 조금씩 익히는 듀오링고 스타일 학습 앱

`Spring Boot 3` `Java 21` `Spring Security` `JWT` `OAuth2` `JPA` `PostgreSQL` `Expo` `Zustand` `TanStack Query`

- **소셜 로그인**(Kakao·GitHub·Google OAuth2) 백엔드 구현 및 앱 연동
- **팔로우·유저 검색·랭킹** API 구현, 검색 결과의 팔로우 여부 조회에서 **N+1 쿼리 최적화**
- **상점·아이템·배너**, **북마크**, **푸시 알림** 기능을 백엔드부터 앱 화면까지 개발

<p>
  <a href="https://github.com/CodeBiteApp/frontend"><img src="https://img.shields.io/badge/CodeBite%20Frontend-181717?style=flat-square&logo=github&logoColor=white" /></a>
</p>

## 📊 GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Shin-In-Gyu&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&theme=transparent&title_color=4F46E5&icon_color=06B6D4" />
<img height="165" src="https://streak-stats.demolab.com?user=Shin-In-Gyu&hide_border=true&theme=transparent&ring=4F46E5&fire=06B6D4&currStreakLabel=4F46E5" />

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4F46E5,100:06B6D4&height=100&section=footer" width="100%" />

</div>
