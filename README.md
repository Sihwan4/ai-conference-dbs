# 🧬 AI Conference DBs (`ai-conference-dbs`)

의학 및 진단검사, 병리학 등 주요 학회에서 발표된 **AI(인공지능) 관련 세션을 수집·분류하고, 웹 브라우저에서 즉시 SQL로 조회할 수 있는 오픈 데이터베이스 프로젝트**입니다.

별도의 백엔드 서버 없이 **GitHub Pages**와 정적 CSV 파일만으로 동작하며, 브라우저 내에서 SQL 쿼리와 실시간 검색/필터링을 지원합니다.

🔗 **Live Demo (웹 뷰어):** [https://sihwan4.github.io/ai-conference-dbs/](https://sihwan4.github.io/ai-conference-dbs/)

---

## ✨ 주요 특징 (Features)

* **Serverless SQL Querying:** [AlaSQL](https://alasql.org/)을 활용해 정적 CSV 데이터를 브라우저 메모리에서 SQL(`SELECT`, `WHERE`, `GROUP BY`, `ORDER BY` 등)로 직접 조회할 수 있습니다.
* **Interactive Data Grid:** [Grid.js](https://gridjs.io/) 기반으로 키워드 실시간 검색, 컬럼별 정렬, 페이지네이션, 컬럼 너비 조절을 지원합니다.
* **체계적인 AI 세션 메타데이터:** 단순 발표 제목뿐만 아니라 AI 관련도(`직접`/`응용`), 세부 분야(`field`), 적용 단계(`stage`), 핵심 요약 및 분류 근거까지 구조화되어 있습니다.
* **간편한 데이터 확장:** `./db/` 디렉토리에 CSV 파일을 추가하거나 업데이트하는 것만으로 데이터베이스를 최신화할 수 있습니다.

---

## 📂 디렉토리 구조 (Directory Structure)

```text
ai-conference-dbs/
├── index.html          # 메인 웹 애플리케이션 (PapaParse + AlaSQL + Grid.js)
├── README.md           # 프로젝트 소개 문서
└── db/                 # 학회 세션 CSV 데이터 보관 폴더
    └── sessions.csv    # 학회 AI 세션 통합/개별 데이터셋
