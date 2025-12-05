---
title: Troubleshooting
description: Common issues and how to resolve them.
---

## "No data found"

### Symptoms
- Chart is empty
- Table shows no players
- Message: "No data found. Check your state parameter and filters."

### Possible Causes

#### 1. Invalid State Code

**Check:** Is your state code a valid 2-letter US state abbreviation?

**Wrong:** `Georgia`, `ga`, `G`
**Right:** `GA`

**Fix:** Enter the correct 2-letter state code (uppercase).

---

#### 2. Timeframe Too Narrow

**Check:** Is there recent tournament activity in your state?

Some states have infrequent tournaments. A 30-day window might return zero results.

**Fix:** Increase timeframe to **3 months**.

---

#### 3. Filters Too Restrictive

**Check:** Are your advanced filters eliminating everyone?

**Example problem:**
- Min Entrants: 128
- Small state with no 128+ person events

**Fix:**
1. Click **Reset** to clear all filters
2. Start with just state + timeframe
3. Add filters gradually

---

#### 4. State Has No Data

**Check:** Does this state have tournament data in the database?

Less populated states or states with few start.gg events may not have data.

**Fix:**
1. Try a major state (e.g., `CA`, `NY`, `FL`, `GA`)
2. Verify the state has active Smash scene on start.gg

---

## "Select a series from the options"

### Symptoms
- Message: "Select a series from the options or Allow Multiple Series to load data."
- Series selection buttons appear
- No chart displays

### What Happened

Your tournament filter matched **multiple series**, and "Allow multiple series" is disabled.

**Example:** Searching for `Guildhouse` might match:
- Guildhouse Weekly (NY)
- Guildhouse Monthly (NY)
- Guildhouse Ultimate (different game)

### Fix

**Option 1: Select a Series**
1. Look at the series buttons that appeared
2. Click the one you want to analyze

**Option 2: Allow Multiple Series**
1. Enable "Allow multiple series" toggle
2. Click **Apply Filters** again
3. Data from all matching series will be combined

---

## Chart Looks "Squished"

### Symptoms
- All players clustered in the bottom-left
- Hard to distinguish individual dots
- Axes extend far to the right but most data is clumped

<!-- SCREENSHOT: Example of squished chart -->

### Cause

**Statistical outliers** with very high opponent strength are compressing the X-axis scale.

### Fix

Enable **Hide outliers** toggle:
1. Find the toggle in the filter panel
2. Click it to enable
3. Chart will auto-rescale
4. Check "X outlier(s) hidden" message

**Result:** Chart "zooms in" on the main cluster, making it easier to read.

<!-- SCREENSHOT: Same chart after hiding outliers -->

---

## Players Missing from Chart but in Table

### Symptoms
- Table shows X players
- Chart shows fewer dots
- Message: "X row(s) skipped (missing win rate or opponent strength)"

### Cause

Some players have **incomplete data**:
- Missing `weighted_win_rate` value
- Missing `opponent_strength` value
- Invalid/null values for either metric

### Why This Happens

- **Too few games** to calculate reliable metrics
- **Data collection errors** from the backend
- Player competed but **didn't face opponents with calculated strength**

### What to Do

**Typically safe to ignore** - these are usually:
- New players with < 3 events
- Inactive players with old, partial data
- Edge cases in the data pipeline

**If it's many players:**
- May indicate a data quality issue
- Try a different state or timeframe to verify

---

## Loading Takes Forever

### Symptoms
- "Loading data..." message persists
- No error appears
- Chart doesn't populate

### Possible Causes

#### 1. Large Dataset

**Check:** Are you querying a large state with 3-month timeframe?

States like California, New York, Florida have thousands of players.

**Fix:**
- Add **Min Entrants** filter to reduce dataset size
- Use shorter timeframe (30-60 days)
- Be patient - large queries can take 5-10 seconds

---

#### 2. Network Issues

**Check:** Is your internet connection stable?

**Fix:**
- Check browser console for errors (F12)
- Refresh the page
- Try a different network

---

#### 3. Backend Server Down

**Check:** Are other queries also failing?

**Fix:**
- Wait a few minutes and try again
- Report the issue if it persists

