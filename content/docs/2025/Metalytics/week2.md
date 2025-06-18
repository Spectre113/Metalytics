---
title: "Week #2"
---

# **Week #2**

## Detailed Requirements Elaboration

This week, the team focused on clarifying the essential analytical and technical requirements for the MVP, with particular emphasis on the machine learning component. The main efforts were directed toward time series analysis and meaningful feature selection based on available gold market data. 
- **analyzed short-term gold distribution similarity**: a statistical comparison of gold price distributions in Russian and U.S. markets was conducted. It was found that both follow a relatively similar trend structure.
- **time series analysis**: volume distribution analysis, open and close price similarity, high and close as well as low and close price similarities similarities, stationarity hypothesis testing for close price, autocorrelation and partial autocorrelation visualization.
- **feature selection** for short-term forecast: these features include historical prices, market-derived metrics etc.
  
Based on early findings, the team decided to priotize short-term forecasting of gold prices using yechnical indicators. This will serve as primary functionallity of the MVP.


### Prioritized backlog

[Kanban board](https://raw.githubusercontent.com/IU-Capstone-Project-2025/Metalytics/refs/heads/main/Assets/kanban.png)

## Project specific progress

### Frontend

- UI design created for FHD monitors.
- HTML structure is set.
- CSS is configured.
- Header section implemented.

### Backend

- Possible API endpoints written.
- API structure set.

### ML

*...*


# Weekly commitments

## Individual contribution of each participant

- **Vladimir Toporkov** - Wrote second report, created the initial HTML structure for the frontend and outlined the basic CSS classes for future styling. Implemented header section. [Commit link](https://github.com/IU-Capstone-Project-2025/Metalytics/tree/f444cf51d3944f5d30b932c8e054c428f65f0da2/frontend)
- **Farit Sharafutdinov** -  Made justification of the choice of indicators and distribution of the Russian and American markets 
    (showed minor statistical differences in a short period, according to Kolmogorov-Smirnov). [Commit link](https://github.com/IU-Capstone-Project-2025/Metalytics/tree/b2c4c218fd0ed2093aadd709913edf37852d4668/ml/reports)
- **Ilya Grigorev** - Baseline model implemented, selected model for MVP, did an analysis of the characteristics of the time series. [Link to the commit](https://github.com/IU-Capstone-Project-2025/Metalytics/tree/93ce41f1691ca2afeca3f958e92c372c776c19fb/ml/notebooks)
- **Rail Sharipov** - 
- **Askar Kadyrgulov** - 
- **Nikita Solomennikov** - Created the first version of the design in Figma. [Link to the commit](https://github.com/IU-Capstone-Project-2025/Metalytics/tree/509f6572b024702642f3b48c39dac67211d82f0c/Assets) and [Link to figma](https://www.figma.com/design/oqrwNbnmT7rRQNl58pdCmO/Metalytics?node-id=0-1&p=f&t=QLLxiA6znFkthbYE-0)

## Plan for Next Week

- Create UI-kit: start working with animations and color namings.
- Finish FHD frontend part: completed main section and implement UI-kit.
- Implement API: integrate the backend endpoints with the frontend
- Select features for long-term forecast: analyze available datasets and select relevant features that impact long-term trends.
- Deploy the first version of the model: package the current machine learning model and deploy it
- Finish with feature selection fot short-term forecast:  finalize the preprocessing pipeline for short-term prediction.

## Confirmation of the code's operability

We confirm that the code in the main branch:
- [ ] In working condition.
- [ ] Run via docker-compose (or another alternative described in the `README.md`).
