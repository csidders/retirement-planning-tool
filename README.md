# Retirement Planning Tool

A Python tool that projects whether a client's retirement savings will last,
and measures how much that answer depends on the assumptions behind it.

## Finding

For a 58-year-old with $400k saved, planning to retire at 67 on $75k a year:

- A straight-line projection at 7% says the plan works and ends near $1.9M.
- Running the same plan across 1,000 randomized market paths, it succeeds 56% of the time.
- Removing Social Security drops that to 22%.

The gap between the single-path answer and the distribution is the reason to
simulate rather than project. The gap between 22% and 56% is a reminder that
the portfolio is only one of a client's income sources.

## What it does

- Year-by-year projection engine with inflation-adjusted spending and Social Security
- Sensitivity sweeps across retirement age and expected return
- Tornado chart ranking which assumptions move the outcome most
- Monte Carlo simulation reporting probability of success, with a fan chart

## Notes

Built on hypothetical client profiles. No real client data. Return, inflation,
and Social Security assumptions are illustrative choices of my own, not
recommendations.

## Running it

Requires numpy, pandas, and matplotlib. Open `RetirementTool.ipynb` and run all cells.
