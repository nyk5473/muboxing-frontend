# MuBoxing 프론트엔드

정적 파일 2개로 구성된 프론트엔드입니다. 별도 빌드 과정이 없습니다.

- `index.html` — 랜딩페이지 (마케팅용 소개 페이지). "시작하기"/"분석 시작" 버튼이 `app.html`로 연결됩니다.
- `app.html` — 실제 5단계(Feeling→Beat→Melody→Structure→Feedback) 언박싱 도구. `muboxing-backend`와 통신합니다.

## 로컬 실행

```bash
python -m http.server 5500
```

그 후 http://127.0.0.1:5500 접속.

## 배포

Render Static Site 등 정적 호스팅에 이 폴더를 그대로 publish directory로 지정하면 됩니다.

`app.html` 안의 `API_BASE` 상수가 백엔드 URL을 가리키므로, 백엔드를 배포한 뒤 그 주소로 값을 바꿔야 합니다:

```js
const API_BASE = 'https://<your-backend>.onrender.com';
```
