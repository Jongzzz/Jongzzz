<div align="center">
  <img src="https://komarev.com/ghpvc/?username=Jongzzz&color=blue" alt="Profile Views" />
</div>

<h1 align="center"> Yeom Jong-hwan (염종환)</h1>

<h3 align="center">데이터 품질(Quality)과 무결성을 책임지는 Data Analytics Engineer</h3>
<h4 align="center">한림대학교 AI의료융합전공 주전공 / 빅데이터 복수전공</h4>

<div align="center">
  <a href="#-about-me"><img src="https://img.shields.io/badge/About%20Me-4285F4?style=flat-square&logo=google&logoColor=white"/></a>
  <a href="#-key-skills--tools"><img src="https://img.shields.io/badge/Skills-F4B400?style=flat-square&logo=firebase&logoColor=white"/></a>
  <a href="#-education--certifications"><img src="https://img.shields.io/badge/Education-0F9D58?style=flat-square&logo=whatsapp&logoColor=white"/></a>
  <a href="#-projects-주요-개발-경험"><img src="https://img.shields.io/badge/Projects-9C27B0?style=flat-square&logo=gmail&logoColor=white"/></a>
</div>

---

## 💡 About Me
신뢰할 수 있는 데이터 환경(Single Source of Truth)을 구축하고, 비즈니스 의사결정을 가속화하는 **Data Analytics Engineer**입니다. 

단순히 방대한 데이터를 다루는 것을 넘어, **데이터의 무결성을 검증하고 편향을 제어하는 파이프라인 최적화**에 집착합니다. 6,250만 행 규모의 시공간 데이터 처리(HALO)와 MIMIC-IV 데이터의 결측치 및 불균형 해소 알고리즘(C.O.R.E.)을 직접 설계하며, 고품질의 데이터 거버넌스 환경을 고민해 왔습니다. 데이터 분석과 모델링이 실제 현장(Product)에서 어떻게 쓰이고 어떤 가치를 창출해야 하는지 명확히 이해하는 엔지니어로 기여하고 싶습니다.

- **Domain Interest:** Data Engineering, Data Governance, Machine Learning, Healthcare AI
- **Contact:** [yeomjh926@gmail.com](mailto:yeomjh926@gmail.com)

---

## 🛠️ Key Skills & Tools
데이터 품질 확보와 파이프라인 구축 및 ML 모델링에 필요한 핵심 기술 스택입니다.

<div align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
</div>

**[Data Engineering & DB]**
- **SQL (MySQL):** 복잡한 조인, 윈도우 함수 등을 활용한 데이터 마트(Mart) 설계 및 최적화 쿼리 작성 (SQLD 자격 보유)
- **Python:** 방대한 정형/비정형 데이터 정제, 파이프라인 스크립트 작성 및 자동화 (Pandas, GeoPandas)

**[Machine Learning & Analysis]**
- **Modeling & Optimization:** Scikit-learn, LightGBM, XGBoost, Optuna (클래스 불균형 해소 및 하이퍼파라미터 최적화)
- **Fairness & XAI:** SHAP 기반 예측 근거 시각화, 편향 제어(Reweighting 등)를 통한 해석 가능한 모델링

**[Tools & Statistics]**
- Git, GitHub, SAS, SPSS

---

## 💻 Projects (주요 개발 경험)
방대한 이종 데이터를 가공하고, 데이터 품질(Data Quality)을 확보하여 비즈니스 가치를 도출한 핵심 프로젝트입니다.

### [Data Engineering/ML] HALO: 6,250만 행 규모의 시공간 위험도 예측 패널 구축 (2026.07)
> **🏆 2026 USC Hackathon 1위 (Grand Prize) | 💡 Role: ML Data Engineer**
- **Problem:** 기존 야간 보행 내비게이션은 '최단 시간' 최적화에만 머물러 보행 환경을 반영하지 못함. 짧은 해커톤 기간 내에 5종 이상의 이질적 공공 오픈 데이터(범죄 발생 이력, 가로등 조도 등)를 병합하여 새로운 시공간 데이터 패널을 구축해야 하는 챌린지.
- **Action (Data Engineering & Pipeline):**
  - 19.5만 개의 보행 도로 세그먼트 공간 데이터(GeoPandas)를 기준으로 다차원 데이터 병합(Merge) 및 정제.
  - 실시간 경로 탐색(API) 시 연산 부하를 줄이기 위해, 경로별 4가지 위험 지표(위험도, 조명, 유동 인구, 안전 장소)를 백엔드에서 사전 연산(Pre-compute)하는 아키텍처 설계.
