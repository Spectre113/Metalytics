---
title: "Week #5"
---

# **Week #5**

## Feedback

### Sessions

During this week team conducted 3 sessions with potential neutral users to get objective observations. The following questions in telegram were asked:
1. How clear was the interface for you?
2. How convenient was it to use the service as a whole?
3. How satisfied are you with the quality of the prediction/analysis?
4. Is there anything that caused difficulties or remained unclear?
5. What would you improve in the interface or functionality?

**Below are the quotes!!!**

---

#### **Dmitry Ivanov (Experienced investor):**

1. The interface is clear and quite simple. But there are some things that I would change for convenience.  
2. On a scale from 1 to 10 — by 7. I would move the news above the chart and make them into posts that can be scrolled. This way they will not overlap the chart and will be convenient for familiarization.
3. I cannot evaluate the prediction yet, because I have not tried to use the system's signals for real trading. But their display is convenient to watch — that's a fact.  
4. There was a difficulty switching the types of metals, but then they explained that so far only gold is working.  
5. I would add a risk display and a pull-up of the real quotation chart online.

Tg - @Dimas_PhT

---

#### **Eugene Marchuk (Engineer):**

1. Most likely, it is understandable. 🤔  
2. Intuitive. 👍  
3. As if it were far from the truth... 🤔  
4. When you try to click on the "silver" and "zinc" buttons, the charts for gold and the previous statistics/forecast are displayed. 👎  
5. For statistics and forecasts for the week, month, and year, there are "currently unavailable" bars. It might be worth placing the same bars on the silver and zinc buttons. Or fix the graphs for silver and zinc.

Tg - @eugene_marchuk

---

#### **Vladimir Bazilevich (ML engineer):**

1. The interface is very simple and intuitive.  
2. I have experience working with QUIK, which is a very clumsy tool in terms of design fashion, but it's hard to compete with it in terms of data display. Animations on the graph when hovering over a point (especially when looking at several neighboring ones) rather, they interfere.  
   To understand the time axis, you have to read the entire label. In the same QUIK, the general part of the label is aggregated — the hour markers and the general date under them. The chart itself is not informative enough from the point of view of trading — there are no opening and closing prices. Candlesticks are more informative than points with interpolation.  
3. It showed some kind of trend, but again, questions for labels on the value axis.
4. The grid doesn't contrast enough — you have to strain your eyes to see it. The grid is important when comparing different points in time, especially considering the discreteness of the timestamps.  

5.
   1. News can be displayed as pop-up windows on the chart, opened by click or hover.  
   2. Meta-information on the news (time of publication, source) would be placed at the beginning of the note.  
   3. In general, the eyes get tired of the interface.  
   4. Things that are not ready, I think it's better to hide — they annoy by their absence.  
   5. The scrolling of the news is too shallow — it is difficult to notice the buttons themselves, the active area is small.

Tg - @vbazilevich

### Analyze

After analyzing feedback from three independent users, the following key conclusions were drawn:

1. **Interface**  
   The interface was generally rated as clear and simple. However, users pointed out that:  
   - Visual comfort needs improvement — the interface **strains the eyes**;  
   - A more flexible or adaptive UI design is recommended to reduce eye strain;  
   - The **chart grid lacks contrast**, making it difficult to read, especially when comparing points in time;  
   - The **time axis is hard to interpret** — labels are too verbose. Consider **aggregated time formatting**, like in the QUIK terminal.

2. **Chart and Data Visualization**  
   The current chart implementation was seen as **insufficiently informative** for trading purposes:
   - Replace the line/point chart with a **candlestick chart** to show open, close, high, and low prices;
   - **Disable or simplify hover animations**, which interfere with the analysis of nearby data points;
   - Improve **axis formatting**, especially the time axis, to enhance readability.

3. **Metal Type Switching**  
   Users encountered issues when switching between metals (silver, zinc):
   - Some buttons display incorrect or duplicate data (gold data shown for silver);
   - If data for a metal is not available, clearly show a **"not available" placeholder** to avoid confusion.

4. **News Section and Contextual Information**  
   Feedback indicated the need for structural changes in the news display:
   - Move **meta-information** (publication time and source) to the **top of each news item**;
   - Consider displaying news as **tooltips or pop-ups** on the chart tied to relevant events;
   - Place the news section **away from the chart**, so it does not block important data;
   - **Scrollbar and buttons** for news are too small — users had difficulty interacting with them.

