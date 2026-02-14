# 표고모 Web App

GitHub에 그대로 올려도 열리는 정적 웹앱 구조입니다.

## 실행 방법 (로컬)
1. 이 폴더에서 정적 서버 실행
   - Python: `python3 -m http.server 8080`
2. 브라우저에서 `http://localhost:8080/index.html` 접속

## 설정 파일
- 기본(커밋됨): `app.config.js`
- 로컬 비공개(커밋 금지): `app.config.local.js`

`app.config.local.js` 예시:
```js
window.__APP_CONFIG__ = {
  GOOGLE_CLIENT_ID: "...",
  SUPABASE_URL: "...",
  SUPABASE_ANON_KEY: "...",
  SCHOOL_DOMAIN: "onedu.jje.go.kr",
  EMAIL_PREFIX: "ps2",
  ADMIN_CODE: "2026",
  ADMIN_EMAIL: "admin@onedu.jje.go.kr"
};
```

## GitHub 업로드 시
- 업로드 필수: `index.html`, `assets/`, `app.config.js`, `README.md`
- 업로드 금지: `.env`, `app.config.local.js`

## Flask 백엔드 폴더
- `표고모/` 폴더는 별도 백엔드 실험 코드입니다.
- 정적 배포만 할 경우 없어도 앱은 열립니다.
