# UEFA Champions League Final 2021/22 — Expected Goals (xG) Analysis

A Python data-analysis project exploring the shot-by-shot performance of **Liverpool and Real Madrid** in the 2021/22 UEFA Champions League Final.

## Project Objective

Analyze the match beyond the final score by examining:
- Shot volume and chance quality.
- Expected Goals (xG) for both teams.
- Cumulative xG throughout both halves.
- The timing and quality of individual shots.
- Shot outcomes and Post-Shot Expected Goals (PSxG).

## Match Snapshot

| Metric | Liverpool | Real Madrid |
|---|---:|---:|
| Shots | 23 | 4 |
| Total xG | 1.54 | 0.78 |
| Goals | 0 | 1 |

The dataset contains **27 recorded shots**. Real Madrid won 1–0, with Vinícius Júnior scoring in the 59th minute.

Liverpool accumulated higher xG, but Real Madrid converted its high-quality opportunity.

## Repository Structure

| File | Description |
|---|---|
| `uefa_cl_2022_xG_report.ipynb` | Jupyter Notebook containing data preparation, analysis, and visualizations. |
| `shots_table.csv` | Shot-by-shot match dataset. |
| `README.md` | Project documentation. |

## Dataset Description

| Column | Description |
|---|---|
| `Minute` | Match minute, including stoppage time. |
| `Player` | Player who took the shot. |
| `Squad` | Team name. |
| `xG` | Expected Goals probability for the shot. |
| `PSxG` | Post-Shot Expected Goals. |
| `Outcome` | Goal, Saved, Blocked, Off Target, etc. |
| `Distance` | Shot distance. |
| `Body Part` | Body part used. |
| `Notes` | Additional shot details. |
| `Assist Player` | Player involved in the immediate build-up. |
| `Assist Event` | Type of assist event. |
| `Second Assist Player` | Player involved in the preceding build-up. |
| `Second Assist Event` | Type of second-assist event. |

## Analysis Workflow

1. Load the CSV dataset using pandas.
2. Select the relevant columns for xG analysis.
3. Calculate cumulative xG separately for each team.
4. Clean missing xG values.
5. Convert stoppage-time values into numeric match minutes.
6. Separate first-half and second-half shots.
7. Compare the teams using visualizations.

## Visualizations

### 1. Cumulative xG Timeline

A step chart showing the running total of expected goals throughout the match.

It helps identify:
- Periods of attacking pressure.
- High-quality scoring opportunities.
- Changes in attacking performance between halves.

### 2. Per-Shot xG Scatter Plot

A scatter plot showing each shot's xG against the match minute.

It helps identify:
- The most dangerous individual shots.
- When each team created chances.
- Differences in shot quality.

## Key Findings

- Liverpool recorded 23 shots and approximately **1.54 xG**.
- Real Madrid recorded 4 shots and approximately **0.78 xG**.
- Liverpool generated more total expected goals through a higher volume of chances.
- Vinícius Júnior scored Real Madrid's winning goal in the 59th minute, from a shot recorded at **0.70 xG**.
- The final score was Real Madrid 1–0 Liverpool.

**Main takeaway:** The team with the higher xG does not necessarily win. A single high-quality opportunity can make the difference.

*The xG totals are calculated from the repository dataset and are not official match statistics.*

## Technologies and Libraries

- Python
- Jupyter Notebook
- pandas — data manipulation and analysis
- NumPy — numerical operations
- Matplotlib — data visualization
- highlight-text — highlighted chart titles

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Aminsfwt/UEFA-CL-2022-Final-xG-stats.git
cd UEFA-CL-2022-Final-xG-stats
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib highlight-text jupyter
```

### 3. Run the notebook

```bash
jupyter notebook
```

Open `uefa_cl_2022_xG_report.ipynb` and execute the cells in order.

Make sure `shots_table.csv` is in the same directory as the notebook.

## Possible Improvements

- Add player-level performance comparisons.
- Include goal markers in the cumulative xG timeline.
- Improve chart labels and legends.
- Compare xG with PSxG.
- Extend cumulative xG lines to the final whistle.
- Add additional shot-outcome visualizations.

## Author

**Amin Safout**

GitHub: [@Aminsfwt](https://github.com/Aminsfwt)

---

This project is intended for educational and analytical purposes. Expected Goals values are estimates and depend on the data provider's model.
