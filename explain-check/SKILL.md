---
name: explain-check
description: AI와 함께 만든 결과물을 사람이 직접 설명하고 방어해야 할 때 쓴다. 설계 시작에 "$explain-check plan", 큰 변경 뒤 "check", 제출 직전 "final"로 부른다.
disable-model-invocation: true
---

# explain-check

목표: 사용자가 AI 없이 결과물을 설명하고 방어할 수 있게 한다. 판단은 사용자가, 정리와 근거 연결은 AI가 한다.
사용자의 지시가 이 스킬보다 우선한다. 코드 분량과 단순화 기준은 이 스킬이 정하지 않는다.

모드에 맞는 문서 하나만 읽는다: plan → `references/plan.md`, check → `references/check.md`, final → `references/final.md`.
과제가 반도체 제조·공정·설비·품질 데이터를 직접 다룰 때만 `references/fab-context.md`도 읽는다.

## 공통 원칙

- 기록은 프로젝트 루트의 `EXPLAIN.md` 한 파일에만 한다.
- 사실과 추정을 나눈다. 실행으로 확인한 것에는 근거(명령과 결과)를 붙이고, 아닌 것은 `미검증: (확인 방법)`으로 둔다.
- 사용자가 그대로 말할 수 있는 짧고 쉬운 문장으로 쓴다. 전문 용어는 처음 쓸 때 괄호 안에 쉬운 말로 풀어 쓴다.
- 사용자에게 묻는 것은 각 문서에 **(결정)**으로 표시한 곳뿐이다. 정리한 결과를 먼저 보여주고, 선택지와 추천을 붙여 한 번에 묻는다.
- 그 밖에 모호한 것은 가정을 밝히고 진행한다. 가정은 EXPLAIN.md에 `가정:`으로 남긴다.
