<div align="center">

# 🏕️ **CampQuest**
### _AI-Powered Enrichment Camp Finder_

> **Discover. Classify. Connect.**  
> AI meets opportunity — helping students find summer and academic programs that match their passions, affordability, and eligibility.

<img src="https://img.shields.io/badge/status-Prototype_v0.9-green?style=for-the-badge&logo=github" />
<img src="https://img.shields.io/badge/platform-Flutter_|_Web-blueviolet?style=for-the-badge&logo=flutter" />
<img src="https://img.shields.io/badge/database-Firebase_|_Supabase-red?style=for-the-badge&logo=firebase" />
<img src="https://img.shields.io/badge/AI-Llama3_|_OpenAI-purple?style=for-the-badge&logo=openai" />

---

 
🌎 **Mission:** Make enrichment opportunities accessible, searchable, and equitable.

</div>

---

## 💡 Vision

> **Equal access to opportunity.**  
> CampQuest bridges AI and education to make every learning opportunity — from MIT to local community colleges — discoverable to all students, regardless of income, gender, or background.

By combining **structured search**, **AI classification**, and **natural-language retrieval**, CampQuest aims to become the national directory for verified enrichment programs — empowering students to explore, compare, and apply confidently.

---

## 🚧 Prototype · v0.9

**Current Dataset:** `967 verified camps`  
**Stage:** Initial prototype — functional scraping and structured database.

### 🧠 Data Pipeline

1. **DuckDuckGo Search API** → Finds official university program URLs.  
2. **BeautifulSoup** → Parses HTML and extracts text fields.  
3. **Llama-3** → Classifies and structures descriptions into labeled attributes.  
4. **Pandas** → Cleans, deduplicates, and merges all data for upload.

### 🗂️ Schema (Current Fields)

| Field | Example | Description |
|--------|----------|-------------|
| **Name** | MIT Beaver Works AI Bootcamp | Program title |
| **Institution** | MIT | Hosting organization |
| **Main Category** | STEM | Broad field |
| **Subject 1 / Subject 2** | AI, Robotics | Specialized focus areas |
| **Dates** | June 15 – July 20, 2025 | Duration |
| **Cost** | $1,500 | Tuition |
| **Eligibility** | Grades 9–12 | Target age/grade range |
| **Selectivity** | High | Admission difficulty |
| **Application Deadline** | March 1, 2025 | Last date to apply |
| **Prerequisites** | Basic Python | Required prior skills |
| **Target Audience** | Women in STEM, low-income students | Intended demographic or access focus |
| **Description** | AI camp combining coding and teamwork | Short summary |
| **URL** | https://beaverworks.mit.edu | Official link |

🗃️ **Storage:**  
Data synced to **Firebase Firestore** for real-time querying and live updates.

---

## 🎯 Next Steps

### 🗺️ **National Data Expansion**
- Add state-based queries for geographic diversity (`"summer camp site:edu California"`, `"AI camp site:edu Texas"`, etc.).  
- Target: **≥20 verified camps per state**.  
- Introduce a `state` field and coordinate mapping (for future visualization).

### 📱 **Mobile App Development (Android & iOS)**
**Framework:** Flutter  
**Backend:** Firebase Firestore + Python Cloud Functions  

**Planned Features**
- 🔍 Search and filter by cost, category, subject  
- 🧭 Offline caching  
- ❤️ Favorite and bookmark camps  
- 🔐 Firebase Auth user login  
- 🔄 Real-time data sync on updates

### 🌐 **Searchable Web App**
**Tech:** Next.js / React + Supabase  
- Fast filters and advanced search  
- Institution & subject-based navigation  
- Mobile-responsive layout  
- Future chatbot preview integration

---

## 🤖 Future Extension · Mini RAG Chatbot

### 🧩 Concept
A **Retrieval-Augmented Generation (RAG)** chatbot that understands natural queries like:  
> “Find affordable AI programs for girls in high school.”  
> “Which camps in Texas offer scholarships?”

### 🧠 Architecture

| Layer | Tool | Purpose |
|--------|------|----------|
| **Semantic DB** | Supabase (PostgreSQL + pgvector) | Vector embeddings + similarity search |
| **Query Parser** | Llama 3 / GPT API | Extracts structured filters |
| **Retriever** | SQL + embeddings | Finds top-matched camps |
| **Generator** | LLM summarization | Writes user-friendly responses |
| **Frontend** | Flutter Chat UI | Interactive chatbot experience |

### ⚙️ RAG Flow
1. Convert user query → embedding  
2. Retrieve top N matching camps via vector similarity  
3. Combine structured filters (`cost < 2000`, `eligibility LIKE '%high school%'`)  
4. Generate answer using Llama-3 / GPT with retrieved context  
5. Display results conversationally with program highlights & links  

**Example Output:**
> “Here are affordable AI camps near Boston:  
> • **MIT Beaver Works AI Bootcamp** ($1500, Grades 9–12, deadline Mar 1)  
> • **BU TechLab Robotics Program** ($900, Grades 9–11)  
> • **Northeastern STEM Scholars** ($1200, Grades 10–12)”

---

## 🧱 Tech Stack Summary

| Category | Tool / Library |
|-----------|----------------|
| **Scraping** | DuckDuckGo API, BeautifulSoup |
| **AI Classification** | Llama 3 |
| **Data Processing** | Pandas |
| **Realtime Database** | Firebase Firestore |
| **Semantic Vector DB** | Supabase (pgvector) |
| **Frontend** | Flutter (mobile), Next.js (web) |
| **LLM API** | OpenAI / Llama 3 |
| **Cloud Functions** | Firebase + Supabase Edge |
| **Analytics/Auth** | Firebase Analytics & Auth |

---

## 🗺️ Roadmap

| Phase | Status | Focus |
|--------|---------|--------|
| **Prototype v0.9** | ✅ | Data pipeline + 967 camps |
| **50-State Coverage** | 🚧 | 1,000–2,000 verified camps |
| **App + Web Interfaces** | 🔜 | Public searchable database |
| **AI Chatbot (RAG)** | 🔮 | Conversational camp recommender |

---

<div align="center">

**Created by [Saanvi](https://github.com/SalmaLilad)**  
🎓 Wayzata High School · Applied AI & Computing Portfolio  

🌐 [Portfolio Website](https://salmalilad.github.io)  
💬 _“Learning should be searchable.”_

</div>

