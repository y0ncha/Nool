# 🌐 Nool – AI-Integrated Google Dashboard

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Tech Stack](https://img.shields.io/badge/stack-React%20%7C%20FastAPI%20%7C%20LangChain-blue)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

**Nool** is a modular, AI-powered dashboard that unifies your Google services — including Calendar, YouTube, and Drive — into a single intelligent interface. It leverages Google’s Model Context Protocol (MCP) and Discovery API to inject contextual intelligence into your everyday workflows. Designed for modularity, low-cost AI execution, and fast iteration, Nool helps you bring your digital content to life through an intelligent personal assistant.

---

## ✨ Features

-  **Google OAuth2** for secure sign-in and authorization
-  **Google Calendar & YouTube integration** (Drive/Gmail coming soon)
-  **AI agent powered by LangChain + OpenAI**
-  **Modular plugin system** for scalable service expansion
-  **User context memory** via embeddings for personalized responses
-  **Fast, modern stack:** React (TS) frontend + Python FastAPI backend

---

##  Tech Stack

| Layer        | Technology                          |
|-------------|--------------------------------------|
| Frontend     | React, TypeScript, Vite, React Router |
| Backend      | Python, FastAPI, Pydantic           |
| AI Engine    | LangChain, OpenAI API               |
| Authentication | Google OAuth2                     |
| Integrations | Google MCP, Discovery API           |
| Infrastructure | Firebase / Vercel / Railway / GCP |
| Database     | Firestore or Supabase (optional)    |

---

##  MVP Goals

- [x] Google sign-in and token handling
- [x] Display Calendar and YouTube data in dashboard
- [x] Build LangChain-powered assistant over user content
- [ ] Add persistent vector-based memory for personalization
- [ ] Polish plugin system and modular UI

---

##  Project Structure
```
nool/
├── client/                 # React frontend
│   ├── components/         # Shared UI components
│   ├── plugins/            # Calendar, YouTube, Drive plugins
│   └── App.tsx             # Root component
├── server/                 # FastAPI backend
│   ├── routes/             # API endpoints
│   ├── agent/              # LangChain logic
│   └── main.py             # Entry point
└── docs/                   # Architecture, prompts, roadmap
```

---

##  Vision

Nool is not just a dashboard — it's the foundation of an intelligent workspace. As it evolves, Nool will become a self-adapting system that understands user behavior and automates repetitive tasks, offering proactive support across services like Gmail, Drive, and Calendar.
