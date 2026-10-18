# E-commerce Data Analysis (Python)

A data-quality deep dive into an e-commerce dataset using pandas.

## What I found

- **Discount validation:** the `Discount Name` field is conditionally populated based on `Discount Availed` — discount availed → name present, no discount → missing. Both consistency checks returned 0 exceptions.
- **Negative net amounts:** 613 records have a negative `Net Amount`. Investigation showed that in every one of those records, `Discount Amount` is greater than `Gross Amount` — a data-entry / business-logic issue worth flagging, not a calculation bug.

## What's inside

- `project.ipynb` — the full analysis: data validation checks, null/date handling, and the findings above.

## Tools

Python, pandas, Jupyter Notebook.

## Why this repo exists

Real datasets are messy — this project is my practice at finding that out systematically. Part of my learning-in-public journey as a data analyst.
