# Understanding Metrics

Smash Watch uses two primary metrics to evaluate player performance. This guide explains how they're calculated and what they mean.

---

## Weighted Win Rate

### What It Is

**Weighted win rate** is not just total wins divided by total games. It's a sophisticated metric that emphasizes:

- **Set count** - Players who compete more frequently
- **Opponent quality** - Wins against stronger players count more
- **Recency** - More recent results may be weighted higher (implementation-dependent)

### Why It Matters

A 60% weighted win rate against strong players is more impressive than 80% against weak opposition.

**Example:**
- Player A: 80% raw win rate, mostly against locals
- Player B: 60% weighted win rate, regularly beating PR'd players

**Player B** likely shows on the chart as having both a lower win rate BUT higher opponent strength - indicating they're competing at a higher level.

---

## Opponent Strength

### What It Is

Opponent strength measures the average skill level of opponents a player has faced. It's calculated based on:

- **Historical performance** of opponents faced
- **Placement results** of those opponents
- **Iterative strength calculations** across the scene

The system calculates strength recursively - beating someone who beats strong players increases your opponent strength more than beating someone who loses to everyone.

### Interpreting Values

Values are relative to your dataset, but general guidelines:

| Range | Competition Level |
|-------|-------------------|
| **< 0.3** | Local/regional level competition |
| **0.3 - 0.6** | Established regional/national level |
| **> 0.6** | Elite/top-level competition |

**Important:** These ranges vary by region and game - use them as relative guides within your filtered data.

---

## Why These Metrics Together?

Using both metrics together reveals player profiles:

### Scenario 1: High Win Rate, Low Strength
**Profile:** Local dominator
- Consistently winning against weaker competition
- May need to travel to tougher events to test themselves

### Scenario 2: High Win Rate, High Strength
**Profile:** Elite player
- Winning consistently against top competition
- Likely PR'd regionally or nationally

### Scenario 3: Low Win Rate, High Strength
**Profile:** Challenger
- Competing above their current level
- Taking losses but gaining valuable experience
- Watch for improvement over time

### Scenario 4: Low Win Rate, Low Strength
**Profile:** Developing player
- New to competitive play or struggling in current bracket level
- May improve by focusing on fundamentals

---

## Comparing Players

When comparing two players:

1. **Similar opponent strength?** → Compare win rates directly
2. **Similar win rates?** → Player with higher opponent strength is likely more skilled
3. **Different on both axes?** → Context matters (see profiles above)

---

## Limitations

### What These Metrics Don't Show

- **Peak performance** - Only averages over the time window
- **Consistency** - A player might have wild variance
- **Character matchups** - No matchup-specific data
- **Format** - Singles vs doubles, best-of-3 vs best-of-5
- **Recency** - 3-month data includes old results

### Data Quality

Metrics are only as good as the underlying data:
- Players who rarely compete have less reliable metrics
- Small sample sizes lead to outliers
- Regional isolation can skew strength calculations

---

## Next Steps

- **Apply this knowledge:** [Tips & Best Practices](08-tips-and-best-practices.md)
- **Filter your view:** [View Types](04-view-types.md)

---

[← Back to Understanding the Chart](02-understanding-the-chart.md) | [Next: View Types →](04-view-types.md)
