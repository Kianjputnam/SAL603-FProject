# SAL603 Final Project: NBA Draft Position vs Career Win Shares

## Project Overview

The NBA Draft is one of the most important mechanisms for team building in professional basketball. Teams invest significant resources into scouting and evaluating prospects with the goal of maximizing long-term player value.

This project analyzes whether draft position is actually predictive of long-term NBA success. Specifically, it examines whether a player’s draft pick number is related to their career **Win Shares**, an advanced metric that estimates the number of team wins contributed by a player. The goal of this project is to evaluate how effective draft position really is as a predictor of long-term player performance.

## Research Questions

* Is draft pick significantly correlated with career Win Shares?
* How much variation in career Win Shares is explained by draft position?
* Does draft position remain predictive outside of the lottery?
* Who have been the biggest draft steals based on predicted Win Shares?

## Data Source

All data was scraped directly from Basketball Reference draft pages using the **pandas `read_html()`** function.

Draft classes from the **2000–2024 NBA seasons** were included.

The primary variables used in the analysis were:

* **Pick** (Draft Position)
* **Player**
* **Career Win Shares (WS)**
* **Draft Year**

All data cleaning and transformations were performed entirely within the Python notebook.

### Data Cleaning

Several cleaning steps were applied:

* Removing rows without player data
* Converting numeric columns to appropriate types
* Filtering relevant variables for analysis

### Analysis

The project includes several statistical analyses and visualizations:

**1. Correlation Analysis**

The correlation between draft pick and career Win Shares was calculated to measure the strength and direction of the relationship.

**2. Regression Analysis**

A linear regression model was used to estimate how well draft position predicts career Win Shares.

**3. Lottery vs Non-Lottery Comparison**

The draft was separated into:

* Lottery picks (1–14)
* Non-lottery picks (15–60)

This allowed the analysis to examine whether draft position remains predictive within these subsets.

**4. Draft Steal Analysis**

Regression residuals were used to identify players who significantly outperformed or underperformed expectations based on their draft position.

## Key Results

* The correlation between draft pick and career Win Shares was approximately **-0.37**.
* This indicates that **earlier draft picks tend to produce higher career Win Shares**.
* The regression model produced an **R² value of about 0.13**, meaning draft position explains roughly **13% of the variation** in career performance.
* The relationship becomes slightly weaker when examining **lottery and non-lottery picks separately**, suggesting outcomes become more unpredictable further down the draft.

## Conclusion

Draft position does have a statistically significant relationship with long-term NBA success, measured by career Win Shares. Earlier selections tend to produce more valuable players on average.

However, the relationship is only moderate in strength. Draft position explains a relatively small portion of the variation in career outcomes, meaning many other factors influence player development and long-term success.

The presence of both major draft steals and underperforming high picks highlights the uncertainty involved in evaluating basketball talent. While teams improve their odds of selecting productive players with earlier picks, the NBA draft remains an inherently unpredictable process.
