---
layout: post
title:  Summary of NBA Data and Introduction to Streamlit APP
author: Tanner Campbell
description: This blog post will go over a steamlit app and outcomes for NBA minutes played VS points scored
image: "/assets/images/finalblog.jpg"
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

- **Interactive Visualizations**: The app generates various visualizations like scatter plots, histograms, and box plots to help users explore the relationship between player minutes and their scoring efficiency. For instance, users can interact with a scatter plot that shows how points per game (PPG) correlate with minutes played. This can be valuable for understanding performance patterns over different playing times.

- **Filters**: The app includes several filters that users can adjust to refine the data and focus on specific subsets of players:
  - **Minimum Games Played Filter**: This slider allows users to filter out players who have played fewer than a specified number of games. For example, users can choose to only show players who have played at least 50 games in the season. This ensures that the analysis focuses on players with substantial playing time and reduces the influence of players with only limited game appearances.
  - **Team Filter**: Users can select one or more teams using the multi-select dropdown. This enables users to focus on a specific team or compare multiple teams' players based on the minutes played and points per game.
  - **Points Per Game Range Filter**: The slider for the "Points Per Game" range allows users to specify a minimum and maximum value. This filter helps users narrow down the analysis to players who score within a specific range, allowing them to explore performance differences between high and low scorers.
  After applying these filters, the data is dynamically updated, providing the user with an updated table of players that match the selected criteria.

---
### How the Filters and Graphics Work:

In the app, the filtering system provides a powerful way to hone in on specific players or performance metrics:
1. **Filtering by Games Played**: The "Minimum Games Played" filter helps users focus on players who have sufficient playing time to make their performance data more meaningful. For instance, users can adjust the filter to only include players who have played at least 50 games, eliminating players with low sample sizes.
   
2. **Team Selection**: The multi-select dropdown allows users to choose one or more teams, enabling comparisons between different teams. This is particularly useful for users who want to focus on players from certain teams or compare players from teams with similar performance profiles.
   
3. **Points Per Game Range**: The points per game range slider helps users zoom in on specific performance bands, whether they’re interested in high scorers or players with lower but consistent scoring.

The app’s visualizations react to these filters, ensuring that users only see the data that fits their selected criteria. For example:
- After selecting specific teams or a range of points per game, the **scatter plot** updates to reflect only those players, making it easier to analyze the relationship between minutes and points for the chosen subset.
- The **histograms** and **box plots** also update dynamically to show the distribution of minutes played or points scored for the filtered players, providing insights into player performance across various segments.

---
You can now use the app to explore these relationships and dive deeper into how minutes played affects performance across different teams and player profiles. The flexibility of filtering and interactive visualizations makes this analysis accessible and insightful for anyone interested in NBA player performance.

## Conclusion
This analysis highlights the importance of considering **player efficiency**, not just the raw numbers of minutes played and points scored. While more time on the court generally results in higher scoring, there are diminishing returns once a certain threshold is passed. Additionally, players who are able to score more in fewer minutes, often in key moments, are often the most valuable assets to their teams.

The Streamlit app offers a dynamic way to explore these findings interactively, making it easy for anyone to dive deeper into the data and uncover additional insights. I encourage readers to experiment with the app and see how different factors like position or team strategy influence player performance.

For those interested in replicating this analysis or learning more about the code behind it, check out my [GitHub repository](git@github.com:tannercamp/Blog-Repository-Code.git).

## Further Reading & Resources
- [NBA API Documentation](https://www.basketball-reference.com/)
- [Advanced Basketball Statistics](https://www.basketball-reference.com/)
