# 직원 분석 (Employee Pulse — 10C Resource Diagnosis)

"직원들이 진짜 필요로 하는 것은 무엇이고, 어디에 자원이 부족한가?"를 진단하는 도구.

---

## FRAMEWORK

Ulrich의 10C 자원 진단 모델 (Ch5, Table 5-2).

Employee Champion 역할의 핵심 도구 — 직원의 요구(Demands)와 자원(Resources)의 균형을 10가지 자원 카테고리로 진단한다.

### Demands vs Resources 원리

Employee Champion은 두 가지 방법으로 직원 기여를 높인다:
1. **요구(Demands)를 줄이거나** — 불필요한 업무, 관료주의 제거
2. **자원(Resources)을 늘리거나** — 아래 10C를 강화

### 10C 자원 목록

| # | 자원 | 핵심 질문 |
|---|------|----------|
| 1 | **Control** | 직원이 업무 방식 의사결정 권한을 보유하는가? |
| 2 | **Commitment** | 열심히 일하게 하는 비전과 방향이 있는가? |
| 3 | **Challenging Work** | 새 기술을 배울 기회가 있는가? |
| 4 | **Collaboration** | 팀으로 목표를 달성하는 환경인가? |
| 5 | **Culture** | 축하, 재미, 개방성 문화가 있는가? |
| 6 | **Compensation** | 성과에 따른 이익 공유가 있는가? |
| 7 | **Communication** | 경영진과 개방적·빈번한 정보 공유가 있는가? |
| 8 | **Concern for Due Process** | 개인 존엄성, 차이 존중이 있는가? |
| 9 | **Computers/Technology** | 업무를 쉽게 하는 기술 접근권이 있는가? |
| 10 | **Competence** | 업무 수행 필요 기술을 보유하는가? |

### 직원 참여 5단계

1. 정보 공유 → 2. 대안 생성 → 3. 권고안 제시 → 4. 결정 동의 → 5. 결과 책임

> 참여 수준이 올라갈수록 요구(demand)가 자원(resource)으로 전환된다

---

## EXECUTE

### 입력 방식 A: 10C 점수 직접 입력

사용자에게 10C 각각에 대해 1~10점으로 평가를 요청한다.

```
아래 10가지 자원에 대해 우리 팀/조직의 현재 수준을 1~10점으로 평가해주세요:

1. Control (자율성): ?
2. Commitment (몰입): ?
3. Challenging Work (성장 기회): ?
4. Collaboration (협업): ?
5. Culture (문화): ?
6. Compensation (보상): ?
7. Communication (소통): ?
8. Concern for Due Process (공정성): ?
9. Computers/Technology (기술 접근): ?
10. Competence (역량): ?
```

### 입력 방식 B: 텍스트 데이터 분석

직원 인터뷰, 설문 결과, 퇴사 면담, Slack 메시지 등 텍스트 데이터를 입력받아 10C에 매핑한다.

각 텍스트에서:
1. 10C 관련 시그널을 추출
2. 해당 C에 매핑
3. 긍정/부정 시그널 분류
4. 종합 점수 추정

### 분석 내용

1. **10C 점수 프로파일** — 전체 패턴 시각화
2. **Demands > Resources 영역** — 직원이 소진되고 있는 영역 식별
3. **클러스터 분석** — 연관된 C끼리 그룹화 (예: Control+Challenging Work = 자율성 클러스터)
4. **개선 우선순위** — 가장 낮은 C부터, 빠르게 개선 가능한 것 우선
5. **액션 제안** — 각 취약 C별 구체적 개선 방안

### 리포트 형식

```markdown
# 직원 자원 진단 (10C) 리포트

**대상:** [팀/조직명]
**날짜:** [YYYY-MM-DD]
**프레임워크:** Ulrich 10C 자원 진단 (Ch5, Table 5-2)

## 10C 점수 프로파일

| # | 자원 | 점수(1~10) | 수준 |
|---|------|-----------|------|
| 1 | Control | | |
| 2 | Commitment | | |
| ... | ... | | |

## Demands > Resources 영역
[직원이 소진되는 영역 + 근거]

## 핵심 발견
- 강점 자원: ...
- 취약 자원: ...
- 연관 패턴: ...

## 권고 액션 (우선순위순)
1. [취약 C] — [구체적 개선 방안]
2. ...
3. ...

## 참여 수준 진단
현재 단계: [5단계 중 몇 단계?]
목표: [다음 단계로 올리려면?]
```

---

## CC-CONCEPT

**연결 개념:** MCP (Model Context Protocol)

> "Employee Champion은 직원의 목소리를 '듣는' 역할이에요. 그런데 목소리가 Slack에도 있고, 설문에도 있고, 메일에도 있죠. MCP는 이 흩어진 채널들을 CC에 연결해서 한 번에 들을 수 있게 해줍니다."

**MCP란:**
- 외부 시스템(Slack, Google Sheets, Notion 등)의 데이터를 CC가 직접 읽을 수 있게 해주는 연결 통로
- 수동으로 복붙하지 않아도, CC가 원본 데이터에 접근

**시각적 설명:**

```
[Slack 채널] ──┐
[설문 결과] ───┤── MCP ──→ CC ──→ 10C 진단 리포트
[퇴사 면담] ───┘
```

**실습 안내:**

> 지금은 텍스트를 직접 붙여넣었지만, MCP를 연결하면 Slack의 특정 채널이나 Google Sheets의 설문 결과를 CC가 자동으로 읽어서 분석할 수 있어요. "우리 회사에서 MCP로 연결하면 좋을 시스템은 뭘까요?"라고 CC에 물어보세요.

---

## 출처

Dave Ulrich, *Human Resource Champions* (1997), Ch5 "Becoming an Employee Champion", Table 5-2 10C 자원 모델.
