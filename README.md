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
2. 저장소 이름: `expense-tracker`
3. **Public** 선택 → Create repository

### 2. 파일 업로드

저장소 페이지에서 **uploading an existing file** 클릭 후
아래 파일들을 드래그해서 업로드:

- `index.html`
- `manifest.json`
- `sw.js`
- `icons/` 폴더

### 3. GitHub Pages 켜기

Settings → Pages → Branch: **main** → Save

### 4. 접속

```
https://내아이디.github.io/expense-tracker
```

---

## Google AdSense 설정

`index.html`에서 두 곳을 수정:

1. 상단 `<script>` 태그의 `ca-pub-XXXXXXXXXXXXXXXX` → 본인 게시자 ID
2. 스크립트 내부의 `AD_CLIENT`과 `AD_SLOT` 값 → 본인 ID

---

## 참고사항

- 데이터는 각 기기의 브라우저에 저장됩니다 (IndexedDB)
- 기기 간 데이터 동기화는 되지 않습니다
- 브라우저 데이터를 삭제하면 가계부 데이터도 사라집니다
