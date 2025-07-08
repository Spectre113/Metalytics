---
title: "Week #5"
---

# **Week #5**

## Feedback

### Sessions

During this week team conducted 3 sessions with potential neutral users to get objective observations. The following questions in telegram were asked:
1. Насколько понятным для вас был интерфейс?
2. Насколько удобно было пользоваться сервисом в целом?
3. Насколько вы довольны качеством предсказания/анализа?
4. Есть ли что-то, что вызвало трудности или осталось непонятным?
5. Что бы вы улучшили в интерфейсе или функциональности?

**Below are the quotes!!!**

---

#### **Dmitry Ivanov (Experienced investor):**

1. Интерфейс понятен и достаточно прост. Но есть некоторые моменты, которые я бы поменял для удобства.  
2. По шкале от 1 до 10 — на 7. Я бы перенес новости над графиком и сделал их в виде постов, которые можно скроллить. Так они не будут перекрывать график и будут удобны для ознакомления.  
3. Пока не могу оценить предсказание, т.к. не пробовал использовать сигналы системы для реальной торговли. Но их отображение удобно смотреть — это факт.  
4. Была трудность с переключением типов металлов, но потом объяснили, что пока работает только золото.  
5. Добавил бы отображение рисков и подтягивание реального графика котировок в режиме онлайн.

Tg - @Dimas_PhT

---

#### **Eugene Marchuk (Engineer):**

1. Скорее всего, понятен. 🤔  
2. Интуитивно понятно. 👍  
3. Как будто, далеко от истины... 🤔  
4. При попытке нажать на кнопки "серебро" и "цинк" выводятся графики для золота и предыдущая статистика/прогноз. 👎  
5. Для статистики и прогнозов на неделю, месяц, год стоят плашки "в настоящий момент не доступно". Возможно, стоит разместить такие же плашки на кнопках серебра и цинка. Либо починить графики для серебра и цинка.

Tg - @eugene_marchuk

---

#### **Vladimir Bazilevich (ML engineer):**

1. Интерфейс весьма простой и понятный.  
2. Имею опыт работы с QUIK — очень топорный инструмент с точки зрения модности дизайна, но в плане отображения данных с ним тяжело тягаться. Анимации на графике при наведении на точку (особенно когда смотришь несколько соседних) скорее мешают.  
   Чтобы разобраться в оси времени, приходится читать целиком весь лейбл. В том же QUIK общая часть метки агрегирована — часовые метки и под ними общая дата. Сам по себе график с точки зрения торгов не достаточно информативен — нет цен открытия и закрытия. Свечи более информативны, чем точки с интерполяцией.  
3. Какой-то тренд показало, но опять же вопросы к лейблам наа оси стоимости.
4. Сетка недостаточно контрастирует — приходится напрягать глаза, чтобы её рассмотреть. Сетка важна при сопоставлении разных моментов во времени, особенно учитывая дискретность меток времени.  
5. 
   1. Новости можно отображать как всплывающие окошки на графике, открывать по клику или ховеру.  
   2. Мета-информацию по новостям (время публикации, источник) вынес бы в начало заметки.  
   3. В целом глаза устают от интерфейса.  
   4. Вещи, которые не готовы, думаю, лучше спрятать — раздражают своим отсутствием.  
   5. Прокрутка новостей слишком мелкая — сложно заметить сами кнопки, активная область маленькая.

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

### Documentation

*Describe what types of documentation you have in your project, and why exactly are they?*

### ML Model Refinement

*If applicable: Describe the process of improving the quality of your ML model, how you managed to achieve this and how you plan to improve it further.*

# Weekly commitments

## Individual contribution of each participant

From Friday to Monday:
- **Vladimir Toporkov** - 
- **Farit Sharafutdinov** -  
- **Ilya Grigorev** - 
- **Rail Sharipov** - 
- **Askar Kadyrgulov** - 
-  **Nikita Solomennikov** -

From Monday to Wednesday:
- **Vladimir Toporkov** - 
- **Farit Sharafutdinov** -  
- **Ilya Grigorev** - 
- **Rail Sharipov** - 
- **Askar Kadyrgulov** - 
-  **Nikita Solomennikov** -

## Plan for Next Week

*...*

## Confirmation of the code's operability

We confirm that the code in the main branch:
- [ ] In working condition.
- [ ] Run via docker-compose (or another alternative described in the `README.md`).
