<!-- BEGIN:nextjs-agent-rules -->

# 당신이 알던 Next.js가 아닙니다

이 버전에는 브레이킹 체인지가 있습니다. 학습 데이터와 API, 관례, 파일 구조가 모두 다를 수 있습니다. 코드를 작성하기 전에 `node_modules/next/dist/docs/`(이 파일이 있는 디렉터리 기준 경로. 모노레포에서는 루트에서 `next` 패키지가 보이지 않을 수 있음)의 관련 가이드를 먼저 읽으세요. deprecation 안내를 따르세요.

이 블록은 `next dev`가 작성하고 다시 삽입합니다. 자세한 내용은 `node_modules/next/dist/server/lib/generate-agent-files.js`를 확인하세요. diff에서 이 부분을 지워도 커밋되지 않은 변경으로 다시 생겨납니다. 작업물과 함께 커밋하면 트리가 깔끔하게 유지됩니다.

<!-- END:nextjs-agent-rules -->

# 웹사이트 리버스엔지니어링 템플릿

## 개요

AI 코딩 에이전트를 이용해 어떤 웹사이트든 깔끔하고 현대적인 Next.js 코드베이스로 리버스엔지니어링하는 재사용 가능한 템플릿입니다. Next.js + shadcn/ui + Tailwind v4 기반 구조가 미리 갖춰져 있으니, `/clone-website <url1> [<url2> ...]`만 실행하세요.

## 기술 스택

- **프레임워크:** Next.js 16 (App Router, React 19, TypeScript strict)
- **UI:** shadcn/ui (Base UI 프리미터티브, Tailwind CSS v4, `cn()` 유틸리티)
- **아이콘:** Lucide React (기본값 — 추출된 SVG로 교체/보완될 예정)
- **스타일링:** oklch 디자인 토큰을 사용한 Tailwind CSS v4
- **배포:** Vercel

## 명령어

- `npm run dev` — 개발 서버 시작
- `npm run build` — 프로덕션 빌드
- `npm run lint` — ESLint 검사
- `npm run typecheck` — TypeScript 검사
- `npm run check` — lint + typecheck + build 실행

## 코드 스타일

- TypeScript strict 모드, `any` 금지
- Named export, PascalCase 컴포넌트명, camelCase 유틸명
- Tailwind 유틸리티 또는 스코프 CSS 사용. 동적 값이 필요한 경우가 아니면 인라인 스타일 지양
- 2스페이스 들여쓰기
- 반응형: 모바일 우선

## 디자인 원칙

- **픽셀 단위 완벽 재현** — 원본의 간격, 색상, 타이포그래피를 정확히 맞춥니다
- **재현 단계에서는 개인 취향 반영 금지** — 먼저 1:1로 맞추고, 커스터마이즈는 나중에 합니다
- **실제 콘텐츠** — 플레이스홀더가 아닌 대상 사이트의 실제 텍스트와 에셋을 사용합니다
- **아름다움 우선** — 모든 픽셀이 중요합니다

## 프로젝트 구조

```
src/
  app/              # Next.js routes
  components/       # React components
    ui/             # shadcn/ui primitives
    sites/<site>/   # Source-specific components, including extracted SVGs
  lib/
    utils.ts        # cn() utility (shadcn)
  types/            # TypeScript interfaces
  hooks/            # Custom React hooks
public/
  sites/<site>/     # Source-specific images, fonts, video, and other assets
docs/
  research/<site>/  # Page brief, asset map, and inspection evidence
  design-references/ # Screenshots and visual references
scripts/            # Asset download scripts
.agents/
  skills/
    clone-website/  # Canonical cross-agent cloning workflow
.claude/
  commands/
    clone-website.md # Thin Claude Code invocation bridge
```

## 에이전트 워크플로

- 클로닝 워크플로 변경은 `.agents/skills/clone-website/`에서 수정하세요. Codex, Cursor, OpenCode가 사용하는 표준 스킬입니다.
- `.claude/commands/clone-website.md`는 표준 스킬로 연결되는 가벼운 Claude Code 브리지로 유지하세요. 워크플로를 중복해서 넣지 마세요.
