<div align="center">

# 🌉 Patent AI (R&D Bridge)

**"기술과 산업의 단절을 잇는 AI 기반 휴면 특허 매칭 플랫폼"**
<br>
<i>Connect dormant patents with industrial needs through Data-Driven Intelligence.</i>

<br>

[![Visit Service](https://img.shields.io/badge/Demo-Visit%20Service-blue?style=for-the-badge&logo=vercel&logoColor=white)](https://귀하의_배포_링크)
[![Presentation](https://img.shields.io/badge/Doc-Presentation-orange?style=for-the-badge&logo=googleslides&logoColor=white)](https://귀하의_발표자료_링크)

</div>

---

## 🧐 Problem Definition: "The Island Effect"

대한민국 대학 및 공공연의 특허 활용률은 33.7%에 불과합니다. 나머지 66%는 연구실 캐비닛 속에 잠들어 있는 '휴면 특허(Dormant Patent)'입니다.

저희는 이 문제의 원인을 물리적 거리가 아닌 '언어와 정보의 단절'로 정의했습니다.
* **대학(Supply):** 기술적 전문 용어 사용 ("광학 간섭 기반 초정밀 센싱")
* **기업(Demand):** 비즈니스적 니즈 언어 사용 ("불량률 0%를 위한 검사 장비")

**Patent AI**는 이 언어 장벽을 허물고, 기업이 필요로 하는 기술을 데이터 기반으로 찾아주는 **수요 견인형(Demand-Driven) 매칭 플랫폼**입니다.

---

## 💡 Key Solution: "Disconnect Index (DI)"

저희는 정성적인 매칭을 넘어, 기술과 산업의 괴리를 수치화한 자체 지표 '단절 지수(Disconnect Index)'를 고안했습니다.

$$DI = 1 - \frac{\text{Realized Value}}{\text{Potential Value}}$$

> **$DI$가 1.0에 가까울수록 기술 잠재력은 높으나 산업적으로 고립된 '고위험 단절' 상태를 의미합니다.**

* **$W_{pot}$ (기술 잠재력):** TRL 단계, 특허 인용 지수, 잔여 수명 기반 평가
* **$W_{rel}$ (산업 연관성):** 지역 주력 산업(반도체, 모빌리티 등) 연관도 분석
* **$A$ (활성화 단계):** 기술이전, 공동연구, NDA 체결 등 '디지털 흔적(Digital Footprint)' 추적

저희 플랫폼은 **DI 지수가 높은 '숨겨진 보석' 같은 특허를 발굴**하여 기업에게 우선적으로 제안합니다.

---

## 🛠️ Tech Stack & Architecture

최신 웹 기술 트렌드를 선제적으로 도입하여, 성능 최적화와 미래 확장성을 확보했습니다.

### **Frontend (Client)**
> **"Performance & Future-Proofing"**

| Tech | Version | Reason for Adoption |
| :--- | :--- | :--- |
| ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white) | **v16.0** | **App Router & Server Actions**를 활용한 최적의 렌더링 성능 확보 |
| ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) | **v19.2** | 최신 Hook(`useOptimistic`, `useActionState`)을 활용한 **비동기 상태 관리 고도화** |
| ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) | **v4.0** | 차세대 **Oxide Engine** 도입으로 빌드 속도 10배 향상 및 CSS 번들 사이즈 최소화 |
| ![Shadcn](https://img.shields.io/badge/Shadcn_UI-000000?style=flat-square&logo=shadcnui&logoColor=white) | **Latest** | Radix UI 기반의 **Accessible(접근성 준수)** 컴포넌트 시스템 구축 |

### **Backend & AI (Server)**
> **"Robustness & Scalability"**

| Tech | Version | Role |
| :--- | :--- | :--- |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) | **v3.13** | 최신 안정 버전을 기반으로 한 **비동기 데이터 처리 및 단절 지수 연산** |
| ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) | **Standard** | **Streaming Response**를 지원하는 고성능 비동기 API 서버 구축 |
| ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) | **Hybrid** | OpenAI(GPT-4o)와 Ollama(Local)를 오가는 **하이브리드 AI 에이전트** 설계 |
| ![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white) | **pgvector** | 정형 데이터(RDB)와 특허 벡터(Vector Store)를 통합 관리하여 **RAG 검색 최적화** |
| ![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) | **Cov 90%+** | Mocking 및 Integration Test를 통한 **엔터프라이즈급 안정성 확보** |

---

## 📂 Repositories

| Repository | Description | Key Tech |
| :--- | :--- | :--- |
| **[`dsc-project-repository`](https://github.com/DSC-HayangKim/dsc-project-repository)** | **🚀 Main Service**<br>통합 웹 애플리케이션 (Frontend & Backend Core) | Next.js, FastAPI |
| **[`vector_vis`](https://github.com/DSC-HayangKim/vector_vis)** | **🧠 AI Engine**<br>특허 데이터 벡터화, 크롤러 및 시각화 엔진 | LangChain, Crawler |
| **[`data-preprocessing`](https://github.com/DSC-HayangKim/data-preprocessing)** | **⚙️ Data Pipeline**<br>KIPRIS/NTIS 원천 데이터 전처리 파이프라인 | Pandas |

---

## 👥 Team

| Role | Name | Responsibilities | GitHub |
| :--- | :--- | :--- | :--- |
| **Lead** | **하태영** | 단절 지수 알고리즘 설계, 특허 데이터 분석, 특허 시각화 맵 제작| [@Hottae0](https://github.com/Hottae0) |
| **AI & Data** | **황현석** | Next.js 아키텍처 설계, UX/UI 구현, 상태 관리 로직| [@Hy3ons](https://github.com/Hy3ons) |

---

<div align="center">
  © 2025 Patent AI Project. All Rights Reserved.
</div>
