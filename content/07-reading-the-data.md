---
title: Reading the Data
description: Once you've applied filters and generated a visualization, this guide helps you interpret and use the results.
---

## The Data Table

Below the scatter chart, you'll find a detailed table with all players in your filtered dataset.

<!-- SCREENSHOT: Data table showing several rows of player data -->

### Columns

| Column | Description |
|--------|-------------|
| **Player** | Gamer tag |
| **Win rate** | Weighted win rate as percentage (0-100%) |
| **Opp strength** | Opponent strength with 3 decimal precision |
| **State** | Player's home state code |

### Table Features

- **Sortable** - Click column headers to sort (implementation may vary)
- **Row count** - Displays at the top: "X rows"
- **Full dataset** - Shows all players, including those filtered from the chart

---

## Understanding Table vs Chart

### Why Some Players Appear in the Table but Not the Chart

Players need **both** valid metrics to appear on the scatter plot:
- `weighted_win_rate` must be a valid number (0-1)
- `opponent_strength` must be a valid number

**If either is missing or invalid**, the player appears in the table but not on the chart.

### Hidden Data Notes

Below the chart and table, you'll see informational messages:

#### "X row(s) skipped (missing win rate or opponent strength)"

**What it means:** Players with incomplete data.

**Why it happens:**
- Too few games to calculate reliable metrics
- Data collection errors
- Player competed but didn't face opponents with calculated strength

**What to do:** These players are typically new or inactive - usually safe to ignore.

---

#### "X outlier(s) hidden"

**What it means:** Players removed by the "Hide outliers" filter.

**Example:** "2 outlier(s) hidden"

**What to do:**
- Toggle "Hide outliers" off to see them
- Check if high performers are being excluded
- Re-enable to focus on the main cluster

---

## Analyzing Results

### Quick Insights

#### High-Performers (Top-Right)
Players in the top-right quadrant are your regional elite:
- High win rate
- High opponent strength
- Likely PR'd or should be

#### Rising Stars (Top-Left)
Players with high win rates but moderate opponent strength:
- Dominating current bracket level
- Ready to level up
- Watch for improvement when they face tougher competition

#### Challengers (Bottom-Right)
Players with lower win rates but high opponent strength:
- Competing above their current level
- Gaining valuable experience
- May show rapid improvement over time

#### Developing Players (Bottom-Left)
Players with both low metrics:
- New to competitive play
- Building fundamentals
- Normal starting position

---

## Using the Data

### For Power Rankings

1. Apply state-level filters with 3-month timeframe
2. Look at top-right quadrant
3. Compare players with similar opponent strength
4. Higher win rate = better ranking (all else equal)

### For Tournament Seeding

1. Filter by tournament series
2. Use 1-2 month timeframe for recency
3. Sort by win rate
4. Consider opponent strength as tiebreaker

### For Personal Improvement

1. Find yourself in the data
2. Note your opponent strength
3. Look at players with slightly higher strength
4. Aim to reach their win rate before moving up

---

## Exporting Data

Currently, there's no built-in export feature. To save data:

1. **Screenshot** the chart for quick reference
2. **Copy** table rows manually if needed
3. **Take notes** on key players and metrics

*(Feature request: CSV export would be useful here)*

---

## Data Freshness

### How Recent Is the Data?

- Data is **precomputed** from the backend
- Timeframe filter controls which events are included
- Typically updated: *(frequency depends on backend implementation)*

### If Data Seems Outdated

- Check that your timeframe is appropriate
- Verify the state code is correct
- Try a different timeframe to confirm

---

## Comparing Across Queries

To compare different filters:

1. **Take screenshots** of each configuration
2. **Note the row counts** - different filters return different player sets
3. **Compare key players** - see how they perform in different contexts

**Example:** How does Player X perform at weeklies vs majors?
- First query: Tournament view, weekly series
- Second query: Min Largest Event: 128
- Compare their positions

---

## Common Patterns

### Cluster in Bottom-Left
**What it means:** Lots of developing players or small local scene.

**Action:**
- Increase Min Entrants to focus on established players
- Look for outliers showing growth

---

### Diagonal Line from Bottom-Left to Top-Right
**What it means:** Healthy competitive distribution - players get better as they face tougher competition.

**Action:** This is ideal! Shows a functioning competitive ecosystem.

---

### Gap in the Middle
**What it means:** Missing intermediate players - scene may be polarized between beginners and veterans.

**Action:**
- Identify ways to help developing players improve
- May indicate need for intermediate-level events

---

### Dense Cluster in Top-Right
**What it means:** Many elite players in the region.

**Action:**
- Use advanced filters to differentiate within this cluster
- Consider character filters or tournament-specific views

---

## Next Steps

- **Apply practical strategies:** [Tips & Best Practices](08-tips-and-best-practices.md)
- **Solve common problems:** [Troubleshooting](09-troubleshooting.md)

---
