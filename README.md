## DBook

### 개요
DBook은 독서 경험을 더 풍성하게 만드는 안드로이드 앱입니다. 책 목록 탐색, 상세 정보 확인, 커뮤니티 리뷰 및 협업형 독서 챌린지 기능을 제공합니다.

### 주요 기능
- 추천/내 서재/검색/알림 등 기본 내비게이션
- 도서 목록 및 상세 화면
- 키워드 태그, 리뷰 미리보기, 챌린지 진행률 표시

### 변경 내역
#### 2025-09-25
- 도서 상세 화면 추가: `BookDetailActivity`
  - 상단 툴바, 줄거리, 키워드 ChipGroup, 챌린지 카드(진행률), 리뷰 미리보기 섹션 구성
  - 더미 키워드/리뷰 샘플 및 토스트 안내 메시지 추가
- 목록 → 상세 화면 이동 연결: `BookAdapter`에서 아이템 클릭 시 `BookDetailActivity`로 이동
- 레이아웃 리소스 추가: `activity_book_detail.xml`, `item_keyword_chip.xml`, `item_review_preview.xml`
- 문자열 리소스 강화: 상세 화면 텍스트, 챌린지/리뷰 샘플 등 (`app/src/main/res/values/strings.xml`)
- 매니페스트 업데이트: `AndroidManifest.xml`에 `BookDetailActivity` 등록, `HomeActivity`를 런처로 지정
- 런처 아이콘 벡터 수정: `app/src/main/res/drawable/ic_launcher_foreground.xml`

### 폴더 구조(발췌)
```
app/
  src/main/
    java/com/example/d_book/
      BookAdapter.java
      BookDetailActivity.java
    res/
      layout/
        activity_book_detail.xml
        item_keyword_chip.xml
        item_review_preview.xml
      values/strings.xml
      drawable/ic_launcher_foreground.xml
    AndroidManifest.xml
```

### 개발 환경
- Android Studio 최신 버전 권장
- 최소 구성: AndroidX, Material Components

### 빌드/실행
1. Android Studio로 프로젝트 열기
2. Gradle Sync 완료 후 `app` 모듈 실행
3. 홈 화면에서 도서 목록 아이템을 탭하여 상세 화면 이동 확인


