# [보고서] AI-Native 개발 프로세스를 위한 Spec Owner 서브에이전트 체계 정의

**작성일:** 2025년 12월 24일
**작성자:** Spec Owner 이은재 (Tony Lee)
**대상:** 개발팀, 디자인팀, 검증팀 및 주요 스테이크홀더

---

## 1. 개요 (Executive Summary)
본 보고서는 쇼피파이(Shopify) 에이전시 환경에서 AI 에이전트(Claude Code)를 활용하여 제품 사양(Spec)의 정밀도를 높이고, 개발 효율을 극대화하기 위한 **'Spec Owner 서브에이전트 체계'**의 도입 및 역할을 정의한다.

## 2. 서브에이전트 도입 배경
기존의 수동 스펙 작성 방식은 기획자의 주관에 따른 논리적 빈틈, 쇼피파이 기술 제약의 미인지, 그리고 불명확한 일정 산출이라는 리스크가 존재했다. 이를 해결하기 위해 Spec Owner의 역할을 5개의 전문화된 서브에이전트로 분리하여 **'설계의 표준화'**를 달성하고자 한다.

---

## 3. 5대 서브에이전트 역할 및 R&R

| 역할군 | 핵심 미션 | 주요 산출물 |
| :--- | :--- | :--- |
| **1. Scope Guard** | 요구사항의 비즈니스 가치 검증 및 구현 범위(Boundary) 확정 | Boundary Definition, Priority Map |
| **2. Shopify Architect** | 쇼피파이 생태계(Metaobjects, API 등) 최적화 데이터 설계 | Data Schema, API Sketch |
| **3. Edge Case Hunter** | 논리적 결함 및 기술적 예외 상황(Failure) 선제적 도출 | Edge Case & Fallback Matrix |
| **4. WBS Orchestrator** | 4대 역할군별 태스크 분할 및 프로젝트 일정 전략 수립 | Project WBS, Milestone Roadmap |
| **5. AC Standardizer** | Verifier를 위한 정량적 합격 기준 및 표준 데이터셋 구축 | AC Checklist, Golden Set |

---

## 4. 에이전트별 상세 직무 정의

### 4.1 Scope Guard (경계 관리)
- **역할:** 고객 요구사항 중 프로젝트 목표(Why)와 일치하지 않는 기능을 필터링한다.
- **기능:** Out-of-Scope 식별, 개발 타당성 검토.

### 4.2 Shopify Schema Architect (데이터 설계)
- **역할:** 요구사항을 쇼피파이 Admin/Storefront API 및 데이터 구조에 매핑한다.
- **기능:** Metafields/Metaobjects 설계, API 호출 한도(Rate Limit) 고려.

### 4.3 Edge Case Hunter (예외 시나리오 분석)
- **역할:** 시스템 장애 및 사용자 오조작 등 발생 가능한 모든 변수를 탐색한다.
- **기능:** 비결정적(AI 등) 기능의 오류 시나리오 도출, Fallback 로직 수립.

### 4.4 WBS Orchestrator (일정 전략)
- **역할:** UI Composer, UI Integrator, Integrator, Verifier에게 최적화된 업무를 배분한다.
- **기능:** 작업 선후 관계(Critical Path) 식별, 작업 단위(Task) 분할.

### 4.5 AC Standardizer (인수 기준 수립)
- **역할:** Verifier가 주관을 배제하고 테스트할 수 있는 정량적 기준을 마련한다.
- **기능:** Pass/Fail 이진 판정 기준 수립, 테스트용 Golden Set 정의.

---

## 5. 기대 효과 (Expected Benefits)
1. **정밀도 향상:** AI의 비판적 분석을 통해 기획 단계에서의 논리적 결함을 90% 이상 사전 차단.
2. **소통 비용 절감:** 명확한 API 스케치와 AC 제공으로 개발 및 검증팀과의 커뮤니케이션 오류 최소화.
3. **일정 가시성 확보:** 촘촘한 WBS 분할을 통해 프로젝트 지연 리스크를 실시간으로 관리.

## 6. 결론 및 향후 계획
본 체계는 `spec-owner-kit` 저장소를 통해 표준 가이드라인으로 배포되며, 향후 실제 프로젝트 데이터를 학습시켜 에이전트의 설계 역량을 지속적으로 고도화할 예정이다.
