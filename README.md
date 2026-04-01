# HR Champions — HR 실무 AI 도구 모음

Dave Ulrich의 **Human Resource Champions**(1997) 프레임워크를 Claude Code로 실행하는 6개 실무 도구.

책을 몰라도 됩니다. 각 도구가 프레임워크를 내장하고 있어서, 업무 상황에 맞는 키워드만 입력하면 바로 실행됩니다.

## 도구 목록

### Skills (5개) — 설치 필요

| # | 파일 | 하는 일 | 소환 키워드 |
|---|------|---------|-----------|
| 1 | **hr-role-checkup.skill** | 40문항으로 HR 4역할 강약점 진단 | "HR 역할 진단", "40문항" |
| 2 | **org-diagnosis.skill** | 조직 아키텍처 6요소 전략 실행력 진단 | "조직 진단", "조직 분석" |
| 3 | **process-reengineering.skill** | HR 프로세스 리엔지니어링 6단계 + 자동화 실행 | "프로세스 개선", "리엔지니어링" |
| 4 | **employee-pulse.skill** | 10C 자원 모델로 직원 니즈 진단 (AI 시대 업데이트) | "직원 분석", "몰입 진단" |
| 5 | **change-readiness.skill** | 변화 성공 7요인 + AI 도입 특화 렌즈 | "변화관리", "변화 준비도" |
| 6 | **hr-for-hr.skill** | HR팀 자체 진단 — AI 시대 준비도 | "HR 자가진단", "HR for HR" |

### 문서

- **QUICK_START.md** — 5분 시작 가이드 + 실전 시나리오 (먼저 읽으세요!)
- **README.md** — 전체 설명

## 빠른 시작 (3단계)

### 1. 설치 (2분)

Claude Code Settings → Skills → 6개 .skill 파일 업로드

**최소 설치:** 2개만 (`hr-role-checkup` + 관심 도구 1개)

> **AI 시대에 이 책이 더 필요한 이유:** Ulrich는 1997년에 "HR은 활동(Doable)이 아니라 산출물(Deliverable)로 측정받아야 한다"고 했습니다. 27년간 많은 HR이 이걸 알면서도 실행 못 한 이유는 도구가 없었기 때문입니다. AI가 그 도구를 줬습니다.

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

## 이런 상황에서 쓰세요

| 상황 | 소환 키워드 | 결과 |
|------|-----------|------|
| 내일 CEO 보고인데 데이터 없다 | "조직 진단해줘" | 6요소 진단 슬라이드 |
| 퇴사자가 또 나왔는데 원인 모름 | "직원 분석해줘" + 면담 기록 붙여넣기 | 10C 근본 원인 + 액션 |
| AI 도입하라는데 어디서부터? | "변화관리 점검해줘" | 7요인 + AI 특화 렌즈 + 실패 패턴 경고 |
| 채용이 너무 느리다고 불만 | "프로세스 개선해줘" | As-Is/Should-Be + ROI + 자동화 실행 |
| HR이 행정만 한다는 피드백 | "HR 자가진단해줘" | 역량 진단 + AI 준비도 + 90일 플랜 |
| 내 HR 커리어 방향 고민 | "내 역할 진단해줘" | 4역할 강약점 + 개발 방향 |
| M&A 후 조직 통합 | 3개 도구 연쇄 사용 | 양사 비교 진단 + 통합 변화관리 |
| 연간 HR 전략 수립 | 6개 전체 풀사이클 | 종합 HR 전략 보고서 |

## 사용 패턴

| 패턴 | 설명 |
|------|------|
| **단발 소환** | 특정 상황에서 1개 도구만 — 대부분의 일상 사용 |
| **연쇄 소환** | 하나의 결과가 다음 도구를 트리거 — 역할 진단 → 약한 역할 도구 |
| **풀사이클** | 6개 전체를 체계적으로 — 연간 전략, M&A 통합 |

## 아웃풋 형태

모든 도구는 마크다운 리포트를 자동 생성한 후, 추가 시각화를 선택할 수 있습니다:

| 형태 | 용도 |
|------|------|
| **HTML 대시보드** | 인터랙티브 차트 + 탭 — 혼자 깊이 분석할 때 |
| **HTML 슬라이드** | 화살표로 넘기는 발표용 — 경영진 보고할 때 |
| **HTML 1-pager** | 한 장 요약 — 빠른 의사결정이 필요할 때 |

## 학술적 근거

모든 도구는 아래 원전의 프레임워크를 기반으로 합니다:

> Dave Ulrich, *Human Resource Champions: The Next Agenda for Adding Value and Delivering Results* (1997), Harvard Business School Press.

## 관련 프로젝트

| 대상 | 저장소 | 성격 |
|------|--------|------|
| **HR/HRD 실무 도구** | 이 저장소 | .skill 파일 모음 — 현업에서 바로 사용 |

## 면책 조항 (Disclaimer)

이 프로젝트는 Dave Ulrich의 *Human Resource Champions: The Next Agenda for Adding Value and Delivering Results* (1997, Harvard Business School Press)에서 소개된 프레임워크에 기반한 독립적 도구입니다. 원저작자 및 Harvard Business School Press와는 무관하며, 공식적으로 승인·보증받은 프로젝트가 아닙니다. 원전의 프레임워크 개념을 참조하여 AI 시대 HR 실무에 적용한 독창적 저작물입니다.

## 라이선스

MIT
