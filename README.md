# ji-report-standards

JRI 정책연구 보고서 작성 표준 (톤·서식·인용)

본 저장소는 여러 보고서 프로젝트에서 공통으로 참조하는 작성 표준을 단일 출처(single source of truth)로 관리함. 인간 작성자와 AI 도구(Claude, ChatGPT, Cursor 등) 모두 동일한 URL을 통해 접근하여 일관된 표준을 적용할 수 있도록 함.

## 빠른 참조 (Raw URL)

* 최신 톤 가이드: <https://raw.githubusercontent.com/z0nam/ji-report-standards/main/tone/latest.md>
* 최신 서식 안내: <https://raw.githubusercontent.com/z0nam/ji-report-standards/main/format/latest.md>
* G-리포트 서식 안내: <https://raw.githubusercontent.com/jeju-inst/ji-report-standards/main/format/g-report/latest.md>
* 최신 인용 표기법: <https://raw.githubusercontent.com/z0nam/ji-report-standards/main/citation/latest.md>

## 구조

```
ji-report-standards/
├── tone/        보고서 본문 톤·bullet 규칙
│   ├── latest.md            → 현재 권장 버전
│   └── YYYY-MM-DD-N.md      → 시점별 동결 버전 (N: 같은 날 연번)
├── format/      장·절 구조, 표·그림 캡션, 서식 docx/hwpx 안내
│   └── g-report/  G-리포트(정책대응 참고자료) 서식 안내
├── citation/    인용 표기법 (제주연구원 인용표기 지침 기반)
└── CHANGELOG.md
```

## 버전 명명 규칙

* 파일명: `YYYY-MM-DD-N.md` (예: `2026-05-11-2.md`)
  * 같은 날 여러 업데이트 시 연번 증가
  * 첫 버전도 `-1`을 명시하여 일관성 유지
* `latest.md`는 항상 최신 버전을 가리킴
* Git tag로 안정 URL 확보 가능
  * 예: `https://raw.githubusercontent.com/z0nam/ji-report-standards/v2026-05-11-2/tone/latest.md`

## 사용 방법

### 인간 작성자

* 브라우저에서 본 README 또는 `tone/latest.md`를 직접 열람
* 보고서 프로젝트에 표준을 복사하지 말고 URL을 참조하도록 권장
  - 프로젝트의 `README.md` 또는 작성 가이드 문서에 본 저장소 URL과 적용 버전(예: `2026-05-11`)을 명시함

### AI 도구

* WebFetch / fetch 도구로 raw URL을 호출하여 가이드 본문을 수신
* 프로젝트별 `CLAUDE.md`, `AGENTS.md`, `.cursorrules` 등에 본 저장소 URL을 참조로 명시
  - 예: "톤·서식은 <https://raw.githubusercontent.com/z0nam/ji-report-standards/main/tone/latest.md> 를 따른다"

### 버전 고정

* 보고서 작성 중간에 가이드가 변경되어도 영향받지 않으려면 `latest.md` 대신 시점별 동결 파일(`2026-05-11.md`)을 참조함
* 보고서 최종본에는 적용한 표준 버전(파일명 또는 commit hash)을 기재 권장

## 변경 절차

* 표준 변경은 PR(Pull Request)로 제안
* 변경 시 `CHANGELOG.md` 갱신과 새 시점 파일 생성을 함께 수행
* `latest.md`는 최신 시점 파일과 동기화 (심볼릭 링크 또는 자동 동기)

## 라이선스

* 본 저장소의 표준 문서는 사내·협업 작성자가 자유롭게 참조·복제·수정할 수 있음
* 외부 인용 시 출처 명시 권장
