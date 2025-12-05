---
title: Understanding the Chart
description: The scatter plot is the core visualization in Smash Watch. This guide explains how to read and interpret it.
---

## What You're Looking At

The scatter plot shows **two key metrics** for each player:

- **Y-axis (Vertical)**: **Weighted Win Rate** (0-100%)
  - Not just raw wins - accounts for bracket difficulty and opponent quality
  - Higher = player wins more consistently

- **X-axis (Horizontal)**: **Opponent Strength**
  - Measures the average skill level of opponents faced
  - Higher = player competes against tougher competition

<!-- SCREENSHOT: Annotated scatter chart showing axes, data points, and tooltip -->

**Each dot** represents one player in your filtered dataset.

---

## Reading the Positions

Understanding where a player appears on the chart tells you a lot about their competitive profile:

| Position | What It Means |
|----------|---------------|
| **Top-left** | High win rate, weaker opponents - dominating local scene |
| **Top-right** | High win rate, strong opponents - elite player |
| **Bottom-left** | Low win rate, weaker opponents - developing player |
| **Bottom-right** | Low win rate, strong opponents - punching up, facing tough competition |

<!-- DIAGRAM: Simple 2x2 grid showing these four quadrants with example labels -->

### Examples

**Player at (0.2 strength, 75% win rate):**
- Winning 3 out of 4 sets against local/regional players
- Likely a strong local hero or rising talent

**Player at (0.7 strength, 80% win rate):**
- Winning 4 out of 5 sets against top-level competition
- Elite player, possibly PR'd nationally

**Player at (0.5 strength, 40% win rate):**
- Losing more than winning against established regional players
- May be new to competitive play or punching above their weight class

---

## Interactive Features

### Hover Tooltips

Hover over any dot to see:
- **Gamer tag** - Player's tag
- **Win rate** - Exact percentage
- **Opp strength** - Precise value (3 decimals)

<!-- SCREENSHOT: Tooltip appearing on hover showing player details -->

### Scroll to Table

Below the chart, you'll find a full data table with sortable columns showing all players in the visualization.

---

## Chart Scaling

The chart automatically scales to fit your data:

- **X-axis** starts at 0 and extends to the maximum opponent strength in the dataset
- **Y-axis** always shows 0-100% for consistency

**Note:** If a few players have extremely high opponent strength, the chart may appear "squished." Use the **Hide outliers** toggle to zoom in on the main cluster.

<!-- SCREENSHOT: Chart before/after hiding outliers, showing the difference in scale -->

---

## What Makes a "Good" Position?

There's no single "best" position - it depends on context:

- **High win rate + moderate strength:** Strong regional player
- **Moderate win rate + high strength:** Competing at a high level, room to grow
- **High win rate + high strength:** Top-tier player

**The ideal position moves up and to the right** as players improve and face stronger competition.

---

## Next Steps

- **Learn about the metrics:** [Understanding Metrics](03-understanding-metrics.md)
- **Filter your data:** [Primary Filters](05-primary-filters.md)

---
