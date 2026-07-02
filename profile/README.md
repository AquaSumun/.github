<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=220&section=header&text=AquaSumun&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=AI-Powered%20Water%20Quality%20Management%20Platform&descSize=18&descAlignY=60" />

<br/>

<p>
  <img src="https://img.shields.io/badge/2026-AX%20경진대회-00BFA6?style=for-the-badge" />
  <img src="https://img.shields.io/badge/공공데이터-한국환경공단-6366F1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge" />
</p>

</div>

<br/>

## 🌊 About AquaSumun

> **AquaSumun**은 공공하수처리시설의 수질 데이터를 AI로 분석하는 관제 플랫폼입니다.  
> 한국환경공단 공공데이터(data.go.kr) 기반으로 **15,022개 시설**의 이상 감지·예측·자동 진단을 지원합니다.

**2026 AX 아이디어 경진대회** — 데이터 활용 제품·서비스(앱/AI Agent) 개발 본선 진출작

<br/>

## 🎯 핵심 기능

| 기능 | 설명 |
| :--- | :--- |
| 🤖 **AI 에이전트** | Observe → Detect → Diagnose → Recommend 자율 진단 루프 |
| 📈 **수질 예측** | BOD/TN/TP 48시간 AI 예측 + 신뢰 구간 시각화 |
| 🔍 **XAI 설명** | SHAP 피처 기여도로 예측 근거 투명하게 제공 |
| 🚨 **이상 감지** | HGB + IsolationForest 앙상블 위험도 실시간 모니터링 |
| 🌧️ **강수·유입부하 분석** | 기상청 API 연동 강수 예보 + 강수 → BOD/TN/TP 유입부하량 산출 |
| 🌿 **조류경보 모니터링** | 국립환경과학원 조류경보제 실시간 측정결과 연동 |
| 🏞️ **하천 수질 현황** | 수질측정망 실시간 API — 상류 하천 수질 컨텍스트 제공 |
| 🗺️ **전국 시설 지도** | Mapbox 기반 시설 위치·위험도·강수 레이어 시각화 |
| 💬 **AI 챗 진단** | RAG + Ollama LLM 기반 시설별 자연어 Q&A |
| 📄 **보고서 자동생성** | 자가측정·일일보고·ESG 보고서 PDF/Excel 자동 생성 |
| 🔔 **알림 전송** | 경보 발생 시 담당자 즉시 통보 (SMS 연동) |

<br/>

## 🧪 기술 스택

#### Frontend
<p>
  <img src="https://img.shields.io/badge/Next.js_16-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS_v4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Zustand_v5-000000?style=flat-square&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Recharts_v3-22B5BF?style=flat-square" />
  <img src="https://img.shields.io/badge/Mapbox_GL-000000?style=flat-square&logo=mapbox&logoColor=white" />
  <img src="https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white" />
</p>

#### Backend & AI / ML
<p>
  <img src="https://img.shields.io/badge/FastAPI_0.3.0-009688?style=flat-square&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
</p>

#### Export & Tools
<p>
  <img src="https://img.shields.io/badge/jsPDF_v4-FF0000?style=flat-square" />
  <img src="https://img.shields.io/badge/ExcelJS-217346?style=flat-square" />
  <img src="https://img.shields.io/badge/html2canvas-FFB800?style=flat-square" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" />
</p>

<br/>

## 🚀 실행 방법

#### 사전 요건
- Node.js 20+
- 백엔드 서버 실행 중 (`http://localhost:8000`) → [aquasumun-backend](../aquasumun-backend)

```bash
# 의존성 설치
npm install

# 개발 서버 시작
npm run dev
# → http://localhost:3000
```

