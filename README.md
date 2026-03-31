# HR Champions — HR 실무 AI 도구 모음

Dave Ulrich의 **Human Resource Champions**(1997) 프레임워크를 Claude Code로 실행하는 5개 실무 도구.

책을 몰라도 됩니다. 각 도구가 프레임워크를 내장하고 있어서, 업무 상황에 맞는 키워드만 입력하면 바로 실행됩니다.

## 도구 목록

### Skills (5개) — 설치 필요

| # | 파일 | 하는 일 | 소환 키워드 |
|---|------|---------|-----------|
| 1 | **hr-role-checkup.skill** | 40문항으로 HR 4역할 강약점 진단 | "HR 역할 진단", "40문항" |
| 2 | **org-diagnosis.skill** | 조직 아키텍처 6요소 전략 실행력 진단 | "조직 진단", "조직 분석" |
| 3 | **process-reengineering.skill** | HR 프로세스 리엔지니어링 6단계 분석 | "프로세스 개선", "리엔지니어링" |
| 4 | **employee-pulse.skill** | 10C 자원 모델로 직원 니즈 진단 | "직원 분석", "몰입 진단" |
| 5 | **change-readiness.skill** | 변화 성공 7요인 다중 관점 진단 | "변화관리", "변화 준비도" |

### 문서 (2개)

- **QUICK_START.md** — 5분 시작 가이드 (먼저 읽으세요!)
- **README.md** — 전체 설명

## 빠른 시작 (3단계)

### 1. 설치 (2분)

Claude Code Settings → Skills → 5개 .skill 파일 업로드

**최소 설치:** 2개만 (`hr-role-checkup` + 관심 도구 1개)

### 2. 테스트 (1분)

```
내 HR 역할 진단해줘
```

### 3. 실전 활용

```
"우리 조직 진단해줘"
"채용 프로세스 개선 분석해줘"
"직원 몰입 분석해줘"
"AI 도입 변화관리 점검해줘"
```

## 도구 연결 흐름

```
hr-role-checkup (나의 4역할 진단)
    │
    ├── Strategic Partner 약함 → org-diagnosis
    ├── Admin Expert 약함 → process-reengineering
    ├── Employee Champion 약함 → employee-pulse
    └── Change Agent 약함 → change-readiness
                                    │
                                    ↓
                        (각 도구가 다음 도구를 자연스럽게 추천)
```

## 학술적 근거

모든 도구는 아래 원전의 프레임워크를 기반으로 합니다:

> Dave Ulrich, *Human Resource Champions: The Next Agenda for Adding Value and Delivering Results* (1997), Harvard Business School Press.

## 관련 프로젝트

| 대상 | 저장소 | 성격 |
|------|--------|------|
| **HR/HRD 실무 도구** | 이 저장소 | .skill 파일 모음 — 현업에서 바로 사용 |
| HR Champions로 CC 학습 | [cc-tutor-hr-champions](https://github.com/ejlee-0924/cc-tutor-hr-champions) | 학습 과정 — 워크샵/셀프 학습용 |

## 라이선스

MIT
