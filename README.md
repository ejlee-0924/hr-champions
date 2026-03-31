# HR Champions x Claude Code

Dave Ulrich의 **Human Resource Champions** 프레임워크를 Claude Code로 실행하는 HR 실무 도구 스킬.

책을 몰라도 됩니다. 각 도구가 프레임워크를 내장하고 있어서, 업무 상황에 맞는 키워드만 입력하면 바로 실행됩니다.

## Quick Start

```bash
npx skills add ejlee-0924/cc-tutor-hr-champions
```

Claude Code에서 아래처럼 사용하세요:

```
조직 진단해줘
프로세스 개선해줘
직원 분석해줘
변화관리 점검해줘
```

## 도구 목록

| 도구 | 하는 일 | Ulrich 원전 | CC 개념 |
|------|---------|------------|---------|
| **HR 역할 진단** | 40문항으로 4역할 강약점 진단 | Ch2 Role-Assessment | 프롬프팅 기초 |
| **조직 진단** | 조직 아키텍처 6요소 분석 | Ch3 Strategic Partner | CLAUDE.md |
| **프로세스 개선** | HR 프로세스 리엔지니어링 | Ch4 Admin Expert | Skill |
| **직원 분석** | 10C 자원 진단으로 직원 니즈 파악 | Ch5 Employee Champion | MCP |
| **변화관리** | 변화 성공 7요인 다중 관점 분석 | Ch6 Change Agent | Subagent/Team |

## 2가지 모드

### 실무 모드 (기본)

개별 도구를 독립적으로 사용합니다. "조직 진단해줘"처럼 업무 상황에 맞게 호출하세요.

### 워크샵 모드

"워크샵 시작"을 입력하면 가상 기업 케이스 시연 → 본인 회사 적용 순서로 4개 도구를 순차 진행합니다. HR Champions x Claude Code 워크샵 퍼실리테이션에 사용하세요.

## 학술적 근거

모든 도구는 아래 원전의 프레임워크를 기반으로 합니다:

> Dave Ulrich, *Human Resource Champions: The Next Agenda for Adding Value and Delivering Results* (1997), Harvard Business School Press.

## 관련 프로젝트

| 대상 | 저장소 |
|------|--------|
| 기업교육 컨설턴트 | [cc-tutor-b2b](https://github.com/ejlee-0924/cc-tutor-b2b) |
| HR 채용 담당자 | [cc-tutor-hr](https://github.com/ejlee-0924/cc-tutor-hr) |
| B2B 마케터 | [cc-tutor-marketing](https://github.com/ejlee-0924/cc-tutor-marketing) |
| **HR/HRD 실무자** | 이 저장소 |

## 라이선스

MIT
