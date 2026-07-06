# 👋 Hi, I'm Katherine 

> Full-stack developer · AI/ML enthusiast · Building things that work

---

## 🚀 Featured Projects

### 🤖 [YouTube Title Grader](https://github.com/katherine101001/youtube-title-grader)

**ML-powered YouTube title quality scoring — end-to-end from notebook to production**

```
┌─ Data Pipeline ───────┐   ┌─ ML Engine ────────────┐   ┌─ Serving Layer ────┐
│ 47K+ GB trending      │ → │ XGBoost classifier     │ → │ FastAPI REST API   │
│ videos (Kaggle)       │   │ Macro F1 = 0.704       │   │ /predict /suggest  │
│ Feature engineering   │   │ SHAP explainability    │   │ /keywords          │
└───────────────────────┘   └────────────────────────┘   └────────────────────┘
                                       │
                         ┌─────────────┴─────────────┐
                         │ Streamlit frontend        │
                         │ Score gauge · helps/hurts │
                         │ AI alternatives (Gemini)  │
                         └───────────────────────────┘
```

`Python` `XGBoost` `FastAPI` `Streamlit` `Gemini AI` `SHAP` `Docker` `Render`

**Architecture highlights:**
- **Separation of concerns** — FastAPI backend (`/predict`, `/suggest`, `/keywords`) decoupled from Streamlit UI; each independently deployable
- **Model interpretability** — SHAP values expose *why* a title scores high/low, not just the score; "helps/hurts" breakdown per feature
- **AI-augmented workflow** — Gemini 3.1 Flash Lite generates alternative title suggestions, creating a human-AI feedback loop beyond simple scoring
- **Trained on real-world data** — 47,591 trending YouTube videos (GB region), custom feature engineering pipeline with NLP text metrics
- **Production deployment** — Docker containerization + Render cloud hosting with automated CI/CD from GitHub

---

### 🍔 [团团外卖 · TuanTuan Delivery](https://github.com/katherine101001/tuan-tuan-delivery)

**Zero-infrastructure-cost campus food delivery PWA — production-grade, RM 0/month**

```
┌── Client (PWA) ────────────────────┐   ┌─ Serverless Backend ──────┐
│ Vue 3 Composition API              │   │ Google Apps Script (GAS)  │
│ Service Worker (offline + cache)   │ → │ Google Sheets as DB       │
│ Web Push API (notifications)       │   │ RESTful JSON API          │
│ Installable (Add to Home Screen)   │   │ Cloudflare CDN + DNS      │
└────────────────────────────────────┘   └───────────────────────────┘
```