5. **Prediction Model and Analysis**  
   Feedbach showed that model need to be updated with the graph itself:
   - Improve prediciton status.

6. **Technical Functionality**  
   Several technical issues and recommendations were mentioned:
   - Ensure the **database is correctly synchronized**, so all charts and news reflect up-to-date data;
   - **Hide or disable non-functional elements**, rather than showing inactive buttons or placeholders — this avoids user frustration.


## Iteration & Refinement

### Implemented features based on feedback

Taking into account the user feedback, the following improvements were made:
- LSTM model improved.
- Interface updated: now silver and zinc data are shown; buttons for predictions on silver and zinc are disabled when not available.
- The database is properly configured.
- All buttons are now either clickable or disabled; no unused or confusing buttons remain.

### Performance & Stability

**Frontend and backend metrics:**
- Website availability: users can easily access the website via the provided link.
- Interface: users can select metals of interest, explore both historical and predicted graphs, and view parsed news.
- Backend: users see dynamic graphs where historical prices update automatically, predictions update dynamically, and news updates are reflected timely.

**Ml metrics:**

### Documentation

*Describe what types of documentation you have in your project, and why exactly are they?*

### ML Model Refinement

*If applicable: Describe the process of improving the quality of your ML model, how you managed to achieve this and how you plan to improve it further.*

# Weekly commitments

## Individual contribution of each participant

From Friday to Monday:
- **Vladimir Toporkov** - [Different resolutions implemented](https://github.com/IU-Capstone-Project-2025/Metalytics/pull/83).
- **Farit Sharafutdinov** -  [Collected features for silver](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/c963ca8c9cf115c31415c50603dbc81de7f36d9a/ml/data_loader.py).
- **Ilya Grigorev** - [Improved LSTM model](https://github.com/IU-Capstone-Project-2025/Metalytics/tree/0fd5aa930fffba07f22c22e0d2449030a6b984e8/ml/lstm_model).
- **Rail Sharipov** - [Collected features for zinc](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/afcea3ace351e0df63a9946fea6134879f6d8801/ml/reports/Zinc%20features%20report.pdf).
- **Askar Kadyrgulov** - [Zinc and silver for hitorical data added](https://github.com/IU-Capstone-Project-2025/Metalytics/blob/e5cc392026c8c75ffb24cb06e7131e3125b32c3c/backend/main.py).
-  **Nikita Solomennikov** - [Improved figma design, added additional waypoint resolution](https://www.figma.com/design/oqrwNbnmT7rRQNl58pdCmO/Metalytics?node-id=136-382&t=xR7dRTgYt5kFhtMQ-0), started working with database.

From Monday to Wednesday:
- **Vladimir Toporkov** - [Implemented the news output from the backend to the screen](https://github.com/IU-Capstone-Project-2025/Metalytics/pull/90)
- **Farit Sharafutdinov** -  [Collected dataset for silver](https://github.com/IU-Capstone-Project-2025/Metalytics/commit/1ef2f30dda886baa012fec33b8d28b264d962a5b).
- **Ilya Grigorev** - [Added filter and refined models](https://github.com/IU-Capstone-Project-2025/Metalytics/commit/8646938b93559dfaba0e765f9edf003c747b0405), [upgraded baseline model](https://github.com/IU-Capstone-Project-2025/Metalytics/commit/4eeaf1ad02be72ecee0bbcd9c31c2443a4df7d61) and [upgraded LSTM model](https://github.com/IU-Capstone-Project-2025/Metalytics/commit/8f971edb5a9d2f3652d9f943cdb25f1b54b6cb5a)
- **Rail Sharipov** - [Collected dataset for zinc](none).
- **Askar Kadyrgulov** - [Updated model in backend](https://github.com/IU-Capstone-Project-2025/Metalytics/commit/727f0d5d4e71f412c8b7948d49417dc5b9607a6a).
-  **Nikita Solomennikov** - [Calibrated db on the server](none).

## Plan for Next Week

*...*

## Confirmation of the code's operability

We confirm that the code in the main branch:
- [ ] In working condition.
- [ ] Run via docker-compose (or another alternative described in the `README.md`).
