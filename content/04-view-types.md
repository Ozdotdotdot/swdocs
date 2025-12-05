---
title: View Types
description: "Smash Watch offers two view modes optimized for different analysis scenarios: State View and Tournament View."
---

## State View

Analyzes **all players** from a specific state over your selected timeframe.

<!-- SCREENSHOT: State view filter panel with "GA" entered -->

### When to Use

**Best for:**
- Regional power rankings
- Identifying rising talent in your scene
- Comparing player performance across the state
- Getting a broad view of competitive activity

### How It Works

**Example:** Setting State to `GA` with 3 months shows everyone who competed in Georgia during that period, regardless of which specific tournaments they attended.

### Primary Filters

- **State** - Two-letter state code (e.g., `GA`, `NY`, `FL`)
- **Timeframe** - 30 days, 60 days, or 3 months
- **Hide outliers** - Toggle to remove statistical outliers

---

## Tournament View

Focuses on **specific tournament series** or individual events.

<!-- SCREENSHOT: Tournament view filter panel with series options -->

### When to Use

**Best for:**
- Weekly series analysis (e.g., who's improving at your local)
- Major tournament deep-dives
- Comparing performance within a specific event series
- Isolating a specific competitive environment

### How It Works

You can filter by:

1. **Tournament Series** - Enter series name (e.g., `4o4`, `Guildhouse`)
2. **Tournament URL/Slug** - Paste a start.gg URL or slug directly

### Series Filtering

#### Single Series
1. Enter series name in "Tournament Series" field
2. Click **Apply Filters**
3. If multiple series match, you'll see selection buttons
4. Click a series button to load that specific dataset

<!-- SCREENSHOT: Multiple series selection buttons appearing after filtering -->

#### Multiple Series (Combined)
1. Enter series name
2. Enable "Allow multiple series" toggle
3. Click **Apply Filters**
4. Data from all matching series is combined

### URL/Slug Filtering

You can paste a **start.gg URL** directly:

**Examples:**
```
https://start.gg/tournament/genesis-9/event/melee-singles
tournament/genesis-9
genesis-9
```

The system will automatically parse and search for matching tournaments.

---

## Switching Between Views

The view type toggle is at the top of the filter panel:

1. Click **State** or **Tournament**
2. Fill in the appropriate filters for that view
3. Click **Apply Filters**

**Note:** Switching views clears your current data - make sure to save any insights first!

---

## View-Specific Advanced Filters

Both views share most advanced filters, but tournament view has additional options:

### State View Only
- Focuses on state-level aggregation
- Simpler filtering (just state code + timeframe)

### Tournament View Only
- **Tournament Series field** - Text search for series names
- **Tournament URL/Slug field** - Direct tournament lookup
- **Allow multiple series toggle** - Combine or separate matching series

---

## Choosing the Right View

| Goal | Recommended View |
|------|------------------|
| "Who's the best in my state?" | State View |
| "How did X tournament go?" | Tournament View (URL/slug) |
| "Who's improving at my weekly?" | Tournament View (series) |
| "Compare two regions" | State View (use Filter States in advanced) |
| "Analyze a major" | Tournament View (URL/slug) |
| "Track local meta over time" | Tournament View (series) |

---

## Next Steps

- **Learn about primary filters:** [Primary Filters](05-primary-filters.md)
- **Dive into advanced options:** [Advanced Filtering](06-advanced-filtering.md)

---
