<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/jagan-hero-dark.svg">
    <img src="assets/jagan-hero-light.svg" alt="Jagan Ambati, Data Analyst" width="100%">
  </picture>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ambati-jagan2002/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://thriving-dragon-b028c4.netlify.app"><img src="https://img.shields.io/badge/Portfolio-12395A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"></a>
  <a href="mailto:ambatijaganreddyj@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

I turn raw data into validated, well-modeled dashboards that stakeholders can act on. My work centres on data validation, Power BI dashboards and clear reporting.

## About me

- 📍 Based in Hyderabad, India, working at iLogitek Business Solutions
- I build Power BI dashboards, from Power Query cleaning to DAX measures and star-schema models
- I use SQL and Google BigQuery to extract, transform and analyse data
- I use Python (Pandas, NumPy) for cleaning and exploratory analysis
- B.Tech in Electronics & Communication Engineering, 2025

## Tech stack

| Category | Tools |
|---|---|
| BI and visualization | Power BI (Power Query, DAX, data modeling), Tableau, Excel |
| Databases and querying | SQL, Google BigQuery |
| Programming | Python: Pandas, NumPy, Matplotlib, Seaborn |
| Data preparation | Alteryx, Power Query |

## Featured projects

| Project | What I did | Tools | Link |
|---|---|---|---|
| **Salesman Performance Dashboard** | Analysed sales trends, target achievement, revenue, customer acquisition and regional performance | Excel | [Repo](https://github.com/Ambati4422/Salesman-performance-dashboard-excel-) |
| **Sales Performance Dashboard with DAX** | Built DAX measures and visuals for sales trends, target achievement and sales by city | Power BI, DAX | [Repo](https://github.com/Ambati4422/Dax-visualization-in-power-bi) |
| **Healthcare Data Analysis** | Cleaned and transformed healthcare data to find trends and improve data quality | Excel | [Repo](https://github.com/Ambati4422/Health-care-data-analyis) |

<!--
Add more rows once each project has its own repository. Template:
| **Project name** | One line on what you did | Tools | [Repo](https://github.com/Ambati4422/REPO-NAME) |
Candidates from your old README: Digital India Performance Dashboard, HRMS Market Analysis,
Mobile Accessories Demand Analysis, Hotel Management Analytics.
-->

## How I work

Collect, clean, validate, model, analyse with SQL, visualise in Power BI, then present the insights.

## Currently learning

Advanced DAX, advanced SQL and Tableau.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Ambati4422/Ambati4422/output/github-contribution-grid-snake-dark.svg">
    <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/Ambati4422/Ambati4422/output/github-contribution-grid-snake.svg">
  </picture>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/footer-dark.svg">
    <img src="assets/footer-light.svg" alt="Turning data into insights, one dashboard at a time" width="100%">
  </picture>
</p>
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}





