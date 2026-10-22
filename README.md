# RoofTrend

**Canadian New Housing Price Analyzer.** RoofTrend compares Statistics Canada's New Housing Price Index across Canadian regions, with significance tests and simple forecasts.

**Status:** rebuild in progress. I first built this in 2023 as a Java Swing university project. This repo is a from-scratch rebuild with a real data pipeline, a cleaner design, and tests.

## The data

[Statistics Canada, New Housing Price Index](https://www150.statcan.gc.ca/n1/en/surveys/2310), table 18-10-0205-01: monthly price indexes for new homes across Canada, the provinces, and major metro areas.

## Plan

- [ ] **1. Data.** A Java client for Statistics Canada's Web Data Service that loads the monthly index into a normalized MySQL schema (regions, series, monthly values), built with Maven.
- [ ] **2. Analysis and design.** Region-to-region comparison, t-tests for whether two regions' trends really differ, and a simple forecast such as linear regression. Organized as MVC, using Observer so views update when data changes and Factory to create charts and analyses.
- [ ] **3. Tests and CI.** JUnit tests running in GitHub Actions on every push.
