# How Apex Works

Apex simulates real mobile searches from precise geographic points to map local pack visibility.

## Workflow Overview

1. **Input**
   - Keyword (e.g., "emergency plumber fort lauderdale")
   - Center coordinates (lat/lng)
   - Radius (default 3 miles)
   - Grid density (default 5x5 = 25 points)

2. **Grid Generation**
   - Creates a uniform square grid centered on input coordinates.
   - Points spaced to fully cover radius without bias.

3. **Query Execution**
   - For each point:
     - Injects exact lat/lng via Maps engine `ll` parameter.
     - Forces mobile context.
     - Retrieves full local results (up to 20+).

4. **Ranking Extraction**
   - Parses structured local results.
   - Assigns exact rank per business at each point.
   - Records distance from center.

5. **Output**
   - Spreadsheet rows: One per business per point (up to ~500 rows for 5x5).
   - Columns: Date, keyword, point coords, distance, rank, business details, top ranker, JSON backup.
   - No interpolation—raw data only.

## Why This Approach
- Avoids UULE snapping (blocky/duplicated results).
- Full depth beyond Top 3 for meaningful gradients.
- Closest possible alignment to real mobile searches at physical locations.

Use Apex to validate visibility claims from other tools. Interpret results with INTERPRETING_RESULTS.md.
