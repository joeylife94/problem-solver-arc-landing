# Proof Assets Pack v1

## 0. Current Portfolio Structure

- **Flagship (provisional):** E-Commerce Scanner
- **Supporting 1:** SeoulGyeol Skin Lab
- **Supporting 2:** Restricted Ops Intake MVP
- **Supporting 3:** Papyr.us
- **Supporting 4:** Interview Copilot

---

## 1. E-Commerce Scanner
**Portfolio Role**  
Flagship Proof Asset

**One-line Definition**  
한국 도매 상품을 기준으로 여러 시장의 가격을 비교하고, 마진 분석과 리포트 생성을 지원하는 스캐너형 운영 도구.

**Problem**  
국가/플랫폼별 가격 비교와 수익성 판단을 수작업으로 하면 느리고, 반복 가능성도 낮고, 판단 근거를 축적하기 어렵다.

**My Role**  
스캔 파이프라인, 마진 분석 흐름, 리포트 출력 구조, 대시보드 모듈을 직접 설계·구현한 시스템 빌더 역할.

**Key Proof Points**
- 비동기 스캔 파이프라인 구조
- YAML 기반 국가/플랫폼 설정 구조
- SQLite 저장 + JSON/Excel/AI 프롬프트 출력 + 대시보드 연결

**Structural Effect / Result**  
수작업 리서치를 반복 가능한 스캔/분석/출력 흐름으로 전환했다.  
외부 비즈니스 KPI는 아직 없지만, 구조적으로는 운영 판단을 더 빠르고 재사용 가능하게 만든 증거가 있다.

**Public Evidence Status**  
Public-Safe: Yes  
사용 가능한 증거: README, CLI/demo commands, repo structure, AI prompt generation flow, dashboard code

**Immediate Next Action**  
대시보드 스크린샷 2장 확보 + 아키텍처 bullet 3개 추출

---

## 2. SeoulGyeol Skin Lab
**Portfolio Role**  
Supporting Proof Asset

**One-line Definition**  
개인정보 보호를 우선하는 다국어 피부 분석 및 리포트 전달 MVP.

**Problem**  
피부 진단/리포트 경험은 종종 판매 유도 중심으로 흐르며, 객관적 흐름과 데이터 처리 방식이 불명확하다.

**My Role**  
프론트엔드 설문 플로우, 점수화 로직, API, 데이터 스키마, 다국어 처리, 이메일 전달까지 포함한 MVP 전반을 설계·구현.

**Key Proof Points**
- 설문 → 분석 → 리포트 전달의 end-to-end 흐름
- deterministic scoring engine
- privacy-aware data/storage + multilingual email flow

**Structural Effect / Result**  
Next.js 기반의 실행 가능한 MVP와 명확한 privacy/report pipeline을 만들었다.  
상용화 성과는 아직 없지만, 제품 방향성과 시스템 구조는 설명 가능하다.

**Public Evidence Status**  
Public-Safe: Yes  
사용 가능한 증거: README, API routes, repo structure, architecture block, local/deploy docs

**Immediate Next Action**  
설문 화면 + 리포트 화면 스크린샷 2장 확보

---

## 3. Restricted Ops Intake MVP
**Portfolio Role**  
Supporting Proof Asset

**One-line Definition**  
승인된 Slack 채널의 운영 요청을 받아 웹 콘솔에서 추적·배정·감사 가능한 형태로 처리하는 내부 운영용 intake MVP.

**Problem**  
운영 요청이 Slack 안에서 흩어지면 누락, 책임 불명확, 감사 이력 부족 문제가 발생한다.

**My Role**  
intake API, workflow UI, governance/control 구조, audit surface를 설계·구현하고 문서화.

**Key Proof Points**
- restricted channel intake enforcement
- signature/replay/dedup 기반 신뢰 체인
- request tracking + audit log + operator flow

**Structural Effect / Result**  
Slack 요청을 단순 메시지에서 추적 가능한 운영 객체로 전환했다.  
로컬 MVP 수준의 흐름은 증명 가능하지만 production maturity는 아직 미검증이다.

**Public Evidence Status**  
Public-Safe: Partial  
사용 가능한 증거: README, demo scripts, API paths, repo structure, Vitest integration tests  
주의사항: workspace/team/channel 식별자는 가려야 함

**Immediate Next Action**  
민감 식별자 제거 후 public-safe 스크린샷 2장 확보

---

## 4. Papyr.us
**Portfolio Role**  
Supporting Technical Proof Asset

**One-line Definition**  
실시간 협업, AI 기능, 팀 격리를 갖춘 Notion-style 협업 위키/문서 플랫폼.

**Problem**  
팀 문서, 작업, 파일, 실시간 협업, AI 기반 지식 활용이 분절되면 생산성과 일관성이 떨어진다.

**My Role**  
프론트엔드, 백엔드, 협업 엔진, AI 기능, 보안, 테스트 전반을 통합한 full-stack/system integration 역할.

**Key Proof Points**
- Yjs + Socket.IO 기반 realtime collaboration
- AI Copilot / search / writing assist
- RBAC + layered architecture + documented test stack

**Structural Effect / Result**  
구현 범위와 기술층이 넓고 테스트 문서화도 강하다.  
다만 실제 사용자 KPI나 운영 성과는 아직 증명되지 않았다.

**Public Evidence Status**  
Public-Safe: Partial  
사용 가능한 증거: README, docs, architecture diagram, repo structure, test scripts  
주의사항: auth/admin/security 관련 세부는 제한적으로 공개해야 함

**Immediate Next Action**  
아키텍처/테스트 증거를 1페이지 proof sheet로 추출

---

## 5. Interview Copilot
**Portfolio Role**  
Supporting Proof Asset (Sensitivity Caution)

**One-line Definition**  
실시간 전사, 번역, 힌트, 분석을 제공하는 인터뷰/미팅 지원 assistant.

**Problem**  
인터뷰나 미팅 중에는 실시간 이해, 기억, 반응 부담이 커서 인지 부하가 높아진다.

**My Role**  
확장 fork의 주요 모듈, Web UI pipeline, integration docs를 포함해 시스템을 유지·확장한 builder/maintainer 역할.

**Key Proof Points**
- local-first end-to-end assistance pipeline
- modular v3.0 expansion structure
- tests/docs/architecture depth

**Structural Effect / Result**  
실행 가능한 시스템 구조와 검증 자산은 존재한다.  
하지만 latency/accuracy KPI와 공개 가능한 demo 범위는 아직 보수적으로 다뤄야 한다.

**Public Evidence Status**  
Public-Safe: Partial  
사용 가능한 증거: README, API docs, architecture docs, tests, repo structure, CLI commands  
주의사항: transcript/conversation/API key 관련 노출 위험 있음

**Immediate Next Action**  
민감 정보 없는 demo-safe Web UI 스크린샷 2장 확보

---

# 2. Packaging Notes

## Flagship Selection Logic
현재 기준에서 대표작은 **E-Commerce Scanner**로 잠정 고정한다.

선정 이유:
- public-safe가 가장 깔끔하다
- 문제 설명이 직관적이다
- 구조 설명이 쉽다
- 랜딩페이지 대표작으로 포장하기 유리하다

## Supporting Logic
- **SeoulGyeol Skin Lab**: 제품형 MVP + privacy framing
- **Restricted Ops Intake MVP**: 운영 통제 구조 증명
- **Papyr.us**: 기술 폭과 협업 구조 증명
- **Interview Copilot**: 실시간 assistant 구조 증명

---