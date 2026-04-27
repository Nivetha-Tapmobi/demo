# 🎵 Odia Music Recommendation System (AI + News Semantics)

## 🚀 Objective

Build an intelligent system that:

1. Scrapes **Odia news (media & entertainment)**
2. Understands **semantic meaning of news**
3. Recommends **relevant songs** based on:
   - Person
   - Event
   - Emotion
   - Cultural context

---

## 🧠 Core Idea

We are NOT doing keyword matching.

> **Semantic Matching System (News → Embeddings → Song Metadata → Recommendation)**

---

## 🔁 Pipeline Overview

### 1. 📰 News Ingestion
- Scrape news articles
- Filter entertainment-related content

---

### 2. 🧠 Semantic Understanding
Extract:
- Entities (actors, singers, movies)
- Context (event, celebration, controversy)
- Emotion (happy, sad, tribute)

---

### 3. 🎧 Song Metadata Generation

```json
{
  "artists": [],
  "mood": "",
  "type": "",
  "language": "",
  "occasion": "",
  "keywords": [],
  "semantic_tags": []
}
```

---

## 🎯 Why Metadata Matters

This connects **news → songs**

| News | Song Metadata |
|------|--------------|
| Actor trending | artist |
| Sad news | mood |
| Festival | occasion |

---

## 🔑 Key Fields

### 🎤 Artists
Used for person matching

### 🎭 Mood
Emotion alignment

### 🎪 Occasion
Festival/cultural mapping

### 🧩 Keywords
Entity-level matching

### 🧠 Semantic Tags
Core for embeddings

---

## 🔗 Matching Flow

News → Embedding → Compare → Song Metadata → Recommend

---

## 📦 Input

```json
{
  "video_id": "...",
  "title": "...",
  "description": "...",
  "metatags": "..."
}
```

---

## 📤 Output

```json
{
  "artists": ["..."],
  "mood": "...",
  "type": "...",
  "language": "...",
  "occasion": "...",
  "keywords": ["..."],
  "semantic_tags": ["..."]
}
```

---

## 🧠 Final Goal

Recommend songs based on:
- Emotion
- Context
- Person relevance