---

## Filter Doesn't Seem to Work

### Symptoms
- You change a filter but results don't change
- Expected different data

### Common Causes

#### 1. Forgot to Click "Apply Filters"

**Fix:** Always click **Apply Filters** after changing settings. Changing filter values doesn't auto-update.

---

#### 2. Filter Has No Effect on Current Dataset

**Example:** Setting "Character Filter: Marth" when no Marth players exist in your state.

**Fix:** Try different filter values or check if the filter is appropriate for your dataset.

---

#### 3. Conflicting Filters

**Example:**
- Min Entrants: 64
- Max Entrants: 32

This is impossible - no one can have average entrants between 64 and 32.

**Fix:** Review your filter values for logical conflicts.

---

## "API error 500" or Similar

### Symptoms
- Error message with HTTP status code
- Happens after clicking "Apply Filters"

### Cause

**Backend server error** - the data API encountered a problem.

### Fix

1. **Try a simpler query:**
   - Click Reset
   - Use just state + timeframe
   - Verify the server is working

2. **Wait and retry:**
   - Server may be temporarily down
   - Try again in a few minutes

3. **Report the issue:**
   - Note your exact filter settings
   - Report to: hello@smash.watch or GitHub issues

---

## Tournament URL Not Working

### Symptoms
- Pasted a start.gg URL
- Got "No data found" or no results

### Possible Causes

#### 1. URL Format Issue

**Check:** Is the URL from start.gg?

**Supported formats:**
```
https://start.gg/tournament/genesis-9/event/melee-singles
tournament/genesis-9
genesis-9
```

**Fix:** Try just the tournament slug (e.g., `genesis-9`)

---

#### 2. Tournament Not in Database

**Check:** Is this tournament in the system?

Only tournaments with:
- Data pulled from start.gg API
- Events in the selected timeframe
- Matching state filter

**Fix:** Try a different tournament or use series name instead.

---

#### 3. Wrong State Filter

**Check:** Does your state filter match the tournament location?

**Example problem:**
- State: `CA`
- Tournament: Genesis (held in California)
- But tournament marked as `NV` in database

**Fix:** Try the tournament's actual state or remove state filter.

---

## Mobile Issues

### Chart Won't Display on Mobile

**Symptoms:** Chart shows but is unreadable or cut off.

**Fix:**
- Rotate to landscape mode
- Zoom out with pinch gesture
- Use desktop view for detailed analysis

---

### Filter Panel Won't Open on Mobile

**Symptoms:** Tapping "Filters" button does nothing.

**Fix:**
- Refresh the page
- Try tapping directly on the button text
- Check if JavaScript is enabled

---

## Performance Tips

### Speed Up Queries

1. **Use Min Entrants:** Reduces dataset size significantly
2. **Shorter timeframes:** 30 days loads faster than 3 months
3. **Specific filters:** Character filters reduce processing
4. **Smaller states:** GA loads faster than CA

### Optimize Browsing

1. **Close other tabs:** Frees up browser memory
2. **Disable browser extensions:** Some extensions slow rendering
3. **Use modern browser:** Chrome, Firefox, Safari (latest versions)

---

## Still Having Issues?

### Before Reporting

1. **Try Reset** - Clears all filters
2. **Try different state** - Verify system is working
3. **Check browser console** - Press F12, look for errors
4. **Screenshot the issue** - Helpful for debugging

### How to Report

**Include:**
- Exact filter settings
- State code used
- Timeframe selected
- Screenshot of error
- Browser and OS version

**Contact:**
- **Email:** hello@smash.watch
- **GitHub Issues:** [github.com/ozdotdotdot/smashDA/issues](https://github.com/ozdotdotdot/smashDA/issues)

---

## Known Limitations

### Not Bugs, But Worth Knowing

1. **Data is precomputed** - Not real-time
2. **US states only** - International support may come later
3. **Melee focus** - Other games may have limited data
4. **No export feature** - Must screenshot results
5. **Limited historical data** - Typically 3-6 months max

---

[← Back to Tips & Best Practices](08-tips-and-best-practices.md) | [Back to Index](README.md)
