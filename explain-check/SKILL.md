---
name: explain-check
description: AI와 함께 만든 결과물을 사람이 직접 설명하고 방어해야 하는 과제용. plan은 설계 직후 설계안·위험·판단 기준을 정리하고 check 규칙을 AGENTS.md에 켜두며, check는 큰 변경마다 변경 내용을 설명하고, final은 제출 직전 근거를 정리하고 퀴즈를 낸다. 사용자가 "$explain-check plan|check|final"로 부를 때만 쓴다.
disable-model-invocation: true
---

# explain-check

목표: 사용자가 AI 없이 결과물을 설명하고 방어할 수 있게 한다. 판단은 사용자가, 정리와 근거 연결은 AI가 한다.

모드에 맞는 문서 하나만 읽는다.
- plan → `references/plan.md`
- check → `references/check.md`
- final → `references/final.md`

과제가 반도체 제조·공정·설비·품질 데이터를 직접 다룰 때만 `references/fab-context.md`도 읽는다. 그 밖의 과제에는 적용하지 않는다.

## 공통 원칙

- 기록은 프로젝트 루트의 `EXPLAIN.md` 한 파일에만 한다.
- 사실과 추정을 나눈다. 실행으로 확인한 것은 근거(명령과 결과)를 붙이고, 아닌 것은 `미검증`으로 표시한다.
- 사용자가 그대로 말할 수 있는 짧고 쉬운 문장으로 쓴다. 전문 용어는 처음 쓸 때 괄호 안에 쉬운 말로 풀어 쓴다.
- 사용자에게 멈춰서 묻는 것은 아래 세 지점뿐이다. 그 밖의 일은 묻지 않고 끝까지 진행한다.
  1. 설계 방식 선택
  2. 위험 대응 결정 (대책을 세울지, 수용할지)
  3. 핵심 로직을 바꿨을 때 유지할지, 되돌릴지
