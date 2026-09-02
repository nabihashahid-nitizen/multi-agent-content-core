# Multi-Agent Content Core Automation Engine

An autonomous, multi-agent AI content production pipeline built in n8n that turns a single topic brief into a publication-ready content package using free-tier tools (Google Gemini & Tavily Web Search).

## 📌 Project Overview
This workflow automates end-to-end content creation. By triggering a simple form, a chain of specialized AI agents performs live web research, builds SEO outlines, writes and edits articles, generates promotional social copy, and logs the full package to Google Sheets and Slack.

**Execution Pipeline:**  
`Form Input` → `Normalize` → `Tavily Web Search` → `Research Agent` → `Outline & SEO Agent` → `Writer Agent` → `Editor Agent` → `LinkedIn Post Agent` → `Image Prompt Gen` → `Slack Preview` → `Google Sheets Logging` → `Slack Notification`

---

## 🔥 Key Features & Multi-Agent Architecture
* **Live Data Grounding:** Integrates **Tavily API** for real-time web search to ensure content accuracy and up-to-date sources.
* **Specialized Multi-Agent Chain:** Uses **Google Gemini** across 7 dedicated agent nodes:
  * **Research Agent:** Summarizes live search results into structured insights.
  * **Outline & SEO Agent:** Generates targeted headings and keyword structures.
  * **Writer Agent:** Drafts full-length articles based on grounded research.
  * **Editor & Quality Agent:** Evaluates draft quality and assigns a 1–10 quality score.
  * **LinkedIn Post Agent:** Converts long-form content into tailored social promo posts.
* **Automated Archiving & Alerts:** Logs completed packages to Google Sheets ("Content Army") and sends real-time execution summaries to Slack.
* **Fault-Tolerant Design:** Features built-in retry logic on Gemini nodes to handle API rate limits and transient errors smoothly.

---

## 🛠️ Tech Stack
* **Orchestration:** n8n
* **LLM Engine:** Google Gemini API
* **Search Engine:** Tavily Search API
* **Integrations:** Google Sheets API, Slack API, n8n Forms

---

## 💻 Source Code & Workflow
* Source n8n JSON workflow file is available in [`workflow.json`](./workflow.json).

---

## 📷 Workflow Visuals & Demo

### n8n Multi-Agent Workflow Canvas
![Multi-Agent Content Core Canvas](workflow-canvas.png)

### 🎬 Video Demo
https://drive.google.com/file/d/1rQ9SdKjjed_S2KwOyLSzpE9Obfnr_s9E/view?usp=sharing