🔗 **[Live Demo](https://katherine101001.github.io/tuan-tuan-delivery/)**

`Vue 3` `PWA` `Service Worker` `Google Apps Script` `Cloudflare` `GitHub Pages`

**Architecture highlights:**
- **PWA-first architecture** — Service Worker enables offline mode, background sync, and installability; works even on unstable campus WiFi
- **Serverless zero-cost backend** — Google Apps Script handles all API routes with Google Sheets as the datastore; no VPS, no cloud bill, no cold-start issues
- **Real-time without WebSockets** — Smart polling with auto-refresh + Web Audio API alerts; merchants get instant audio notifications for new orders
- **3-role RBAC** — Customer, Merchant, Admin with role-gated views and actions; demo mode (`?demo`) uses localStorage for instant preview without backend
- **Edge-cached delivery** — Cloudflare CDN in front of GitHub Pages; sub-100ms global latency on static assets
- **Progressive enhancement** — works as a basic website, upgrades to installable app with push notifications on supporting browsers

---

### 🏗️ [Project Management System](https://github.com/katherine101001/project-management-system)

**Full-stack enterprise platform — Clean Architecture, C# .NET, containerized microservices**

```
┌──────────────────────────────────────────────────────────┐
│                   Clean Architecture                     │
├────────────┬──────────────┬───────────────┬──────────────┤
│  Domain    │ Application  │Infrastructure │    API       │
│  Entities  │ Use Cases    │ EF Core       │ ASP.NET Core │
│  Value Obj │ DTOs         │ SQL Server    │ RESTful      │
│  Interface │ AutoMapper   │ Repositories  │ Swagger      │
├────────────┴──────────────┴───────────────┴──────────────┤
│              Dependency Inversion (DI)                   │
│  All layers depend inward → Domain has zero dependencies │
└──────────────────────────────────────────────────────────┘
```

`C#` `.NET 9` `EF Core` `React 18` `Redux Toolkit` `Tailwind CSS` `Docker Compose` `GitHub Actions`

**Architecture highlights:**
- **5-layer Clean Architecture** — `Domain` (entities, repository interfaces) → `Application` (DTOs, services, AutoMapper) → `Infrastructure` (EF Core, SQL Server, Mailjet) → `API` (ASP.NET Core controllers, Swagger) → `Shared` (cross-cutting exceptions); inner layers have zero external dependencies
- **Repository + Unit of Work pattern** — 6 repository implementations behind interfaces, enabling testability and future DB swapping without touching business logic
- **SOLID throughout** — Dependency Injection for all services; AutoMapper for object mapping; interface-based design at every boundary
- **React + Redux Toolkit** — Centralized state management with 3 slices (user, projects, theme); role-based protected routes (ADMIN/LEADER/MEMBER) enforced at both frontend router and backend controller levels
- **Real-time collaboration** — Comments with @mentions, Mailjet transactional emails, in-app notification system with read/unread tracking
- **Analytics engine** — Recharts bar/pie visualizations; task completion rate, priority distribution, overdue detection; computed on-the-fly from Redux state
- **DevOps-ready** — Docker Compose multi-container (backend + frontend); GitHub Actions auto-deploy to AWS EC2 on push to main; Swagger auto-generated API docs

---

### 🔗 [Blockchain Supply Chain Traceability](https://github.com/katherine101001/blockchain-supply-chain)

**End-to-end product traceability on Ethereum — FYP**
`FastAPI` `Web3.py` `Solidity` `Flutter` `PostgreSQL`

- Immutable product journey records stored on-chain via smart contracts
- Flutter cross-platform app (Android / iOS / Web / Desktop) with BLoC state management
- SupplyChainRegistry smart contract with filtered trace queries; design system + i18n

---

### 📊 [AI Adoption Frontier — PySpark Analytics](https://github.com/katherine101001/ai-adoption-analysis)

**150K company records · full ML pipeline on distributed Spark**
`PySpark 4.0` `Spark SQL` `MLlib` `Matplotlib` `Seaborn`

- Data profiling → cleaning → feature engineering (9 custom metrics) on 150K records
- KMeans clustering (4 company AI-adoption archetypes), Chi-square statistical testing
- Binary classification: Logistic Regression vs Gradient Boosted Trees on AI tool adoption
- RandomForest regression for AI maturity score prediction
- Spark SQL: CUBE rollups, Window functions (RANK / LAG / rolling averages)

---

### 📱 [Study Crossing · 学霸森友会](https://github.com/katherine101001/study-crossing-android)

**Animal Crossing-themed educational Android game**
`Kotlin` `Android XML` `SQLite` `Gamification`

🔗 **[Demo Video (Google Drive)](https://drive.google.com/drive/folders/13CheMPt1-2ONk62PxLU8EUoKi822PbTU?usp=sharing)**

- 21 screens, 14 quests, 4 mini-game types across English, Math & General Knowledge
- 3 user roles (Student / Teacher / Admin), 7-table SQLite schema, coin economy + badge system
- Slot Machine, Word Track, Fossil Excavation & Multiple Choice game mechanics

---

### 🔧 [OS Thread Synchronization](https://github.com/katherine101001/os-thread-synchronization)

**C pthreads — dynamic producer-consumer with adaptive buffer resizing**
`C` `pthreads` `Semaphore` `Mutex` `POSIX`

- Extended producer-consumer: 5 robot threads + 2 worker threads with dynamic slot management
- Adaptive buffer: auto-expands at 90% occupancy, auto-shrinks at 50% — prevents both overflow and memory waste
- Semaphore + mutex dual-lock synchronization preventing race conditions and deadlocks

---

## 🧠 AI & Machine Learning

### 🖐️ AI Hand Gesture Detection for Robot
**ESP32 edge AI · Real-time rock-paper-scissors robot hand**
`TensorFlow` `ESP32` `Edge AI` `Computer Vision`

🔗 **[Demo (Google Drive)](https://drive.google.com/drive/folders/126jratrKIuIWTJHm4VEP_lD-KLpFd6vG?usp=sharing)**

- Custom image dataset: photographed and labeled hand gestures manually
- Trained CNN → quantized (INT8) for microcontroller deployment on ESP32-CAM
- Real-time inference at the edge — **robot hand always wins**
- Full pipeline: data collection → training → compression → edge deployment

---

### 👁️ Real-Time Object Detection for Visually Impaired
**Distance-aware obstacle detection with adaptive audio feedback**
`TensorFlow` `Computer Vision` `Real-time`

- Real-time object detection from camera feed
- Distance estimation — closer objects trigger **louder / faster audio alerts** (proximity-to-frequency mapping)
- Designed for assistive wearable use case; low-latency inference optimized for mobile

---

## 🎮 Game Development (Unity)

### ⚔️ 2D Platforming RPG
**Level-up action RPG with equipment system**
`Unity` `C#` `2D Game Design`

🔗 **[Gameplay Demo (Google Drive)](https://drive.google.com/drive/folders/1ABr6sw38J0VVHfneg2fHb-smhJQCvNMY?usp=sharing)**

- Side-scrolling platformer with combat mechanics
- Experience & leveling system with stat progression; equipment upgrade tree

---

### 🥽 VR Underwater World
**Immersive ocean exploration in virtual reality**
`Unity` `VR` `3D Environment Design`

🔗 **[VR Demo (Google Drive)](https://drive.google.com/drive/folders/118hCtjrkLvWZzJwutX4XQ9TX-cFLENQ7?usp=sharing)**

- Full underwater ecosystem: coral reefs, marine life, dynamic lighting
- VR headset interaction: explore, observe, interact with sea creatures

---

## 🧪 Testing & QA

### Automated Testing Suite
**End-to-end test automation for web applications**
`Selenium` `JMeter` `Test Automation`

- Automated UI regression tests with Selenium WebDriver
- JMeter load & stress testing; CI-integrated test pipelines

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Languages** | C, Python, Kotlin, C#, Java, JavaScript, Dart, SQL |
| **AI/ML** | PySpark, TensorFlow, XGBoost, scikit-learn, Spark MLlib, SHAP |
| **Backend** | FastAPI, .NET 9, Spring Boot, Google Apps Script, Web3.py |
| **Frontend** | Vue 3, React 18, Flutter, Streamlit, PWA, Tailwind CSS |
| **Mobile** | Android (Kotlin), Flutter |
| **Game Dev** | Unity (2D & VR) |
| **Data** | PostgreSQL, MySQL, SQLite, Google Sheets, PySpark |
| **DevOps** | Docker, GitHub Actions, Render, Cloudflare |
| **Embedded** | ESP32, Edge AI, Model Quantization (INT8) |

---

## 📬 Contact

- 👾 [GitHub](https://github.com/katherine101001)
- 📧 katherinetan1014@gmail.com

---

<p align="center">
  <i>Open to opportunities · Always building</i>
</p>
