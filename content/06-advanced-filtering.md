---
title: Advanced Filtering
description: Advanced filters provide fine-grained control over your dataset. Access them by clicking Advanced in the filter panel.
---

## Filter State(s)

**What it does:** Overrides the main state filter with a custom comma-separated list of states.

**Format:** `GA, FL, AL` (comma-separated state codes)

**Use case:** Analyze a multi-state region or compare players across state boundaries.

### Example

**Filter States:** `GA, TN, AL, FL`

**Result:** Shows players from Georgia, Tennessee, Alabama, and Florida combined.

**Why use this?**
- Southeast regional analysis
- Cross-border scenes (e.g., NYC area includes NJ, CT)
- Comparing related regions

---

## Character Filters

**What it does:** Shows only players who main specific characters.

**Format:** `Falco, Sheik, Fox` (comma-separated character names)

### How It Works

- Matches against player's **registered main character**
- For weighted calculations, uses the **first character listed**
- Case-insensitive matching

### Examples

**Filter:** `Marth`
**Result:** Only Marth mains

**Filter:** `Fox, Falco`
**Result:** Spacie players (Fox or Falco)

**Filter:** `Sheik, Marth, Fox`
**Result:** Top-tier character analysis

### Use Cases

- Compare character meta in your region
- Find mirror match opponents
- Analyze character representation
- Study character-specific bracket performance

---

## Min/Max Entrants (average)

Controls which players appear based on the **average size** of brackets they attend.

### Min Entrants

**What it does:** Keeps players whose average event had **at least** this many entrants.

**Format:** Number (e.g., `32`, `64`)

**Example:** `Min: 32` = Only players who average 32+ person brackets

**Use cases:**
- Focus on established locals/regionals
- Filter out players who only attend small friendlies
- Find players who compete at a certain bracket tier

---

### Max Entrants

**What it does:** Keeps players whose average event had **at most** this many entrants.

**Format:** Number (e.g., `64`, `128`)

**Example:** `Max: 64` = Only players who average ≤64 person brackets

**Use cases:**
- Exclude players who primarily attend majors
- Focus on local/regional grinders
- Analyze mid-tier bracket performers

---

### Combining Min and Max

**Example:** `Min: 16, Max: 48`

**Result:** Players who compete in mid-sized brackets (16-48 entrants on average)

**Why?** Target a specific bracket tier without including smaller locals or large majors.

---

## Min Largest Event Entrants

**What it does:** Requires players to have attended **at least one event** with this minimum entrant count.

**Format:** Number (e.g., `64`, `128`)

**Example:** Setting `64` = "Show only players who've competed in at least one 64+ person bracket"

### Use Case

Find players with **major tournament experience**, regardless of whether they attend majors regularly.

**Difference from Min Entrants:**
- **Min Entrants:** Average across all events
- **Min Largest Event:** Just the biggest single event

**Example:**
- Player attends: 16, 32, 32, 128 entrant events
- Average: 52 entrants
- Largest: 128 entrants

With `Min Entrants: 60`, they're **excluded**.
With `Min Largest Event: 100`, they're **included**.

---

## Large Event Threshold

**What it does:** Defines what counts as a "large event" for the share calculation below.

**Format:** Number (default: `32`)

**Example:** Set to `48` if you consider only 48+ brackets to be "large" in your region.

### Regional Context

What counts as "large" varies:
- **NYC:** 32+ might be a typical weekly
- **Rural area:** 16+ could be a major local
- **Major:** 128+ is the standard

Adjust this to match your regional context.

---

## Min Large Event Share

**What it does:** Requires a minimum **fraction** of a player's events to meet the "large event" threshold.

**Format:** Decimal between 0 and 1 (e.g., `0.33` = 33%, `0.5` = 50%)

### How It Works

1. System counts how many of a player's events meet the "Large Event Threshold"
2. Calculates: (large events) / (total events)
3. Keeps players where this ratio ≥ Min Large Event Share

### Example

**Settings:**
- Large Event Threshold: `32`
- Min Large Event Share: `0.5`

**Player's Events:**
- Attended: 8 events total
- Large events (32+): 5 events
- Share: 5/8 = 0.625 (62.5%)

**Result:** Player is **included** (62.5% ≥ 50%)

### Use Case

Find players who **consistently compete at higher-level events**, not just locals.

**Example Use:**
- Threshold: `40`
- Share: `0.6`
- **Result:** Players where 60%+ of their events had 40+ entrants

---

## Start After

**What it does:** Excludes players whose **most recent event** started on or after this date.

**Format:** Date picker (MM/DD/YYYY)

**Example:** Setting `01/01/2024` excludes players who haven't competed since January 1st, 2024.

### Use Cases

**Filter out inactive players:**
- Set to 1-2 months ago
- Removes players who've retired or taken a break

**Analyze a specific historical window:**
- Set both timeframe and start date
- Example: "3 months of data, ending in March 2024"

---

## Combining Advanced Filters

Filters work together multiplicatively - each one narrows the dataset further.

### Example: Finding Elite Local Grinders

**Settings:**
```
Min Entrants: 32
Max Entrants: 64
Large Event Threshold: 40
Min Large Event Share: 0.5
```

**Result:** Players who:
- Average 32-64 person brackets
- Attend 40+ person events at least half the time
- Likely dedicated local/regional grinders

---

### Example: Major Tournament Veterans

**Settings:**
```
Min Largest Event: 128
Character Filter: Fox, Falco, Marth
```

**Result:** Top-tier character players with major experience.

---

## Tips for Effective Filtering

1. **Start broad, narrow gradually** - Apply filters one at a time to see their effect
2. **Check row counts** - If you get 0 results, filters are too restrictive
3. **Use Reset liberally** - Don't be afraid to start over
4. **Consider regional context** - A "large" event in one state might be small in another
5. **Combine character + entrant filters** - Find serious mains of specific characters

---

## Next Steps

- **Interpret your results:** [Reading the Data](07-reading-the-data.md)
- **Apply practical strategies:** [Tips & Best Practices](08-tips-and-best-practices.md)

---
