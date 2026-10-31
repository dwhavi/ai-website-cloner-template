<div align="center">

# AI Website Cloner Template

### 하나의 명령어로 어떤 웹사이트든 복제하세요

AI 코딩 에이전트에게 URL을 건네면, 깔끔한 Next.js 앱으로 다시 만들어지는 과정을 지켜보세요.

**[Claude Code](https://docs.anthropic.com/en/docs/claude-code) + Opus 5.5 조합에서 가장 좋은 결과를 얻습니다. Codex, Cursor, OpenCode도 지원합니다.**

[![Use this template](https://img.shields.io/badge/Use_this_template-Create_your_copy-2ea44f?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JCodesMore/ai-website-cloner-template/generate) [![Discord](https://img.shields.io/badge/Join_the_community-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/hrTSX5yTpB)

[빠른 시작](#빠른-시작) · [데모 보기](#데모) · [지원 플랫폼](#지원-플랫폼)

<a href="https://github.com/JCodesMore/ai-website-cloner-template/blob/master/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT License" /></a> <a href="https://github.com/JCodesMore/ai-website-cloner-template"><img src="https://img.shields.io/github/stars/JCodesMore/ai-website-cloner-template?style=flat" alt="Stars" /></a> <img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/JCodesMore/ai-website-cloner-template/badges/token-badge.json" alt="tokens" />

  <a href="https://trendshift.io/repositories/24302?utm_source=repository-badge&amp;utm_medium=badge&amp;utm_campaign=badge-repository-24302" target="_blank" rel="noopener noreferrer"><img src="https://trendshift.io/api/badge/repositories/24302" alt="JCodesMore%2Fai-website-cloner-template | Trendshift" width="250" height="55" /></a> <a href="https://www.star-history.com/jcodesmore/ai-website-cloner-template/"><picture><source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/badge?repo=JCodesMore/ai-website-cloner-template&amp;theme=dark" /><source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/badge?repo=JCodesMore/ai-website-cloner-template" /><img alt="Star History Global Rank" src="https://api.star-history.com/badge?repo=JCodesMore/ai-website-cloner-template" width="216" height="55" /></picture></a>

</div>

---

## 데모

[![데모 보기](docs/design-references/comparison.png)](https://youtu.be/O669pVZ_qr0)

> 위 이미지를 클릭하면 YouTube에서 전체 데모를 볼 수 있습니다.

## 빠른 시작

### 1. 프로젝트 준비

**권장 방법: 에이전트에게 시키세요.** 아래 문구를 Codex, Claude Code 또는 사용 중인 코딩 에이전트에 붙여넣으세요:

```text
Set up https://github.com/JCodesMore/ai-website-cloner-template
as a standalone project in a new folder on my computer.
Ask me where to put it. Clone the repository, remove its origin remote,
install dependencies, and run npm run check. Leave it ready for me
to clone a website.
```

**또는 직접 GitHub 저장소를 만드세요:**

[![Use this template](https://img.shields.io/badge/Use_this_template-Create_your_copy-2ea44f?style=for-the-badge&logo=github&logoColor=white)](https://github.com/JCodesMore/ai-website-cloner-template/generate)

이름을 정하고 **Create repository**를 클릭하세요. 그런 다음 새 저장소의 링크를 에이전트에게 주고, 컴퓨터에 복제한 뒤 의존성을 설치하고 `npm run check`를 실행해 달라고 요청하세요.

### 2. 웹사이트 복제

브라우저 접근이 켜진 상태로 에이전트에서 프로젝트를 여세요. Claude Code나 Cursor에서는 다음을 실행합니다:

```text
/clone-website https://example.com
```

URL은 복제하고 싶은 웹사이트 주소로 바꾸세요. 빌드가 끝나면 원하는 변경 사항을 에이전트에게 요청하세요.

## 지원 플랫폼

| 에이전트                                                     | 상태                   |
| ------------------------------------------------------------- | -------------------------- |
| [Claude Code](https://docs.anthropic.com/en/docs/claude-code) | **권장** — Opus 5.5 |
| [Codex CLI](https://github.com/openai/codex)                  | 지원됨                  |
| [OpenCode](https://opencode.ai/)                              | 지원됨                  |
| [Cursor](https://cursor.com/)                                 | 지원됨                  |

## 사전 준비물

- [Node.js](https://nodejs.org/) 24 이상
- AI 코딩 에이전트([지원 플랫폼](#지원-플랫폼) 참고)

## 기술 스택

- **Next.js 16** — App Router, React 19, TypeScript strict
- **shadcn/ui** — 기본 UI 프리미터티브 + Tailwind CSS v4
- **Tailwind CSS v4** — oklch 디자인 토큰
- **Lucide React** — 기본 아이콘(클로닝 과정에서 추출된 SVG로 교체됨)

## 동작 방식

`/clone-website` 스킬은 네 단계로 진행됩니다:

1. **맵(Map)** — 원본 URL을 로컬 라우트에 매핑하고 기존 작업을 보존합니다.
2. **관찰(Observe)** — 데스크톱/모바일 페이지를 살펴보고, 실제 에셋과 폰트를 추출하며, 다양한 상태를 직접 실행해 봅니다.
3. **빌드(Build)** — 편집 가능한 컴포넌트와 동작하는 인터랙션을 구현합니다. 필요하면 독립적인 섹션은 위임합니다.
4. **비교(Compare)** — 원본과 로컬 페이지를 같은 크기/상태에서 검토하고, 보이는 차이를 고친 뒤 프로덕션 검사를 실행합니다.

Framer 페이지와 애니메이션이 많은 사이트에는 반응형 변형, 미디어, 고정(sticky) 장면, 스크롤/시간 기반 모션에 대한 전용 살펴보기 안내가 있습니다. 가능하면 직접 HTTP나 에셋 도구로 추출하고, 브라우저 비교로 모양과 동작을 확정합니다. 산출물에는 라우트 매핑, 실행 방법, 비교 스크린샷, 남은 차이점이 포함됩니다.

## 사용 사례

- **플랫폼 이전** — 직접 소유한 사이트를 WordPress/Webflow/Squarespace에서 현대적인 Next.js 코드베이스로 다시 만듭니다
- **소스 코드 분실** — 사이트는 살아 있는데 저장소가 사라졌거나, 개발자가 떠났거나, 스택이 레거시인 경우. 현대적인 형태로 코드를 되찾습니다
- **학습** — 실제 코드로 작업하면서 프로덕션 사이트가 특정 레이아웃, 애니메이션, 반응형 동작을 어떻게 구현하는지 분해해 봅니다

## 의도되지 않은 용도

- **피싱 또는 사칭** — 기만적 목적, 사칭, 법을 위반하는 활동에는 이 프로젝트를 사용해서는 안 됩니다.
- **타인의 디자인을 자기 것인 양 사용** — 로고, 브랜드 에셋, 원문 카피의 권리는 각 소유자에게 있습니다.
- **이용약관 위반** — 스크래핑이나 복제를 명시적으로 금지하는 사이트도 있습니다. 먼저 확인하세요.

## 프로젝트 구조

```
src/
  app/              # Next.js routes
  components/       # React components
    ui/             # shadcn/ui primitives
    sites/<site>/   # Source-specific components and extracted SVGs
  lib/utils.ts      # cn() utility
  types/            # TypeScript interfaces
  hooks/            # Custom React hooks
public/
  sites/<site>/     # Source-specific images, fonts, videos, and other assets
docs/
  research/<site>/  # Page brief, asset map, and inspection evidence
  design-references/ # Screenshots
.agents/skills/
  clone-website/    # Canonical skill and inspection reference
.claude/commands/
  clone-website.md  # Thin Claude Code bridge
AGENTS.md           # Agent instructions (single source of truth)
CLAUDE.md           # Claude Code config (imports AGENTS.md)
```

## 명령어

```bash
npm run dev    # Start dev server
npm run build  # Production build
npm run lint   # ESLint check
npm run typecheck # TypeScript check
npm run check  # Run lint + typecheck + build
```

### docker를 사용하는 경우

```bash
docker compose up app --build # build and run the app
docker compose up dev --build # run the app in dev mode on port 3001
```

## 에이전트 지원

이 프로젝트는 `.agents/skills/clone-website/`에 이식성 높은 Agent Skill 하나를 유지합니다. Codex, Cursor, OpenCode는 이를 직접 읽습니다. Claude Code는 `.claude/commands/clone-website.md`의 작은 명령어 브리지를 사용하므로, `/clone-website`와 인자가 그대로 동작하면서 다른 에이전트에는 중복 스킬이 노출되지 않습니다.

## 스타 히스토리

![Star History Chart](docs/assets/star-history.png)

## 라이선스

MIT
