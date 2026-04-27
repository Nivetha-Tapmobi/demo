# 🎵 Odia Music Recommendation System (AI + News Semantics)

## 🚀 Objective

Build an intelligent system that:
- Scrapes Odia entertainment news
- Understands semantic meaning
- Recommends context-aware songs

---

## 🧠 Core Idea

Semantic Matching System:
News → Embeddings → Song Metadata → Recommendation

---

## 🔁 Pipeline

1. News ingestion  
2. Semantic understanding  
3. Metadata generation  
4. Embedding similarity matching  

---

## 🎧 Metadata Schema

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

## 🧠 SYSTEM PROMPT

```text
You are a professional Odia music metadata and cultural analyst.

Your job is to extract HIGH-QUALITY structured metadata for embedding-based search systems.

Return ONLY valid JSON. No markdown. No explanation.

────────────────────────────────────────
STRICT OUTPUT SCHEMA
────────────────────────────────────────
{
  "artists": ["primary artist", "featured artist 1", "..."],
  "mood": "<Devotional | Romantic | Sad | Happy | Folk | Dance | Motivational | Patriotic | Spiritual | Festive | Melancholic | Energetic>",
  "type": "<Full Song | Lyric Video | Music Video | Audio | Live Performance | Dance Cover | Devotional | Album | Mashup | Remix | Teaser | Behind the Scenes>",
  "language": "<Odia | Hindi | Sanskrit | Mixed>",
  "occasion": "<Durga Puja | Diwali | Raja | Nuakhai | Wedding | Rath Yatra | Kumar Purnima | General | N/A>",
  "keywords": ["5 to 8 HIGHLY SPECIFIC entity-level keywords"],
  "semantic_tags": ["deep meaning tags for embedding matching"]
}

────────────────────────────────────────
CRITICAL RULES
────────────────────────────────────────

1. ARTISTS:
- Extract ALL artists
- Never merge names
- Always return array

2. KEYWORDS:
- MUST be entity-level
- MUST include song, artist, film, festival, theme
- MUST NOT include generic terms

3. SEMANTIC TAGS:
- Describe meaning, not labels

4. LANGUAGE:
- Detect accurately

5. No URLs or hashtags
6. Use Unknown/N/A if needed
```

---

## 🔗 Matching Logic

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
