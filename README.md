# Apex-The-Local-Truth-Engine-2026
Apex — The Local Truth Engine

**Measured local visibility. No modeling. No smoothing. No guessing.**

Apex is a **100% free, open-source local rank measurement tool** designed to answer one question:

> _“What does Google actually show at this exact location?”_

Not what a model predicts.  
Not what a map suggests.  
Not what a heatmap smooths.

Just reality — measured point by point.

* * *

## 🚨 Why Apex Exists

Most local rank tools **model visibility**.

They:

*   interpolate grids
    
*   reuse responses
    
*   smooth results
    
*   collapse locations
    
*   hide dead zones
    

That’s fine — **as long as you treat them like models**.

The problem is:

> **We don’t.**

We make real decisions — SEO, spend, categories, links — based on data that _looks_ like ground truth.

Apex exists to be a **measurement instrument**, not a reassurance machine.

* * *

## 🧠 What Makes Apex Different

| Typical Grid Tools | Apex |
| --- | --- |
| Modeled visibility | Measured visibility |
| Interpolated grids | One request per point |
| Smoothed heatmaps | Raw, jagged output |
| Centroids & snapping | Exact latitude/longitude |
| Maps-centric | Google Search local surface |
| Confidence-first | Truth-first |

If Google returns nothing — Apex records nothing.  
That’s not an error. That’s the data.

* * *

## 🔬 What Apex Measures

*   Google **Search** local results (not Maps API)
    
*   Location-specific queries at **exact coordinates**
    
*   Mobile-style search context
    
*   Real volatility, suppression, and dead zones
    

Apex does **not**:

*   infer missing points
    
*   average neighbors
    
*   “fix” ugly grids
    
*   normalize output
    

Ugly data is often the most honest data.

* * *

## 📦 What’s In This Repo

    /apex
    ├── /apps-script
    │   ├── apex.gs          # Core Apps Script logic
    │   ├── grid.gs          # Grid generation
    │   ├── serp.gs          # SERP request handling
    │   └── helpers.gs       # Distance, parsing, utils
    │
    ├── /docs
    │   ├── ENGINEERING_NOTE.md
    │   ├── HOW_IT_WORKS.md
    │   ├── INTERPRETING_RESULTS.md
    │   ├── RED_TEAM_TESTS.md
    │   └── CONTRIBUTING.md
    │
    ├── /examples
    │   ├── sample_keywords.csv
    │   └── sample_results.csv
    │
    └── README.md
    

* * *

## ⚙️ How It Works (High Level)

1.  You define:
    
    *   keyword
        
    *   center lat/lng
        
    *   radius
        
2.  Apex:
    
    *   generates a grid of geographic points
        
    *   runs **one Google local query per point**
        
    *   records the raw result
        
3.  Results are written exactly as returned.
    
    *   No cleanup
        
    *   No smoothing
        
    *   No interpolation
        

* * *

## 🚀 Getting Started (5 Minutes)

### 1️⃣ Make a Copy of the Sheet

*   Open the provided Google Sheet template
    
*   Make a copy to your Drive
    

### 2️⃣ Open Apps Script

*   Extensions → Apps Script
    
*   Paste in the files from `/apps-script`
    

### 3️⃣ Add Your API Key

*   Menu → `Apex → Set API Key`
    
*   Uses **your own** SerpApi key (BYO key)
    

Apex never resells data.  
You pay the API provider directly.

### 4️⃣ Run a Grid

*   Enter keywords + coordinates
    
*   Click `Run Grid Scan`
    

That’s it.

* * *

## 📊 How to Read Apex Results

### Rank Interpretation

*   **1–3** → Local Pack visibility
    
*   **4–20** → Finder depth
    
*   **No results** → suppression, filtering, or low confidence
    

Dead zones are real.  
They matter.

* * *

## ⚠️ Important: What Apex Is NOT

Apex is **not**:

*   a daily rank tracker
    
*   a forecasting tool
    
*   a pretty heatmap generator
    
*   a reassurance engine
    

It’s a **truth check**.

Use it when:

*   data looks wrong
    
*   grids contradict reality
    
*   decisions are high-impact
    

* * *

## 🧪 Red-Team Philosophy

Apex was built alongside a **red-team test suite** that attempts to break local rank tools.

**If a grid:**

*   looks too clean
    
*   never embarrasses you
    
*   never shows suppression
    
*   never contradicts intuition
    

…it should be questioned.

See `/docs/RED_TEAM_TESTS.md`.

* * *

## 🧠 Community Data (The Fun Part)

This project is **community-driven**.

You’re encouraged to:

*   upload anonymized grids
    
*   share before/after comparisons
    
*   submit contradictions
    
*   contribute test cases
    

### How to Share Results

*   Export results as CSV
    
*   Remove business names if needed
    
*   Submit via Pull Request or Issues
    

Over time, this repo becomes:

> **A public corpus of how Google _actually_ behaves.**

* * *

## 🧑‍⚖️ Legal & Ethical Notes

*   Apex does not claim other tools are scams
    
*   Apex does not name vendors
    
*   Apex does not guarantee rankings
    
*   Apex makes **no promises except measurement**
    

If Apex ever disagrees with a real device:

> **Trust the device. Not Apex.**

That’s the rule.

* * *

## 🤝 Contributing

We welcome:

*   code improvements
    
*   performance tuning
    
*   additional validation methods
    
*   documentation clarity
    
*   new red-team tests
    

See `/docs/CONTRIBUTING.md`.

* * *

## 🧭 Core Doctrine

> Models explain.  
> Measurements reveal.

> Clean data feels good.  
> Truth is better.

> If the grid never embarrasses you —  
> it’s not real.

* * *

## ⭐ Final Note

Apex is free because:

*   truth shouldn’t be paywalled
*   measurement shouldn’t be proprietary
*   confidence shouldn’t be sold as reality
     
    

**Use it. Break it. Challenge it. Improve it. That’s the point.**  

  

* * *

If you want next, I can:

*   write the **CONTRIBUTING.md** in detail
    
*   design a **community leaderboard / gallery**
    
*   help you add a **“submit your grid” workflow**
    
*   or write a **Code of Ethics** section (very powerful)
    

Just say the word.
