# explain-check

AI와 함께 만든 결과물을 **AI 없이 직접 설명해야 하는 상황**(제출 전 이해도 확인, 후속 서술형, 코드 설명 면접)을 대비하는 에이전트 스킬입니다. Codex와 Claude Code에서 쓸 수 있습니다.

## 하는 일

| 모드 | 언제 | 하는 일 |
|---|---|---|
| `plan` | 설계를 정한 직후 | 나중에 설명해야 할 5가지 질문을 정하고, 예외 테스트와 약점 측정을 작업 계획에 넣습니다 |
| `final` | 제출 직전 | 실제 실행으로 근거를 모아 방어 노트를 만들고, 한 문제씩 퀴즈를 냅니다 |

5가지 질문 유형: 설계 선택 / 검증 범위 / 동작과 예외 / 가장 약한 지점 / AI 협업 판단

## 설치

**Codex**: 프로젝트의 `.agents/skills/` 또는 `~/.agents/skills/`에 `explain-check` 폴더를 넣고 Codex를 재시작합니다.

**Claude Code**: `~/.claude/skills/`에 `explain-check` 폴더를 넣습니다.

## 사용

```
$explain-check plan    # Codex
$explain-check final

/explain-check plan    # Claude Code
/explain-check final
```

기록은 프로젝트 루트의 `EXPLAIN.md` 한 파일에 남습니다.

## License

MIT
