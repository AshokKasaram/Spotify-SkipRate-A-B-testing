# Spotify-SkipRate-A-B-Testing
This project simulates an A/B test to evaluate whether switching from a popularity-based recommender to a collaborative-filtering variant reduces skip rates in algorithmic playlists (e.g., Discover Weekly, Daily Mix).

---

## Goal
Reduce early **skip rate** in algorithmic playlists by switching from a **popularity-based recommender (A)** to a **collaborative-filtering variant (B)**, while also improving positive engagement.

---

## Context
For Spotify, **skip rate is a proxy for dissatisfaction** — if users skip too many songs early, the playlist feels irrelevant.  
Lower skips → better personalization → higher engagement and retention.  

---

## Quick Start
1. Open `Spotify_SkipRate_AB_Test.ipynb` and run all cells.  
2. Tweak the **CONFIG** section to explore different effect sizes or sample sizes.  
3. Check:  
   - `RESULTS.md` → concise readout of results  
   - `sessions_simulated.csv` → simulated dataset  

---

## Metrics
- **Primary:** Skip rate (≤ 30s skip proxy) — *lower is better*  
- **Secondary:** Save rate — *higher is better*  
- **Tertiary:** Session minutes — *higher is better*  

---

## Results Summary
- **Skip Rate:** B reduced skips by ~10 percentage points.  
- **Save Rate:** B increased saves by ~4 percentage points.  
- **Session Minutes:** B added ~2 extra minutes per session.  

All differences were statistically significant (p < 0.001).  
Visuals (bar charts) in the notebook make the win obvious to stakeholders.

---

## Decision Template
If skip rate decreases **and** saves/session minutes increase with statistical significance:  
→ Recommend a **staged rollout (10–25%)** with guardrails (complaints, churn proxies) and cohort monitoring (device, time-of-day).  

---

## Next Steps / Extensions
- Analyze **long-term retention** and churn impacts.  
- Explore **time-of-day and user tenure cohorts**.  
- Test **hybrid recommenders** that combine collaborative filtering with editorial or contextual signals.  

---

## Files
- `Spotify_SkipRate_AB_Test.ipynb` → full simulation & analysis notebook  
- `RESULTS.md` → summarized findings  
- `sessions_simulated.csv` → synthetic dataset used in analysis  
