# 💰 가계부 (Expense Tracker PWA)

링크 하나로 어디서든, 어떤 기기에서든 쓸 수 있는 가계부 앱입니다.

- ✅ PC, 모바일, 태블릿 모두 지원
- ✅ PC가 꺼져 있어도 항상 접속 가능
- ✅ 오프라인에서도 동작
- ✅ 홈 화면에 설치하면 네이티브 앱처럼 사용
- ✅ 서버 없음 — 데이터는 각 기기 브라우저에 저장

---

## 배포 방법 (GitHub Pages)

### 1. GitHub 저장소 만들기

1. https://github.com/new 에서 새 저장소 생성
   - 저장소 이름: `expense-tracker` (원하는 이름)
   - Public 선택
   - Create repository 클릭

### 2. 파일 업로드

저장소 페이지에서 **"uploading an existing file"** 클릭 후,
아래 파일/폴더를 전부 드래그해서 업로드합니다:

```
index.html
manifest.json
sw.js
icons/
  icon-192.png
  icon-512.png
```

Commit changes 클릭.

### 3. GitHub Pages 켜기

1. 저장소 → **Settings** 탭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. Source 항목에서:
   - Branch: **main**
   - Folder: **/ (root)**
4. **Save** 클릭

### 4. 완료!

1~2분 후 이 주소로 접속하면 됩니다:

```
https://내아이디.github.io/expense-tracker
```

이 링크를 폰으로 열면 가계부 앱을 쓸 수 있고,
**"홈 화면에 추가"**하면 앱처럼 설치됩니다.

---

## 폰에서 앱처럼 설치하기

### Android (Chrome)
1. 링크를 Chrome으로 열기
2. 앱 내 "홈 화면에 추가" 배너가 뜨면 **설치** 클릭
3. 또는 Chrome 메뉴(⋮) → "홈 화면에 추가"

### iPhone (Safari)
1. 링크를 Safari로 열기
2. 하단 공유 버튼(□↑) 클릭
3. **"홈 화면에 추가"** 선택

---

## 참고사항

- 데이터는 **각 기기의 브라우저**에 저장됩니다 (IndexedDB)
- 기기 간 데이터 동기화는 되지 않습니다 (각각 독립)
- 브라우저 데이터를 삭제하면 가계부 데이터도 사라집니다
- 시크릿/비공개 모드에서는 데이터가 유지되지 않습니다

---

## Google AdSense 광고 설정

### 1. AdSense 가입 및 승인

1. https://adsense.google.com 에서 가입
2. 사이트 URL에 `https://내아이디.github.io` 입력
3. Google의 사이트 검토 승인 대기 (보통 1~14일)

### 2. 광고 단위 만들기

1. AdSense 대시보드 → 광고 → 광고 단위별
2. **디스플레이 광고** 선택 → 이름 입력 → 만들기
3. 생성된 코드에서 두 가지 값을 복사:
   - `data-ad-client="ca-pub-1234567890123456"` → 게시자 ID
   - `data-ad-slot="1234567890"` → 광고 단위 ID

### 3. index.html에 적용

`index.html`을 메모장으로 열어서 두 곳을 수정합니다:

**① 상단 script 태그** (7번째 줄 근처):

```
변경 전: ca-pub-XXXXXXXXXXXXXXXX
변경 후: ca-pub-1234567890123456  (본인 게시자 ID)
```

**② 스크립트 내부 설정** ("Google AdSense 설정" 검색):

```
변경 전: const AD_CLIENT = "ca-pub-XXXXXXXXXXXXXXXX";
변경 후: const AD_CLIENT = "ca-pub-1234567890123456";

변경 전: const AD_SLOT   = "XXXXXXXXXX";
변경 후: const AD_SLOT   = "1234567890";
```

수정 후 GitHub에 다시 업로드하면 광고가 표시됩니다.

### 광고 위치

현재 3곳에 광고가 배치되어 있습니다:
- **홈 화면**: 잔액 카드 아래
- **내역 탭**: 상단
- **통계 탭**: 차트와 카테고리 분석 사이
