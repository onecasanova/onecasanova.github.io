---
layout: post
title: "US Housing Affordability Heatmap"
date: 2026-02-18 -0500
permalink: /projects/housing-heatmap
categories: projects
---

## What
An interactive choropleth map visualizing housing affordability across all 50 US states and Washington D.C. The affordability index is calculated as the ratio of median home value to median household income, using data from the U.S. Census Bureau's American Community Survey.

## How
A Python script fetches live data from the Census Bureau ACS API, computes the price-to-income ratio for each state, and generates a self-contained HTML page with an interactive Plotly.js map. Hover over any state to see its median income, median home value, and affordability ratio.

<iframe src="{{ site.baseurl }}/assets/Housing_Heatmap/housing_heatmap.html" width="100%" height="850" style="border: none; border-radius: 8px;"></iframe>

## Key Findings
- States like Hawaii and California consistently have the highest price-to-income ratios, making them the least affordable.
- Midwestern and Southern states tend to have the most affordable housing relative to income.
- The national median ratio provides a useful benchmark for comparing individual states.

## Data Source
U.S. Census Bureau American Community Survey — Variables: B19013_001E (median household income), B25077_001E (median home value).
