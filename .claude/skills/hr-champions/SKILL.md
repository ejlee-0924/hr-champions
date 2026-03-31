---
name: hr-champions
description: HR 실무 도구 — 조직 진단, 프로세스 개선, 직원 분석, 변화관리를 Ulrich 프레임워크 + Claude Code로 실행. "조직 진단", "프로세스 개선", "직원 분석", "변화관리", "HR 역할 진단", "hr-champions" 요청에 사용.
---

# HR Champions: HR 실무 AI 도구

Dave Ulrich의 HR Champions 프레임워크를 기반으로, HR 실무 과제를 Claude Code로 즉시 실행하는 스킬.
책을 몰라도 된다 — 각 도구가 프레임워크를 내장하고 있다.

---

## 1. 스킬 모드

이 스킬은 2가지 모드로 동작한다.

### 워크샵 모드

퍼실리테이터가 "워크샵 시작" 또는 "워크샵 모드"를 입력하면 활성화.
가상 기업 A사 케이스 시연 → 본인 회사 적용 순서로 4개 도구를 순차 진행한다.
워크샵 흐름은 `references/case-company-a.md`의 데이터를 사용한다.

진행 순서:
1. HR Champions 소개 (`references/hr-champions-overview.md`)
2. HR 역할 진단 (`references/hr-role-checkup.md`)
3. 조직 진단 (`references/org-diagnosis.md`)
4. 프로세스 개선 (`references/process-reengineering.md`)
5. 직원 분석 (`references/employee-pulse.md`)
6. 변화관리 (`references/change-readiness.md`)

### 실무 모드 (기본)

개별 도구를 독립적으로 사용한다. 아래 트리거 중 하나가 감지되면 해당 레퍼런스를 읽고 실행한다.

---

## 2. 도구 라우팅

| 트리거 키워드 | 레퍼런스 | 하는 일 |
|-------------|---------|---------|
| "HR 역할 진단", "40문항", "내 역할 점검" | `references/hr-role-checkup.md` | Ulrich 40문항으로 4역할 강약점 진단 |
| "조직 진단", "조직 분석", "아키텍처 진단" | `references/org-diagnosis.md` | 조직 아키텍처 6요소 진단 + CLAUDE.md 작성 가이드 |
| "프로세스 개선", "리엔지니어링", "프로세스 분석" | `references/process-reengineering.md` | HR 프로세스 리엔지니어링 6단계 + Skill 자동화 가이드 |
| "직원 분석", "직원 목소리", "몰입 진단", "10C" | `references/employee-pulse.md` | 10C 자원 진단 + MCP 연결 가이드 |
| "변화관리", "변화 진단", "변화 준비도" | `references/change-readiness.md` | 변화 성공 7요인 다중 관점 분석 + Subagent 가이드 |

**트리거가 불명확할 때:**

```
어떤 HR 과제를 다루고 싶으세요?

1. HR 역할 진단 — "나는 어떤 HR 역할이 강한가?"
2. 조직 진단 — "우리 조직의 전략 실행력은?"
3. 프로세스 개선 — "이 HR 프로세스를 어떻게 효율화하지?"
4. 직원 분석 — "직원들이 진짜 필요로 하는 건?"
5. 변화관리 — "이 변화 프로젝트, 성공할 수 있을까?"

번호나 키워드로 선택해주세요.
```

---

## 3. 실행 프로토콜

각 도구는 동일한 3단계로 실행한다:

### Step 1: 프레임워크 안내

해당 레퍼런스의 **FRAMEWORK** 섹션을 읽고:
- 프레임워크의 핵심 개념을 1~2문장으로 설명
- "왜 이 진단이 필요한지" 비즈니스 맥락 제시
- Ulrich 원전 근거 간략 언급

### Step 2: 데이터 수집 + 분석 실행

레퍼런스의 **EXECUTE** 섹션을 읽고:
- 필요한 입력 데이터를 사용자에게 요청
- 데이터를 프레임워크에 대입하여 분석
- 구조화된 리포트 생성

### Step 3: CC 개념 연결 (선택)

레퍼런스의 **CC-CONCEPT** 섹션을 읽고:
- "이 분석을 더 강화하려면?" 으로 CC 개념 소개
- 실습 안내 (CLAUDE.md 작성, Skill 만들기, MCP 연결, Subagent 활용)
- 사용자가 관심 없으면 건너뛴다

---

## 4. 리포트 생성 규칙

모든 분석 리포트는 아래 구조를 따른다:

```markdown
# [도구명] 분석 리포트

**대상:** [회사/팀/프로세스명]
**날짜:** [YYYY-MM-DD]
**프레임워크:** [Ulrich 원전 출처]

## 진단 결과
[프레임워크별 구조화된 분석]

## 핵심 발견
- 강점: ...
- 개선 필요: ...

## 권고 액션 (우선순위순)
1. ...
2. ...
3. ...

## 다음 단계
[연결 가능한 다른 도구 안내]

---
*Powered by HR Champions x Claude Code*
*Framework: Dave Ulrich, Human Resource Champions (1997)*
```

---

## 5. 도구 간 연결

분석 완료 후, 관련 도구를 자연스럽게 안내한다:

| 현재 도구 | 다음 추천 | 연결 논리 |
|----------|----------|----------|
| HR 역할 진단 | 가장 약한 역할의 도구 | "Admin Expert가 약하시네요 → 프로세스 개선 해볼까요?" |
| 조직 진단 | 프로세스 개선 또는 변화관리 | "Governance가 낮으면 → 프로세스 개선, Work Process가 낮으면 → 변화관리" |
| 프로세스 개선 | 직원 분석 | "프로세스 변경이 직원에게 미치는 영향 점검" |
| 직원 분석 | 변화관리 | "직원 니즈를 반영한 변화 계획 수립" |
| 변화관리 | 조직 진단 | "변화 후 조직 상태 재진단" |

---

## 6. 학술적 근거 표기

분석 결과에 Ulrich 원전 근거를 포함할 때:

- 출처: Dave Ulrich, *Human Resource Champions* (1997), Harvard Business School Press
- 챕터와 도구명을 명시: "Ch3 조직 아키텍처 6요소 (Table 3-4)"
- 실증 데이터 인용 시: "12,689명 대상 연구 (Figure 8-4)" 등

허위 인용이나 책에 없는 프레임워크를 Ulrich 것으로 귀속하지 않는다.
