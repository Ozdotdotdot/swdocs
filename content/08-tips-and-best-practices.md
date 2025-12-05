---
title: Tips & Best Practices
description: Practical strategies for getting the most out of Smash Watch.
---

## Common Use Cases

### Finding Rising Talent

**Goal:** Identify up-and-coming players in your region.

**Steps:**
1. Use **State View** with **3 months** timeframe
2. Set **Min Entrants: 24** to focus on established brackets
3. Enable **Hide outliers** to avoid top players dominating the view
4. Look for players in the **top-left** quadrant
   - High win rate (60-80%)
   - Moderate opponent strength (0.2-0.4)

**What you're seeing:** Players dominating their current bracket level who may be ready to compete at the next tier.

**Follow-up:** Check their recent tournament results and consider them for regional PR or invitations to higher-level events.

---

### Analyzing a Weekly Series

**Goal:** Understand performance trends at your local weekly.

**Steps:**
1. Switch to **Tournament View**
2. Enter the series name (e.g., `Guildhouse`, `The Function`)
3. Use **30 days** to see recent trends
4. Leave **Allow multiple series** disabled
5. Select the specific series from buttons if multiple match

**What to look for:**
- Who's improving? (moving up and right over time - requires multiple queries)
- Who's consistent? (high win rate, stable strength)
- Who's challenging themselves? (lower win rate, higher strength)

**Pro tip:** Run this query monthly and screenshot results to track improvement over time.

---

### Comparing Character Performance

**Goal:** See how different characters perform in your region.

**Steps:**
1. Use **State View** with **3 months**
2. Go to **Advanced → Character Filters**
3. Enter one character (e.g., `Fox`)
4. Click **Apply Filters**
5. Note the average cluster position
6. Screenshot the results
7. Reset and repeat for other characters

**What you're comparing:**
- Average win rate by character
- Average opponent strength faced
- Number of active players per character

**Example Analysis:**
- `Marth` mains: 15 players, average 0.35 strength, 58% win rate
- `Fox` mains: 22 players, average 0.42 strength, 61% win rate
- **Conclusion:** More Fox players, facing slightly tougher competition

---

### Preparing for a Major

**Goal:** Research opponents before a major tournament.

**Steps:**
1. Switch to **Tournament View**
2. Paste the **tournament URL** from start.gg
3. Set timeframe to **3 months**
4. Look for players in your region or registered for the event

**What to study:**
- Win rates of potential bracket opponents
- Who they've beaten (check their strength)
- Character matchups you'll face

**Pro tip:** Cross-reference with the tournament's attendee list to focus on likely matchups.

---

### Evaluating Your Own Progress

**Goal:** Track your competitive improvement.

**Steps:**
1. Run a state-level query monthly
2. Find yourself in the results
3. Track these metrics over time:
   - Your win rate (going up?)
   - Your opponent strength (going up?)
   - Your position relative to known players

**Healthy progression:**
- Win rate stays stable or increases
- Opponent strength gradually increases
- You move from top-left → top-right over months

**Warning signs:**
- Win rate dropping while strength stays constant (hitting a wall)
- Neither metric improving over 3+ months (need to change training approach)

---

## Advanced Strategies

### Finding Your Next Rival

**Goal:** Identify players slightly better than you to practice against.

**Steps:**
1. Find your position on the chart
2. Look for players with:
   - 5-10% higher win rate
   - Similar opponent strength (±0.1)
3. These are ideal practice partners

**Why this works:** Playing people slightly better accelerates improvement without being discouraging.

---

### Regional Meta Analysis

**Goal:** Understand what's working in your region.

**Steps:**
1. **Character Distribution:**
   - Run queries for top-tier characters
   - Count players per character
   - Note win rates

2. **Bracket Tier Analysis:**
   - Query 1: `Min Entrants: 32, Max Entrants: 64` (locals/regionals)
   - Query 2: `Min Entrants: 64` (majors)
   - Compare player overlap

3. **Trend Detection:**
   - Run same query monthly
   - Track changes in player count and positions
   - Spot emerging trends

---

### Tournament Series Comparison

**Goal:** Compare multiple weekly series.

**Steps:**
1. Query each series separately (Tournament View)
2. Screenshot each result
3. Compare:
   - Average opponent strength
   - Number of unique players
   - Win rate distributions

**Use case:** Deciding which weekly to attend for optimal competition level.

---

## Data Interpretation Tips

### Don't Over-Index on Single Metrics

**Bad:** "Player A has 0.01 higher opponent strength, therefore they're better."

**Good:** "Player A and B have similar strength, but A has 10% higher win rate - A is likely performing better currently."

**Why:** Small differences in metrics can be statistical noise. Look for meaningful gaps (10%+ win rate difference, 0.1+ strength difference).

---

### Context Matters

**Example Scenario:**
- Player A: 75% win rate, 0.3 strength
- Player B: 55% win rate, 0.6 strength

**Question:** Who's better?

**Answer:** Depends on context!
- Player A dominates locals but hasn't tested themselves
- Player B competes at high level but is still improving
- In 6 months, Player B may surpass Player A

**Takeaway:** Consider player trajectory, not just current metrics.

---

### Watch for Sample Size Issues

Small sample sizes lead to unreliable metrics:

**Red flags:**
- Player shows up but you've never seen them
- Extreme metrics (95%+ win rate, very high strength)
- Player has very few events in the timeframe

**What to do:** Use **Min Entrants** or **Min Large Event Share** to filter out low-sample players.

---

## Workflow Optimization

### Start Broad, Then Narrow

1. Run a basic state-level query
2. Review the overall distribution
3. Identify interesting clusters or outliers
4. Add filters to zoom in on those areas

**Example:**
- Initial query: All GA players
- Notice a cluster of mid-level Fox players
- Add filter: `Character: Fox`, `Min Entrants: 32`
- Analyze just that group

---

### Use the Reset Button

Don't be afraid to **Reset** frequently:
- Clears mental clutter
- Prevents filter interactions you forgot about
- Fresh start when exploring new questions

**When to reset:**
- Switching between unrelated analyses
- Getting zero results and not sure why
- Starting a new session

---

### Save Your Screenshots

Since there's no export feature:
- Screenshot interesting visualizations
- Label them with date and filter settings
- Build a library for longitudinal analysis

**Naming convention example:**
```
2024-01-15_GA_State_3mo_Fox.png
2024-01-15_Guildhouse_Weekly_30d.png
```

---

## Common Mistakes to Avoid

### Mistake 1: Comparing Different Timeframes

**Wrong:** "Player A is better because they had higher win rate in 3-month view than Player B in 30-day view."

**Right:** Use the same timeframe for all players you're comparing.

---

### Mistake 2: Ignoring Opponent Strength

**Wrong:** "Player A has 80% win rate, Player B has 60%, therefore A is better."

**Right:** Check opponent strength. B might be facing much tougher competition.

---

### Mistake 3: Over-Filtering

**Symptoms:** Getting zero results or fewer than expected.

**Solution:**
- Remove filters one at a time
- Check your state code spelling
- Increase timeframe

---

### Mistake 4: Treating Outliers as Noise

**Wrong:** Always hiding outliers.

**Right:** Outliers can be meaningful:
- Elite players who should be studied
- Statistical anomalies worth investigating
- Data quality issues to report

**Rule of thumb:** Hide outliers for readability, but check who they are before dismissing them.

---

## Next Steps

- **Troubleshoot issues:** [Troubleshooting](09-troubleshooting.md)
- **Understand core concepts:** [Understanding Metrics](03-understanding-metrics.md)

---
