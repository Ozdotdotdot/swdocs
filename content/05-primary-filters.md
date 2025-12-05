---
title: Primary Filters
description: Primary filters are the essential controls for defining your dataset. They're always visible in the filter panel.
---

## State

**What it does:** Filters players by their home state.

**Format:** Two-letter state code (e.g., `GA`, `NY`, `FL`)

**Example:** Entering `CA` shows only California-based players.

### Tips
- Must be uppercase (the system auto-converts)
- Must be a valid US state code
- Required field - you must enter a state to get data

---

## Timeframe

**What it does:** Limits data to events within the selected time window.

**Options:**
- **Last 30 days** - Most recent month of activity
- **Last 60 days** - Past two months
- **Last 3 months** - Full quarter (default)

### When to Use Each

| Timeframe | Best For |
|-----------|----------|
| **30 days** | Current form, recent meta changes, weekly series |
| **60 days** | Smoothing out variance, seasonal trends |
| **3 months** | Full picture, power rankings, stable metrics |

### Important Notes

- More recent timeframes show **current form**
- Longer windows **smooth out variance** but may include inactive players
- Events are counted by **start date**
- Selecting a longer timeframe returns more data (slower load times)

---

## Hide Outliers

**What it does:** Removes players in the top ~1% of opponent strength to prevent extreme values from distorting the chart scale.

**Exception:** Players with win rates ≥70% are **always kept**, even if they're statistical outliers.

<!-- SCREENSHOT: Chart before/after hiding outliers, showing the difference in scale -->

### When to Use

**Enable "Hide outliers" when:**
- Chart looks "squished" or "zoomed out"
- A few elite players are compressing the scale
- You want to focus on the bulk of your regional scene
- Analyzing locals where most players cluster in a small range

**Disable "Hide outliers" when:**
- You specifically want to see elite player performance
- Analyzing majors where high-strength opponents are expected
- Dataset is small (< 20 players) and every data point matters
- You need to see the full competitive spectrum

### What Gets Hidden

The filter calculates the 99th percentile of opponent strength in your dataset, then:

1. **Removes** players above that threshold
2. **Keeps** all players with ≥70% win rate (even if above threshold)
3. **Displays** a count of hidden outliers below the chart

**Example:**
- Dataset: 200 players
- 99th percentile strength: 0.65
- Players above 0.65: 4 players
- Players above 0.65 with ≥70% win rate: 2 players
- **Result:** 2 outliers hidden, 198 shown

---

## How Filters Interact

Filters are applied in this order:

1. **State** - Selects the geographic region
2. **Timeframe** - Filters by event date range
3. **Hide outliers** - Removes extreme values (if enabled)
4. **Advanced filters** - Further refinement (see [Advanced Filtering](06-advanced-filtering.md))

Each filter narrows the dataset further.

---

## Filter Workflow

### Recommended Process

1. Select your **view type** (State or Tournament)
2. Enter a **state code**
3. Choose your **timeframe** based on your goal
4. Click **Apply Filters**
5. Evaluate the chart
6. Toggle **Hide outliers** if the chart is hard to read
7. Add **advanced filters** if needed

---

## Resetting Filters

Click the **Reset** button to:
- Clear all filter values
- Return to State view (default)
- Reset timeframe to 3 months
- Disable "Hide outliers"
- Clear all advanced filters

This is useful when starting a fresh analysis.

---

## Next Steps

- **Refine your search:** [Advanced Filtering](06-advanced-filtering.md)
- **Read your results:** [Reading the Data](07-reading-the-data.md)

---
