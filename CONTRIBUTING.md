# 기여하기

**AI Website Cloner Template** 개선에 관심을 가져주셔서 감사합니다! 이 가이드는 템플릿 자체에 기여하는 방법을 다룹니다.

> **참고:** 이 저장소는 *템플릿*입니다. 웹사이트를 복제하고 싶다면 여기서 PR을 열지 마세요. **Use this template**을 눌러 직접 사본을 만들고 그곳에서 작업하세요([README](README.md#빠른-시작) 참고). Pull request는 템플릿 개선이어야 합니다: `/clone-website` 스킬, 문서화된 4개 에이전트 지원, 스캐폴드, 또는 문서.

## 기여 방법

- **`/clone-website` 스킬 개선** — 더 정교한 추출, 더 나은 프롬프트, 새로 감지할 동작
- **에이전트 지원 개선** — Claude Code, Codex, Cursor, OpenCode 관련 수정
- **버그 수정** — Next.js 스캐폴드의 버그
- **문서 개선** — README, `AGENTS.md`, 스킬 레퍼런스

[열린 이슈](https://github.com/JCodesMore/ai-website-cloner-template/issues)에서 할 일을 찾아보세요. 규모가 크거나 호환성이 깨질 수 있는 변경은, 본격 작업 전에 이슈를 먼저 열어 방향을 맞추는 것을 권장합니다.

## 개발 환경 설정

**사전 준비물:** [Node.js](https://nodejs.org/) 24 이상.

```bash
git clone https://github.com/YOUR-USERNAME/ai-website-cloner-template.git
cd ai-website-cloner-template
npm ci
```

PR을 열기 전에 프로젝트가 정상 상태인지 확인하세요:

```bash
npm run check   # lint + typecheck + build
```

## 원본 파일

프로젝트 지침은 `AGENTS.md`에 있습니다. 표준 클로닝 워크플로는 `.agents/skills/clone-website/`에 있으며 Codex, Cursor, OpenCode가 직접 읽습니다. Claude Code는 `.claude/commands/clone-website.md`를 통해 진입하며, 이 파일은 두 번째 워크플로 사본이 아닌 가벼운 브리지로 유지되어야 합니다.

표준 스킬과 그 레퍼런스를 직접 수정하세요. 별도의 생성·동기화 단계는 없습니다.

## Pull Request 제출

1. 저장소를 **포크**하고 `master`에서 브랜치를 만드세요 (예: `fix/skill-hover-extraction`, `docs/clarify-setup`).
2. 해당 원본 파일에서 범위를 좁혀 변경하세요.
3. `npm run check`을 실행하고 통과하는지 확인하세요.
4. 변경 내용을 설명하는 명확한 커밋 메시지를 쓰세요. `fix:`, `feat:`, `docs:` 같은 접두사는 환영하지만 필수는 아닙니다.
5. `master` 대상으로 PR을 열고, PR 템플릿을 채운 뒤 관련 이슈가 있으면 연결하세요 (예: `Closes #123`).
6. PR은 작게 유지하세요. 논리적인 변경 하나당 PR 하나가 리뷰·병합하기 훨씬 쉽습니다.

## 질문

[Discord 커뮤니티](https://discord.gg/hrTSX5yTpB)에 물어보세요. 시작을 도와드리겠습니다.