#### 환경변수 (`.env.local`)

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_USE_MOCK=false
```

> `NEXT_PUBLIC_USE_MOCK=true` 로 변경하면 목업 데이터로 백엔드 없이 실행 가능합니다.

<br/>

## 🔑 데모 계정

```yaml
email   : demo@example.com
password: demo123
```

<br/>

## 📂 프로젝트 구조

```bash
src/
├── app/                        # Next.js App Router 페이지
│   ├── login/                  # 로그인
│   ├── map/                    # 전국 시설 지도
│   ├── mypage/                 # 마이페이지
│   └── plants/
│       ├── page.tsx            # 시설 목록
│       └── [id]/               # 시설별 상세
│           ├── dashboard/      # 대시보드 (수질 지표·예측·진단)
│           ├── forecast/       # AI 예측 + SHAP 설명
│           ├── reports/        # 보고서 생성
│           ├── alerts/         # 경보 타임라인
│           ├── chat/           # AI 챗 진단
│           └── notifications/  # 알림 내역
├── features/                   # 기능별 UI 컴포넌트
│   ├── auth/                   # LoginPage · MyPage
│   ├── dashboard/              # DashboardPage · ForecastChart · DiagnosisCard
│   │                           # AgentRunModal · RainfallImpactPanel · WeatherContextPanel
│   ├── forecast/               # ForecastPage · TimeSeriesChart · ShapChart
│   ├── map/                    # MapPage · PlantMap (Mapbox)
│   ├── alerts/                 # AlertsPage · AlertTimeline
│   ├── chat/                   # ChatPage (RAG + LLM)
│   ├── notifications/          # NotificationsPage
│   ├── plants/                 # PlantsListPage · PlantCard
│   └── reports/                # ReportsPage · ReportPreview
├── components/
│   ├── common/                 # Button · Badge · Card · Modal · Skeleton · AquaLogo
│   └── layout/                 # Header · Sidebar
├── api/                        # 백엔드 API 호출 레이어 (index.ts · mock.ts)
├── hooks/                      # useAuth · usePlant · useStream
├── store/                      # Zustand 전역 상태
├── types/                      # TypeScript 인터페이스
├── constants/                  # 방류 기준 등 상수
└── utils/                      # 공통 유틸 · reportPdf
```

<br/>

## 🏗️ 시스템 아키텍처

```mermaid
flowchart TD
    %% ── 개발자 / CI ──────────────────────────────────────
    DEV(["👨‍💻 개발자"])
    DEV -- git push --> GH_FE["GitHub\nAquaSumun/Frontend"]
    DEV -- git push --> GH_BE["GitHub\nAquaSumun/Backend"]

    %% ── 클라이언트 ───────────────────────────────────────
    subgraph CLIENT["🌐 클라이언트 (브라우저)"]
        BROWSER(["Chrome / Firefox / Edge"])
    end

    %% ── 프론트엔드 ───────────────────────────────────────
    subgraph FRONTEND["💚 Frontend  ·  Next.js 16 (App Router)"]
        direction TB
        NEXT["⬛ Next.js 16\nTurbopack · SSR/CSR"]
        ZUSTAND["🗂 Zustand v5\n전역 상태 관리"]
        RECHARTS["📊 Recharts v3\n수질 시각화 · 예측 차트"]
        MAPBOX["🗺️ Mapbox GL\n전국 시설 지도"]
        EXPORT["📄 jsPDF v4 + ExcelJS\nPDF · Excel 보고서"]
        NEXT --- ZUSTAND
        NEXT --- RECHARTS
        NEXT --- MAPBOX
        NEXT --- EXPORT
    end

    %% ── 백엔드 ───────────────────────────────────────────
    subgraph BACKEND["🟠 Backend  ·  FastAPI 0.3.0 + Uvicorn"]
        direction TB
        API["🔶 REST API\n/api/plants · /api/auth"]
        AUTH["🔐 인증\nBearer Token Session"]
        RAG["💬 RAG 진단 엔진\nTF-IDF + Ollama LLM"]
        AGENT["🤖 AI 에이전트\nObserve → Detect\nDiagnose → Recommend"]
        WEATHER["🌧️ 기상 API\n기상청 단기예보"]
        ALGAE["🌿 조류경보 API\n국립환경과학원"]
        RIVER["🏞️ 수질측정망 API\n실시간 하천 수질"]
        API --- AUTH
        API --- RAG
        API --- AGENT
        API --- WEATHER
        API --- ALGAE
        API --- RIVER
    end

    %% ── ML 파이프라인 ────────────────────────────────────
    subgraph ML["🤖 ML Pipeline  ·  aqua_risk (Python)"]
        direction LR
        HGB["📈 HGB\n이상 감지"]
        ISO["🌲 IsolationForest\n이상 감지"]
        ENS["⚡ Ensemble\n위험도 점수"]
        FEAT["🔍 피처 중요도\nXAI · SHAP-like"]
        FORE["📅 Forecast\nBOD/TN/TP 예측"]
        HGB --> ENS
        ISO --> ENS
        ENS --> FEAT
        ENS --> FORE
    end

    %% ── 데이터 ───────────────────────────────────────────
    subgraph DATA["📂 공공 데이터  ·  한국환경공단 (data.go.kr)"]
        direction LR
        CSV["🗄 원본 CSV\n2015 – 2024"]
        PANEL["labeled_panel.csv\n15,022개 시설"]
        SCORES["risk_scores_all.csv\n이상 점수"]
        CSV --> PANEL --> SCORES
    end

    %% ── 연결 ─────────────────────────────────────────────
    GH_FE -. "CI/CD Deploy" .-> FRONTEND
    GH_BE -. "CI/CD Deploy" .-> BACKEND

    BROWSER -- "HTTPS\nrequest / response" --> NEXT
    NEXT -- "REST API\nBearer Token" --> API

    API -- "예측 · 지표 조회" --> ENS
    API -- "피처 중요도" --> FEAT
    API -- "진단 보고서" --> RAG

    DATA --> ML
    ML --> BACKEND
