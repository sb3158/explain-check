# explain-check

AI와 함께 만든 결과물을 **AI 없이 직접 설명해야 하는 상황**(제출 전 이해도 확인, 후속 서술형, 코드 설명 면접)을 대비하는 에이전트 스킬입니다. Codex와 Claude Code에서 쓸 수 있습니다.

## 하는 일

| 모드 | 언제 | 하는 일 |
|---|---|---|
| `plan` | 설계 방향을 정한 직후 | 문제 정의, 성공 기준과 완료 조건, 방식 비교, 위험(Tiger/Paper/Elephant), 예외, 담당자 확인 질문, 설명 질문을 정리합니다 |
| `check` | 큰 변경마다 (자동) | plan이 AGENTS.md에 규칙을 넣어두면 큰 변경마다 자동으로 변경 내용을 설명하고, 전후 지표를 비교해 유지·되돌림을 기록합니다. 직접 불러도 됩니다 |
| `final` | 제출 직전 | 주장마다 근거를 연결하고, 방어 노트를 만들고, 한 문제씩 퀴즈를 냅니다 |

반도체 제조·공정·설비·품질 데이터를 다루는 과제에서만 현업 지표, 오판 비용, 현장 데이터의 함정을 함께 반영합니다.

## 설치

**Codex**: 프로젝트의 `.agents/skills/` 또는 `~/.agents/skills/`에 `explain-check` 폴더를 넣고 Codex를 재시작합니다.

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

## License

MIT
