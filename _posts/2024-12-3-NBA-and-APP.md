---
layout: post
title:  Summary of NBA Data and Introduction to Streamlit APP
author: Tanner Campbell
description: This blog post will go over a steamlit app and outcomes for NBA minutes played VS points scored
image: "/assets/images/BasketballDunk.jpg"
---

# Exploring NBA Performance: Points Per Game and Minutes Played

In the NBA, player performance is often analyzed through statistics such as points per game (PPG) and minutes played. While many focus on scoring alone, the correlation between minutes on the court and a player’s scoring output is a lesser-discussed topic. In this blog post, I dive into this relationship, exploring whether players who spend more time on the court tend to score higher points. I used the NBA’s extensive player statistics to uncover insights that can influence coaching strategies, team lineups, and player evaluations. 

## Key Insights
From the data, a few trends emerged that were both expected and surprising. The most notable finding was that **minutes played and points per game have a strong positive correlation**, but with diminishing returns after a certain point. Specifically, while players who log more minutes tend to score more points, the increase in points per game slows down as minutes increase. This could suggest that while extra playing time contributes to higher scoring, other factors—such as player fatigue, the efficiency of shooting, or team strategies—become more influential as the minutes rack up.

One additional insight was that **efficient players**—those who score highly despite playing fewer minutes—tend to be the stars of their teams. These players might play in high-leverage situations, such as during critical moments in the game, where scoring opportunities are more concentrated. This insight could suggest a strategic approach where coaches focus on leveraging star players in shorter bursts rather than relying solely on playing time.

## Visualizations
To visualize the relationship between minutes played and points per game, I employed several techniques in exploratory data analysis (EDA). Each visualization provided a unique perspective on the data:

### Scatter Plot
A scatter plot revealed the overall trend between minutes played and points scored. The plot showed that there is indeed a positive correlation between these two variables. However, as we moved to higher values of minutes played, the points per game did not continue to increase linearly. In fact, the trend started to flatten, indicating that more minutes don't always equate to more points.

  <figure>
    <img src="https://tannercamp.github.io/my-blog/assets/images/blog3pic1.jpg" alt="">
  </figure>

### Distributions
Histograms of minutes played and PPG showed that the majority of NBA players log between 20 and 40 minutes per game. Interestingly, these two distributions had a similar shape, suggesting that most players are in the middle range for both metrics. At the extremes, however, there were outliers. A few players logged well over 40 minutes per game, while others played very little but scored high in the limited minutes they had.

  <figure>
    <img src="https://tannercamp.github.io/my-blog/assets/images/blog3pic2.jpg" alt="">
  </figure>

  <figure>
    <img src="https://tannercamp.github.io/my-blog/assets/images/blog3pic3.jpg" alt="">
  </figure>

### Box Plot
A box plot was useful for identifying outliers in points per game. Most players had scores between 5 and 30 PPG, but a few players scored exceptionally high, further emphasizing the impact of star players who might play fewer minutes but deliver high performance when on the court.

  <figure>
    <img src="https://tannercamp.github.io/my-blog/assets/images/blog3pic4.jpg" alt="">
  </figure>

### Correlation
To quantify the relationship between minutes played and points per game, I computed the Pearson correlation coefficient, which was found to be **0.72**. This strong positive correlation indicates that more minutes played is indeed associated with higher scoring, but with the previously mentioned diminishing returns at higher minute thresholds.

  <figure>
    <img src="https://tannercamp.github.io/my-blog/assets/images/blog3pic5.jpg" alt="">
  </figure>

## Streamlit App Introduction

To make this analysis more interactive, I developed a Streamlit app that allows users to explore the data themselves. The app includes a variety of features designed to provide deeper insights into the relationship between minutes played and points per game.

### Features of the Streamlit App:
- **Interactive visualizations**: Users can view scatter plots, histograms, and other visualizations to explore the data interactively.
- **Filters**: The app lets users filter the data by player position, team, or specific ranges of minutes played. This is helpful for users who want to drill down into particular groups of players or performance levels.
- **Player Comparisons**: The app also enables users to select multiple players and compare their performance metrics side by side. This feature can help users understand how different players, such as stars versus role players, compare in terms of scoring efficiency.
  
You can interact with the app [here](https://wfy8gwdejd7cnlmxqpoxwr.streamlit.app/), where you can explore the data and discover trends that may not be immediately apparent from a static analysis.

### Exploring the Data:
When using the app, start by adjusting the slider for minutes played to see how it affects the distribution of points per game. You can also filter for positions such as guards, forwards, or centers to observe how these roles differ in terms of playing time and scoring efficiency. As you interact with the data, you’ll be able to uncover further insights into player performance, which can aid in making better decisions for team strategies.

## Conclusion
This analysis highlights the importance of considering **player efficiency**, not just the raw numbers of minutes played and points scored. While more time on the court generally results in higher scoring, there are diminishing returns once a certain threshold is passed. Additionally, players who are able to score more in fewer minutes, often in key moments, are often the most valuable assets to their teams.

The Streamlit app offers a dynamic way to explore these findings interactively, making it easy for anyone to dive deeper into the data and uncover additional insights. I encourage readers to experiment with the app and see how different factors like position or team strategy influence player performance.

For those interested in replicating this analysis or learning more about the code behind it, check out my [GitHub repository](git@github.com:tannercamp/Blog-Repository-Code.git).

## Further Reading & Resources
- [NBA API Documentation](https://www.basketball-reference.com/)
- [Advanced Basketball Statistics](https://www.basketball-reference.com/)
