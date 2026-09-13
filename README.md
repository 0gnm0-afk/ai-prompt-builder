# 요청문 빌더 — Prompt Builder Skill

AI에게 시킬 **거친 요청을 잘 짜인 프롬프트로 다듬어 주는** Claude 스킬입니다.

> A Claude skill that turns rough requests into well-structured prompts, using the **GCROUND** framework for text tasks and dedicated checklists for image tasks.

## 무엇을 하나

거친 요청을 주면 작업 종류를 판별하고, 빠진 핵심만 되물은 뒤 **복사해 바로 쓸 프롬프트**를 만들어 줍니다.

| 작업 | 적용하는 틀 |
|---|---|
| 텍스트 (분석·추출·조사·작성·코딩) | **GCROUND** — 목표·배경·자료·조건·출력·불확실성·다음단계 |
| 이미지 분석 (읽기) | 목표·범위·출력·근거·불확실성 + 검수 주의 |
| 이미지 생성/편집 (그리기) | 구성 요소 명시 / '유지할 것' 먼저 + 도구 안내 |

예시는 [`prompt-builder/references/examples.md`](prompt-builder/references/examples.md) 참고.

## 설치 방법 (Claude Code)

이 저장소의 `prompt-builder/` 폴더를 스킬 디렉터리에 복사하면 됩니다.

```bash
# 저장소 클론
git clone https://github.com/0gnm0-afk/ai-prompt-builder.git

# 프로젝트에서 쓰려면
cp -r ai-prompt-builder/prompt-builder .claude/skills/

# 어디서든 쓰려면 (사용자 전역)
cp -r ai-prompt-builder/prompt-builder ~/.claude/skills/
```

설치 후 Claude에게 "이 요청 프롬프트로 다듬어줘" 같이 말하면 자동으로 이 스킬이 적용됩니다.

## 참고

- 스킬은 **Claude 안에서만** 작동합니다. 다른 AI에 붙여넣을 프롬프트를 만드는 데는 쓸 수 있지만, 스킬 자체는 GPT 등에서 실행되지 않습니다.

## 라이선스

MIT

## 저장소 이력

- 최초 저장소 생성일: 2026-07-18 (한국 시간, 기존 GitHub 메타데이터 기준)
- 재등록일: 2026-09-14 (한국 시간)
- 과거에 공개했던 저장소를 개인정보 정리를 위해 삭제한 뒤, 정리한 코드를 새 Git 이력으로 다시 공개했습니다. 기존 커밋·PR 기록은 새 저장소에 포함하지 않았습니다.
