# 🚧 AI-Powered Community Problem Mapper

An **AI-driven civic issue reporting platform** that allows citizens to report road infrastructure problems using **photos, voice, or text**, while automatically organizing and prioritizing them for government authorities.

The system combines **Computer Vision, NLP, Speech Recognition, and Geospatial Analysis** to transform unstructured citizen reports into structured, actionable complaints.

---

## 🤖 AI/ML Integration

This project demonstrates **real-world deployment of AI models in a civic workflow**.

| AI Module | Model | Purpose |
|----------|------|---------|
| Image Classification | CLIP (ViT-B/32) | Detects issue category from uploaded photo |
| Speech Recognition | Whisper | Converts voice complaints into text |
| Semantic Understanding | Sentence-BERT | Interprets impact from citizen descriptions |
| Duplicate Detection | CLIP Embeddings + Cosine Similarity | Detects visually similar complaints |
| Geospatial Analysis | MongoDB GeoSpatial Queries | Groups complaints within a radius |
| AI Draft Generation | LLaMA3 (Ollama) | Generates formal civic complaint emails |

---

## ⚡ Key Features

### Citizen Portal
- 📸 Report issues with **photo evidence**
- 🎙 Optional **voice description**
- 📍 Automatic **GPS location detection**
- 🧠 AI-based **issue classification**
- 🔁 **Duplicate detection** to prevent spam reports
- 📊 Track complaint status

### Government Portal
- 📥 Smart complaint inbox
- 🗺 Map view of issues
- 📊 Analytics dashboard
- 🧾 AI-generated email drafts
- 🚦 Automatic priority assignment
- 🔒 Status locking after resolution

---

## 🧠 How AI Works

1. Citizen uploads a **photo + optional voice/text**
2. **CLIP** assigns similarity scores to each category  
3. Highest scoring category becomes the **final complaint type**
4. **Whisper** converts voice → text
5. **SBERT** interprets citizen impact
6. System checks for duplicates using:
   - Geo distance
   - Image embedding similarity
7. Complaint becomes either:
   - **New master complaint**, or
   - **Duplicate report of existing issue**

---

## 🛠 Tech Stack

**Frontend**
- React
- Vite
- TailwindCSS
- Leaflet (Map)

**Backend**
- FastAPI
- Python

**Database**
- MongoDB with GeoSpatial indexing

**AI Models**
- CLIP
- Whisper
- Sentence-Transformers
- LLaMA3 (Ollama)

---

## 🚀 Run Locally

### Backend

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

### Frontend
cd frontend
npm install
npm run dev
