# MeaLit — Personalized Food Recommendation Engine

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![ML](https://img.shields.io/badge/ML-Collaborative_Filtering-138808?style=for-the-badge)](https://github.com/ArjunDeshmukh16/MeaLit)

> A web-based food recommendation engine combining **collaborative filtering** and **content-based machine learning** to deliver personalized restaurant and recipe suggestions — adapting to user preferences and search history in real time.

---

## Overview

MeaLit demonstrates end-to-end ML system design: from data scraping and model training through to a user-facing web application. It uses two complementary recommendation approaches:

| Method | How It Works |
|---|---|
| **Collaborative Filtering** | Finds users with similar taste profiles and surfaces what they liked |
| **Content-Based Filtering** | Matches food attributes (cuisine, ingredients, price range) to user preferences |
| **Hybrid Scoring** | Combines both signals for higher-quality, diverse recommendations |

The system continuously improves as users interact — search history feeds back into the model to refine future suggestions.

---

## Features

- **User authentication** — registration and login with session management
- **Preference quiz** — cuisine, location, and budget inputs to cold-start recommendations
- **Restaurant recommendations** — name, cuisine, location, price range, and ratings
- **Recipe recommendations** — ingredient-based matching with cooking instructions
- **CRUD operations** — save, categorize, and manage favourite restaurants and recipes
- **Search history loop** — past interactions improve future recommendation quality
- **Popular section** — most-liked restaurants and recipes across all users
- **Web scraping pipeline** — live data via Beautiful Soup and Selenium

---

## Getting Started

### Local Setup

```bash
git clone https://github.com/ArjunDeshmukh16/MeaLit.git
cd MeaLit
pip install -r requirements.txt
python app.py
```

Visit `http://localhost:8000/` in your browser.

### Docker

```bash
docker build -t mealit .
docker run -p 8000:8000 mealit
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Front-end | HTML, CSS, Bootstrap, JavaScript |
| Back-end | Python Flask |
| Database | SQLite |
| ML | Collaborative filtering, content-based filtering |
| Scraping | Beautiful Soup, Selenium |
| Containerization | Docker |

---

## Repository Structure

```
├── app.py                  # Flask application entry point
├── models.py               # Database models and ML recommendation logic
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container config
├── MeaLitdb.sqlite3        # SQLite database
├── templates/              # HTML templates (Jinja2)
├── static/                 # CSS, JS, images
├── Scraping/               # Web scraping scripts (Beautiful Soup + Selenium)
└── csv files/              # Training data for recommendation models
```

---

## Why This Is Interesting (ML Perspective)

Building a recommendation system from scratch — without using a pre-built recommendation library — requires:

1. **User-item matrix construction** from scraped restaurant and recipe data
2. **Similarity computation** (cosine similarity for content-based; matrix factorization for collaborative)
3. **Cold-start handling** via the preference quiz (new users have no history)
4. **Feedback loop** — search history updates the user profile vector in real time

This mirrors production ML recommendation systems at scale (Netflix, Spotify, DoorDash).

---

**→ [View Portfolio](https://arjundeshmukh16.github.io) · [LinkedIn](https://linkedin.com/in/arjun-deshmukh1609) · [GitHub](https://github.com/ArjunDeshmukh16)**
