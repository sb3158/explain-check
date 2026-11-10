# explain-check

AI와 함께 만든 결과물을 **AI 없이 직접 설명해야 하는 상황**(제출 전 이해도 확인, 후속 서술형, 코드 설명 면접)을 대비하는 에이전트 스킬입니다. Codex와 Claude Code에서 쓸 수 있습니다.

## 하는 일

| 모드 | 언제 | 하는 일 |
|---|---|---|
| `plan` | 설계를 시작할 때 (인터뷰·합의 후, 코딩 전) | 문제 정의, 성공 기준과 완료 조건, 방식 비교(사용자 선택), 위험(Tiger/Paper/Elephant), 예외, 구조(모듈 지도), 작업 단계, 담당자 확인 질문, 설명 질문을 정리하고, AGENTS.md에 기본 작업 규칙과 check 규칙을 넣습니다 |
| `check` | 큰 변경마다 (자동) | plan이 AGENTS.md에 규칙을 넣어두면 핵심 로직이나 모듈 구성이 바뀔 때마다 자동으로 변경 내용을 설명하고 전후 지표를 비교합니다. 지표가 나빠졌거나 설계와 달라졌을 때만 유지·되돌림을 묻습니다. 직접 불러도 됩니다 |
| `final` | 제출 직전 | 주장마다 근거를 연결하고, 방어 노트를 만들고, 한 문제씩 퀴즈를 냅니다 |

반도체 제조·공정·설비·품질 데이터를 다루는 과제에서만 현업 지표, 오판 비용, 현장 데이터의 함정을 함께 반영합니다.

## 설치

**Codex**: 프로젝트의 `.agents/skills/`에 `explain-check` 폴더를 넣고 Codex를 재시작합니다.

**Claude Code**: `~/.claude/skills/`에 `explain-check` 폴더를 넣습니다.

## 사용

```
$explain-check plan    # Codex
$explain-check check
$explain-check final

/explain-check plan    # Claude Code
/explain-check check
/explain-check final
```

기록은 프로젝트 루트의 `EXPLAIN.md` 한 파일에 남습니다.

터미널을 여러 개 쓸 때: 모든 터미널이 AGENTS.md를 통해 EXPLAIN.md 설계를 따라 구현합니다. EXPLAIN.md는 plan을 실행한 터미널만 고치고, 다른 터미널의 check 결과는 화면에만 보여줍니다(필요하면 plan 터미널에 넘겨 기록). final은 plan을 실행한 터미널에서 부릅니다.

코드 분량과 단순화 기준은 정하지 않으므로, ponytail 같은 코드 단순화 스킬과 함께 써도 겹치지 않습니다.

## License

MIT
