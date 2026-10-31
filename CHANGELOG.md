# 변경 기록

이 파일에는 이 프로젝트의 주요 변경 사항이 기록됩니다.

형식은 [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)를 따르며,
이 프로젝트는 [Semantic Versioning](https://semver.org/spec/v2.0.0.html)을 준수합니다.

## [미출시]

### 수정됨

- README 토큰 �지를 CI에서 집계해, 오래된 호스팅 집계가 아닌 현재 기본 브랜치를 반영하도록 했습니다.

## [0.6.1] - 2026-10-05

### 변경됨

- 클로닝 가이드를 일반화했습니다. 너비·높이·입력·상태를 바꿔가며 각 관찰을 규칙 샘플로 다루고, 원본의 실제 파일을 사용하며, 관찰된 모든 상태에서 공유 컴포넌트를 만드세요.

## [0.6.0] - 2026-10-05

### 변경됨

- 공유 웹사이트 클로닝 워크플로를 단순화하고, 반응형·모션 안내를 개선했으며, 프로젝트 문서를 정리했습니다.

## [0.5.1] - 2026-09-26

### 변경됨

- README에서 Claude Code + Opus 5.5를 권장합니다
- 정적 Star History 차트를 2026년 9월까지로 갱신했습니다
- README에서 표준 스킬 편집 관련 중복 안내를 제거했습니다

### 보안

- Next.js와 eslint-config-next를 16.3.5로 업데이트하고 버전을 고정했으며, 취약한 전이 의존성을 갱신했습니다. [#117](https://github.com/JCodesMore/ai-website-cloner-template/issues/117)에서 신고하고 [#118](https://github.com/JCodesMore/ai-website-cloner-template/pull/118)에서 수정안을 제안한 @atahan150님께 감사드립니다.

## [0.5.0] - 2026-09-17

### 추가됨

- README에 저장소 순위 �지를 추가했습니다

### 변경됨

- 복사 가능한 에이전트 설정 프롬프트, 템플릿 버튼, 하나의 클로닝 명령어 예시로 빠른 시작을 단순화했습니다
- Claude Code, Codex, Cursor, OpenCode 지원을 `.agents/skills/clone-website/`의 표준 Agent Skill 하나로 통합했습니다
- Claude Code 연동을 가벼운 명령어 브리지로 축소해, 다른 에이전트에 중복 스킬을 만들지 않고 인자를 표준 스킬로 전달합니다
- 웹사이트 살펴보기 가이드를 표준 스킬의 주문형 레퍼런스로 옮겼습니다

### 삭제됨

- 만료된 스폰서 연동
- 일본어·중국어 간체 README. 영어 README가 유일하게 유지되는 진입점입니다
- README의 중복 워크플로 다이어그램
- 지원하지 않거나 중복되는 에이전트 플랫폼용 생성 스킬·지침 사본
- 에이전트 규칙·스킬 동기화 스크립트와 생성 파일 CI 게이트

## [0.4.0] - 2026-08-10

### 추가됨

- 로컬 개발과 다단계 프로덕션 빌드용 Docker 워크플로
- 생성된 워크스페이스 `/clone-website` 스킬을 통한 Kiro 지원
- Roo 슬래시 명령어 브리지를 포함한 Cline·Roo Code용 완성형 워크스페이스 스킬
- 영어 문서와 동일한 온보딩·워크플로 안내를 담은 중국어 간체·일본어 README
- 비공개 취약점 신고 경로를 포함한 기여자·보안 정책
- 생성된 에이전트 규칙·스킬이 원본 파일과 동기화되도록 강제하는 CI
- 모든 README에 간단한 파이프라인 다이어그램과 정적 Star History 차트

### 변경됨

- 프로젝트 Node.js 기준을 로컬 개발, CI, Docker, 기여자 문서 전반에서 24로 올렸습니다
- Next.js를 16.3, React를 19.2.4 및 관련 의존성으로 갱신했습니다
- `/clone-website`가 이후 실행에서도 기존 페이지를 보존하고, 대상마다 라우트·리서치·컴포넌트·에셋·다운로더를 격리하도록 개선했습니다
- 충돌 방지 출력 네임스페이스와 명시적 라우트 검증으로 다중 출처·쿼리/프래그먼트 계획을 개선했습니다
- 템플릿 워크플로, Opus 5 권장, 지원 플랫폼, 커뮤니티 링크 중심으로 README 온보딩을 재설계했습니다
- 최신 플랫폼 스키마와 결정적 출력에 맞게 규칙·스킬 생성기를 강화했습니다

### 수정됨

- 필수 name 누락 수정과 프롬프트 스키마 평탄화로 Gemini CLI 명령어 검증을 고쳤습니다
- Cline·Roo Code 호출, frontmatter, 인자 처리를 수정했습니다
- 생성된 에이전트 규칙의 Next.js 문서 경로 해석을 수정했습니다
- 취약한 프레임워크 의존성과 생성 파일 일관성 검사를 수정했습니다

### 삭제됨

- Aider를 공식 지원 플랫폼 목록에서 제외했습니다. 전체 브라우저·서브에이전트 워크플로를 안정적으로 실행할 수 없기 때문입니다. 일반 프로젝트 컨텍스트 로드용 `.aider.conf.yml`은 그대로 둡니다

### 보안

- GitHub 비공개 취약점 신고를 통한 책임 있는 공개 절차를 문서화했습니다
- 취약한 의존성을 패치된 릴리스로 업데이트했습니다

## [0.3.1] - 2026-03-29

### 수정됨

- CRLF 줄바꿈 때문에 Windows에서 `sync-agent-rules.sh`가 `@file` 가져오기를 해석하지 못하던 문제. 이제 플랫폼 지침 파일에 Inspection Guide 내용이 올바르게 인라인됩니다

## [0.3.0] - 2026-03-29

### 추가됨

- `/clone-website` 다중 URL 지원 — 병렬 처리와 격리된 출력으로 한 번의 명령으로 여러 사이트 복제
- GitHub Actions 기반 CI 품질 게이트 — 모든 푸시·PR마다 lint, typecheck, build 자동 실행
- 로컬 품질 검증을 위한 `npm run typecheck`, `npm run check` 스크립트
- 크로스플랫폼 줄바꿈 정규화용 `.gitattributes`
- 기여자 일관성을 위한 Node.js 20 고정 `.nvmrc`

### 변경됨

- PR 템플릿 간소화 — 중복 체크리스트 항목과 스크린샷 섹션 제거
- 프로젝트 설명·README 개선 — 사용 사례, 제한, 현대적 표현을 명확히 했습니다
- 모든 플랫폼의 문서·에이전트 규칙을 명확하고 일관되게 다듬었습니다
- 안정적인 Windows 동작을 위해 `sync-skills.mjs`의 CRLF 처리를 수정했습니다

### 삭제됨

- README 문서의 오래된 사용 사례

## [0.2.0] - 2026-03-28

### 추가됨

- 다중 플랫폼 AI 에이전트 지원: Claude Code, Codex CLI, OpenCode, GitHub Copilot, Cursor, Windsurf, Gemini CLI, Cline/Roo Code, Continue, Amazon Q, Augment Code, Aider
- 지원 에이전트별 플랫폼 전용 지침 파일과 `/clone-website` 스킬
- AGENTS.md에서 플랫폼 지침 파일을 재생성하는 `scripts/sync-agent-rules.sh`
- 모든 플랫폼에 `/clone-website` 스킬을 재생성하는 `scripts/sync-skills.mjs`
- Gemini CLI 설정용 GEMINI.md
- README의 지원 플랫폼 표
- README의 "다른 플랫폼용 업데이트" 문서 섹션

### 변경됨

- README가 멀티 에이전트 프로젝트를 설명하도록 변경 (Claude Code 권장, 필수 아님)
- 동기화 스크립트 설명을 AGENTS.md에 업데이트

## [0.1.1] - 2026-03-28

### 추가됨

- 버그 신고·기능 요청 이슈 템플릿
- 체크리스트가 있는 Pull Request 템플릿
- Keep a Changelog 형식의 CHANGELOG.md
- Package.json 메타데이터 (설명, 저장소, 홈페이지, 키워드, engines)

### 수정됨

- LICENSE 저작권자를 JCodesMore로 정정했습니다

## [0.1.0] - 2026-03-28

### 추가됨

- Claude Code용 웹사이트 리버스엔지니어링 초기 템플릿 스캐폴드
- 전체 사이트 클로닝 파이프라인용 `/clone-website` 스킬
- `/build-from-spec`, `/customize` 스킬
- git worktree 격리를 적용한 병렬 빌더 에이전트
- 디자인 토큰 추출용 Chrome MCP 연동
- 종합 살펴보기 가이드와 프로젝트 구조 문서
- Next.js 16 + shadcn/ui + Tailwind CSS v4 기반 스캐폴드
- MIT 라이선스
- �지, 데모 섹션, 빠른 시작, 스타 히스토리를 담은 README

[미출시]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.6.1...HEAD
[0.6.1]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.6.0...v0.6.1
[0.6.0]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.5.1...v0.6.0
[0.5.1]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.3.1...v0.4.0
[0.3.1]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.1.1...v0.2.0
[0.1.1]: https://github.com/JCodesMore/ai-website-cloner-template/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/JCodesMore/ai-website-cloner-template/releases/tag/v0.1.0