```

<br/>

## 🔭 TMS 연동 확장 로드맵

> 현재 버전은 한국환경공단 **공개 공공데이터(연간 통계 CSV)** 기반 PoC입니다.  
> 아래 로드맵을 통해 **실시간 TMS 센서 데이터** 연동으로 확장 가능합니다.

| 단계 | 내용 | 비고 |
| :---: | :--- | :--- |
| **Phase 1 (현재)** | 한국환경공단 공공데이터(2015–2024) 기반 학습·예측 + 기상/조류/하천 API 연동 | PoC 완료 |
| **Phase 2** | 환경부/환경공단 수질TMS API 협약 체결 | 기관 협약 필요 |
| **Phase 3** | TMS 실시간 측정값(15분 간격) 수신 → 자동 재학습 파이프라인 구축 | 인프라 확장 |
| **Phase 4** | 실측 이상 발생 시 AI 에이전트 자동 경보 → 담당자 즉시 통보 | 현장 적용 |

```
현재 데이터 흐름:
  공공데이터 CSV (연간) → ML 학습 → 예측 API → 대시보드
  기상청 / 국립환경과학원 / 수질측정망 API → 실시간 컨텍스트

TMS 연동 후:
  TMS 센서 (15분 간격) → 스트리밍 수신 → 실시간 이상 감지 → 자동 경보
```

<br/>

## 🤝 개발 방식

```yaml
architecture:
  frontend : "Next.js 16 App Router + Zustand v5"
  backend  : "FastAPI 0.3.0 REST API (Bearer token)"
  ml       : "HGB + IsolationForest Ensemble"
  rag      : "TF-IDF + Ollama LLM (RAG)"
  map      : "Mapbox GL + react-map-gl"

data:
  source   : "한국환경공단 공공하수처리시설 현황 (2015–2024)"
  size     : "15,022개 시설 · 연도별 수질 및 처리 효율"
  forecast : "5,683개 시설 AI 예측 가능 (2년 이상 데이터)"
  external : "기상청 단기예보 · 국립환경과학원 조류경보 · 수질측정망 실시간 API"

roadmap:
  phase2   : "수질TMS 실시간 API 연동 (환경부 협약)"
  phase3   : "15분 간격 센서 데이터 자동 재학습 파이프라인"
  phase4   : "현장 AI 에이전트 자동 경보 시스템"
```

<br/>

## 📬 Contact

<p>
  <a href="mailto:wjdwoals000619@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://github.com/AquaSumun">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

<br/>

<div align="center">

---

<sub>Made with 🌊 by <strong>AquaSumun</strong> · AI for a cleaner water future.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2C5364,50:203A43,100:0F2027&height=120&section=footer" />

</div>