- **Action (Data Quality & Leakage Prevention):**
  - 모델 학습 시 미래 데이터가 참조되는 것을 막기 위해 훈련/예측 기간을 철저히 분리한 '타겟 누수 방지 로직(Leakage-Safe by Design)' 적용.
  - 윤리적 데이터 거버넌스를 위해 취약계층 신고 등 모델을 왜곡하는 신고 데이터를 선별 배제하여 6,250만 행 규모의 거대한 훈련 데이터 마트 완성.
- **Stack:** Python, GeoPandas, SQL

### [Healthcare AI] C.O.R.E CDSS: 응급실 Triage 기반 중증도 분류 예측 모델 파이프라인 (2026.03)
> **🎓 캡스톤 프로젝트 | 💡 Role: Tech Lead & Data Engineer**
- **Problem:** MIMIC 임상 데이터 내 심각한 결측치 존재, 1등급/5등급 환자의 극심한 클래스 불균형으로 인한 모델 붕괴 위험 및 예측 신뢰도 하락.
- **Action (Data Engineering):**
  - 타겟 데이터 누수(Leakage) 원천 차단을 위해, 훈련 세트에만 독립적으로 학습되는 'MICE 기반 커스텀 대치기' 구축.
  - L5 클래스 오버샘플링 및 L3 가중치 신규 추가 등 Optuna 기반의 샘플링 로직 및 손실함수 최적화.
- **Action (XAI & Governance):**
  - 비개발 직군(의료진)도 데이터를 쉽게 해석하고 신뢰할 수 있도록 SHAP 기법을 도입하여 AI의 예측 근거를 시각화한 대시보드 구축.
- **Stack:** Python, XGBoost, Optuna, SHAP

### [Data Analysis] HIRA 의료 빅데이터 기반 정신질환 지원 정책 기획 (2025.08)
> **🏆 2025 HIRA(건강보험심사평가원) 보건의료빅데이터 경진대회 대상 | 💡 Role: Data Analyst**
- **Problem:** 방대하고 파편화된 심평원(HIRA)의 공단 청구 데이터를 비즈니스(정책 지원) 목적에 맞게 구조화하고, 막연한 의료비 지출 문제를 데이터 기반의 구체적인 상관관계로 증명하여 정책 입안자를 설득해야 함.
- **Action & Result:**
  - SQL과 Python을 활용해 수천만 건의 비식별화된 진료 데이터를 추출, 조인, 정제하여 분석 테마에 맞는 정돈된 형태의 데이터 마트로 구조화.
  - 연관 규칙(Association Rule) 알고리즘 및 R 기반 탐색적 데이터 분석(EDA)을 적용하여, 특정 정신질환 환자의 동반 질환 연관성 및 의료비 급증 구간을 수치화.
  - 이를 바탕으로 단순한 재정 지원을 넘어 실효성 있는 맞춤형 금전/비금전적 지원 정책을 성공적으로 도출 및 제안하여 대상 수상.
- **Stack:** SQL, Python, R

**[Additional Projects]**
- 심부전 환자 간 질병수치 상관관계 비교 예측 모델링 (2024.06)
- 문화체육관광부 체육시설 공공데이터 활용 앱 개발 (2024.11)
- 기상(일교차) 데이터와 질병(감기) 내원 환자 분석을 통한 알림 서비스 (2025.06)

---

## 🎓 Education & Certifications
- **한림대학교 (Hallym University)**
  * AI의료융합전공 주전공, 빅데이터 복수전공 (2021.02 - 현재)
  * **학점:** 4.24 / 4.5 (전공: 4.27 / 4.5)
- **Licenses & Certifications:**
  * **빅데이터분석기사** (실무 데이터 핸들링)
  * **SQLD** (데이터베이스 자격증, 2025.08)
  * **ADsP** (데이터분석 준전문가, 2025.02)

---

## 🌍 Experience & Research (경험 및 학술 활동)
| 기관/프로그램 | 역할/내용 | 기간 |
| --- | --- | --- |
| **University of Southern California (USC)** | **글로벌 SW교육프로그램 (LA)**<br>- 데이터 사이언스 및 ML 교육 이수<br>- AI/ML 기반 글로벌 해커톤 프로젝트 수행 | 2026.07 |
| **UMASS Medical School & Harvard** | **글로벌 역량 강화 프로그램 (Boston)**<br>- 대규모 임상 데이터 기반 응급 환자 예측 모델링<br>- **공정성(Fairness) 인지 임상 AI 연구**: 데이터 편향 완화 및 SHAP 검증 | 2026.01 |
| **한림대 춘천성심병원 안과** | **학부 연구원 (Data Researcher)**<br>- EMR 기반 시계열 임상 데이터 추출 및 전처리 파이프라인 경험<br>- 비정형 의료 이미지 데이터 선별 관리 | 2021.07 - 2021.08 |
