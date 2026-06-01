# JSON Formatter & Validator

> 붙여넣은 JSON을 **서버로 보내지 않고 브라우저에서만** 포맷·검증·트리 탐색하는 단일 파일 웹 도구.
> A single-file web tool that formats, validates, and explores JSON **entirely in your browser — no upload**.

**no upload · no tracking · no signup** — 입력한 데이터는 어디로도 전송되지 않습니다 / your data never leaves the page.

앰버 CRT 터미널 테마 · 외부 라이브러리 0개 · 정적 호스팅 가능 (단일 `index.html`).

---

## ✨ 기능 / Features

- **Format / Pretty-print** — 들여쓰기 2칸 / 4칸 / 탭 선택
- **Minify** — 모든 공백 제거, 한 줄 압축 (전송·저장용)
- **Validate** — 파싱 실패 시 **줄·칸(Line/Col)** 위치와 메시지 표시, 해당 줄 강조
- **트리 뷰 / Tree view** — 접고 펼 수 있는 재귀 트리, 타입별 색상(문자열·숫자·불리언·null), 키/항목 개수
- **복사 / 다운로드** — 클립보드 복사 + `.json` 파일 다운로드
- **드래그앤드롭** — `.json`/텍스트 파일을 떨어뜨리면 자동 로드·포맷
- **통계 / Stats** — UTF-8 바이트(원본·결과), Minify 절약률 %, 키 개수, 최대 중첩 깊이
- **샘플 로드 / 지우기**, 단축키 `Ctrl/⌘ + Enter`
- 5 MB 입력 가드 + 대용량 결과 경고

## 🔒 프라이버시 / Privacy

모든 파싱·포맷·검증은 **브라우저(JavaScript) 안에서만** 처리됩니다. 회사 API 응답, 고객 정보, 토큰이 섞인 JSON도 안심하고 붙여넣을 수 있습니다 — 업로드도, 추적도, 회원가입도 없습니다.

All parsing, formatting, and validation happen **only in your browser**. Nothing is uploaded, stored, or tracked.

## 🌐 다국어 / Bilingual (KR · EN)

- 우측 상단 **KR / EN** 토글, 선택 언어는 `localStorage`에 저장되어 다음 방문에도 유지
- 라벨·버튼·안내·**에러 메시지**까지 전부 번역
- 기본 언어는 `navigator.language` 기준 자동 감지

## 🔍 SEO

- `title` / `description` / Open Graph / Twitter Card 메타태그
- **JSON-LD 구조화 데이터** (`WebApplication` + `FAQPage`) — 현재 언어에 맞춰 동적 생성
- 소개 글 + FAQ 본문, `canonical` / `og:url` 런타임 자동 주입

## 🚀 사용 / Usage

브라우저에서 [`index.html`](index.html)을 열기만 하면 됩니다. 빌드 도구·서버·설치 불필요.

로컬에서 서버로 띄워 보려면 / To serve locally:

```bash
python -m http.server 8753
# http://localhost:8753
```

## 🛠 기술 / Tech

- 단일 `index.html` (CSS·JS 인라인), 표준 Web API만 사용 — **의존성 0개**
- `JSON.parse` / `JSON.stringify`, `TextEncoder`, `FileReader`, Clipboard API
- 폰트: JetBrains Mono + Gowun Dodum (Google Fonts)
- 정적 호스팅(GitHub Pages, Netlify, Vercel 등)에 그대로 배포 가능

## 📁 구조 / Structure

```
index.html    ← 진입점이자 전체 앱 (단일 파일)
README.md
```

## 🗺 로드맵 / Roadmap (확장)

MVP 이후 확장 후보: JSON Path 추출(`$.a.b[0]`), 트리 검색/필터, JSON ↔ YAML·CSV 변환, 두 JSON diff.

## 📄 License

MIT

---

CODINGNOW · JSON Formatter
