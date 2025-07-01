# GenProject 2nd project

# GenProject

Spring Boot + Thymeleaf + MyBatis + Oracle 연동 웹 프로젝트입니다.  
회원(User)과 그룹(Group) CRUD 예제를 포함하며 Thymeleaf 템플릿 엔진을 사용해 View를 처리합니다.

---

## 주요 역할

본 프로젝트에서 저는 실시간 알림/채팅, 게시판(게시글/댓글), 신고, 간편매칭 필터 등 주요 사용자 기능을 직접 기획하고 설계하여 구현했습니다.

- **실시간 알림 시스템**
    - Spring WebSocket & STOMP 기반 실시간 알림 구현
    - 특정 이벤트(댓글 작성, 신고, 채팅 메시지) 발생 시 대상자에게 알림 전송
- **실시간 채팅 기능**
    - 그룹별 채팅방 생성 및 WebSocket 연결
    - 채팅 메시지 송수신, 삭제, 신고 처리
- **게시판 & 댓글**
    - 게시글 CRUD, 페이징 처리
    - 게시글 정렬 및 카테고리별 필터 및 검색
    - 댓글 작성/수정/삭제 및 대댓글(계층형) 구조 구현
    - 신고 기능과 연동하여 불법/부적절 콘텐츠 관리
- **신고 시스템**
    - 게시글/댓글/채팅 메시지 신고 모달 구현
    - 신고 유형 및 사유 선택, 신고 내역 DB 저장
    - 누적 신고 시 제재 로직 설계
- **간편매칭 필터**
    - 조건(카테고리, 연령, 성별 등)에 따른 그룹 리스트 필터링
    - 필터 결과에서 상세 페이지 & 채팅방으로 동적 연결

---

## Stack

- **Framework:** Spring Boot
- **View:** Thymeleaf
- **ORM:** MyBatis
- **DB:** Oracle XE
- **빌드:** Gradle (또는 Maven)

---

## DB 설정 (application.properties)

```properties
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:xe
spring.datasource.username=system
spring.datasource.password=12345

mybatis.mapper-locations=classpath:mapper/*.xml
```

## 실행 방법

- ./gradlew bootRun

---


## 접속 주소

- http://localhost:8080/

---

## 느낀점

이번 프로젝트를 통해 실시간 WebSocket 통신과 사용자 편의 기능(알림, 신고)을 직접 설계하고 구현하면서,
Spring Boot MVC 구조와 DB 연동, 인증 흐름을 실무에 가깝게 경험할 수 있었습니다.
팀원 간 커뮤니케이션의 중요성과 협업에 대해 많은 경험을 했습니다.
또한 GitHub Flow 기반의 브랜치 전략과 코드 리뷰 경험을 통해 실전 협업 역량을 키울 수 있었습니다.



