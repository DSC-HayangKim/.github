<div align="center">

# 🌉 Patent AI (R&D Bridge)

**"기술과 산업의 골든타임을 잇는 AI 기반 특허 선제적 매칭 플랫폼"**
<br>
<i>Connect patents with industrial needs before they go dormant.</i>

<br>

[![Visit Service](https://img.shields.io/badge/Demo-Visit%20Service-blue?style=for-the-badge&logo=vercel&logoColor=white)](https://귀하의_배포_링크)
[![Presentation](https://img.shields.io/badge/Doc-Presentation-orange?style=for-the-badge&logo=googleslides&logoColor=white)](https://귀하의_발표자료_링크)

</div>

---

## 🧐 Problem Definition: "Prevention, Not Cure"

기존의 기술 이전 방식은 이미 시장 가치를 잃은 오래된 특허(휴면)를 처리하는 데 집중했습니다. 하지만 기업은 **'가장 신선한 최신 기술'**을 원합니다.

저희는 KAIST, 충남대학교, ETRI 등 **총 151개 주요 연구 기관**의 데이터를 분석하여, 문제의 본질을 **'골든타임의 상실'**로 재정의했습니다.

* **Supply (대학/연):** 기술적 전문 용어 사용 (예: "광학 간섭 기반 초정밀 센싱")
* **Demand (기업):** 비즈니스적 니즈 언어 사용 (예: "불량률 0%를 위한 검사 장비")

**Patent AI**는 이 언어 장벽을 허물고, 등록 1년 이내의 최신 특허를 기업에게 선제적으로 제안하여 **휴면 특허 발생 자체를 예방(Prevention)**하는 플랫폼입니다.

---

## 💡 Key Solution: "Golden Time Protected Matching Score (GT-PMS)"

저희는 단순히 유사도만 보는 것이 아니라, 기술의 '신선도(Recency)'를 핵심 가치로 둔 **'골든타임 보호 매칭 스코어'**를 고안했습니다.

$$PMS = (\alpha \cdot S + \beta \cdot N) \times T_{decay}$$

> **1년(12개월)의 골든타임 동안은 가치를 100% 보호하고, 그 이후부터는 시간이 지날수록 점수가 하락하여 '긴급성'을 부여합니다.**

#### **Parameters**
* **$S$ (Similarity):** 기술 적합성
    * 기업의 자연어 니즈와 특허 요약/청구항 간의 벡터 유사도 (Vector Similarity)
* **$N$ (Needs):** 시장 수요 강도
    * 해당 기술 키워드의 시장 트렌드 및 검색량 증가율 반영
* **$T_{decay}$ (Time Decay):** **조건부 시간 감쇠 계수**
    * $t \le 12$ (1년 이내): **1.0 (감점 없음, 골든타임 보호)**
    * $t > 12$ (1년 경과): **$e^{-\lambda(t-12)}$ (지수 함수적 감점 적용)**

저희 플랫폼은 **GT-PMS 점수가 높은 '갓 등록된 우수 특허'**를 기업에게 최우선으로 노출합니다.

---

## 🛠️ Tech Stack & Architecture

최신 웹 기술 트렌드를 선제적으로 도입하여, 성능 최적화와 미래 확장성을 확보했습니다.

### **Frontend (Client)**
> **"Performance & Future-Proofing"**

| Tech | Version | Reason for Adoption |
| :--- | :--- | :--- |
| ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white) | **v16.0** | **App Router & Server Actions**를 활용한 최적의 렌더링 성능 확보 |
| ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) | **v19** | 최신 Hook(`useOptimistic`, `useActionState`)을 활용한 **비동기 상태 관리 고도화** |
| ![Tailwind](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) | **v4.0** | 차세대 **Oxide Engine** 도입으로 빌드 속도 10배 향상 및 CSS 번들 사이즈 최소화 |
| ![Shadcn](https://img.shields.io/badge/Shadcn_UI-000000?style=flat-square&logo=shadcnui&logoColor=white) | **Latest** | Radix UI 기반의 **Accessible(접근성 준수)** 컴포넌트 시스템 구축 |

### **Backend & AI (Server)**
> **"Robustness & Scalability"**

| Tech | Version | Role |
| :--- | :--- | :--- |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) | **v3.13** | 최신 안정 버전을 기반으로 한 **비동기 데이터 처리 및 PMS 알고리즘 연산** |
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
| **[`data-preprocessing`](https://github.com/DSC-HayangKim/data-preprocessing)** | **⚙️ Data Pipeline**<br>151개 대학/연구소 원천 데이터 전처리 파이프라인 | Pandas, NumPy |

---

## 👥 Team

| Role | Name | Responsibilities | GitHub |

| :--- | :--- | :--- | :--- |

| **Lead** | **하태영** | 단절 지수(DI) 알고리즘 설계, 특허 데이터 마이닝, 백엔드 아키텍처 | [@Hottae0](https://github.com/Hottae0) |

| **Frontend** | **황현석** | Next.js 클라이언트 구현, UX/UI 디자인 시스템


---
<div align="center">
  © 2025 Patent AI Project. All Rights Reserved.
</div>
