# GenProject 2nd project

# GenProject

Spring Boot + Thymeleaf + MyBatis + Oracle を連携した Web プロジェクトです。
ユーザー(User)とグループ(Group)の CRUD サンプルを含み、Thymeleaf テンプレートエンジンを使用して View を処理します。

---

## 主な担当内容

本プロジェクトでは、リアルタイム通知・チャット、掲示板（投稿・コメント）、通報、簡易マッチングフィルターなどの主要なユーザー機能を自ら企画・設計し、実装しました。

- **リアルタイム通知システム**
    - Spring WebSocket & STOMP を用いたリアルタイム通知の実装
    - コメント作成、通報、チャットメッセージなどの特定イベント発生時に対象者へ通知を送信
- **リアルタイムチャット機能**
    - グループごとにチャットルームを生成し、WebSocket で接続
    - チャットメッセージの送受信、削除、通報処理
- **掲示板 & コメント**
    - 投稿 CRUD、ページネーション処理
    - 投稿の並び替え、カテゴリー別フィルターおよび検索
    - コメントの作成・編集・削除、階層型コメント（大コメント）構造を実装
    - 通報機能と連携し、違法・不適切コンテンツを管理
- **通報システム**
    - 投稿・コメント・チャットメッセージの通報モーダルを実装
    - 通報カテゴリと理由を選択し、通報履歴を DB に保存
    - 通報の累積に応じた制裁ロジックを設計
- **簡易マッチングフィルター**
    - 条件（カテゴリー、年齢層、性別など）によるグループリストのフィルタリング
    - フィルター結果から詳細ページ & チャットルームへ動的に接続

---

## Stack

- **Framework:** Spring Boot
- **View:** Thymeleaf
- **ORM:** MyBatis
- **DB:** Oracle XE
- **ビルド:** Gradle 

---

```properties
DB 設定 (application.properties)
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:xe
spring.datasource.username=system
spring.datasource.password=12345

mybatis.mapper-locations=classpath:mapper/*.xml
```

---

## 接続 URL
- http://localhost:8080/

---

## 学び・感想
今回のプロジェクトを通じて、リアルタイム WebSocket 通信やユーザー向け機能（通知、通報）を自ら設計・実装することで、
Spring Boot の MVC 構造と DB 連携、認証フローを実務に近い形で経験できました。
チームメンバーとのコミュニケーションの重要性や協働作業の大切さを学び、
また GitHub Flow に基づくブランチ戦略とコードレビューの経験を通じて、実践的なチーム開発力を高めることができました。

-----------------------------------------------------------------------


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
- **빌드:** Gradle

---

## DB 설정 (application.properties)

```properties
spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:xe
spring.datasource.username=system
spring.datasource.password=12345

mybatis.mapper-locations=classpath:mapper/*.xml
```

## 접속 주소

- http://localhost:8080/

---

## 느낀점

이번 프로젝트를 통해 실시간 WebSocket 통신과 사용자 편의 기능(알림, 신고)을 직접 설계하고 구현하면서,
Spring Boot MVC 구조와 DB 연동, 인증 흐름을 실무에 가깝게 경험할 수 있었습니다.
팀원 간 커뮤니케이션의 중요성과 협업에 대해 많은 경험을 했습니다.
또한 GitHub Flow 기반의 브랜치 전략과 코드 리뷰 경험을 통해 실전 협업 역량을 키울 수 있었습니다.



