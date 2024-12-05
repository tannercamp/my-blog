---
layout: post
title:  Summary of NBA Data and Introduction to Streamlit APP
author: Tanner Campbell
description: This blog post will go over a steamlit app and outcomes for NBA minutes played VS points scored
image: "/assets/images/BasketballDunk.jpg"
---

# Exploring NBA Performance: Points Per Game and Minutes Played

In the NBA, player performance is often analyzed through statistics such as points per game (PPG) and minutes played. In this blog post, I explore the relationship between these two metrics, specifically whether more minutes on the court result in higher scoring. Using data pulled from the NBA API, I analyzed the performance of NBA players to uncover insights into player efficiency and game strategy.

## Key Insights
The analysis revealed a strong positive correlation (0.72) between minutes played and points per game, showing that players who play more minutes tend to score more points. However, the relationship is not linear, with diminishing returns in scoring after a certain amount of playtime. Efficient players, who score more with fewer minutes, are often stars in high-leverage situations.

## Visualizations
Through scatter plots, histograms, and box plots, I visualized the data, offering insights into how players’ minutes correlate with their scoring output. Key visuals included:
- A scatter plot showing a positive correlation between minutes played and PPG.
- Distribution graphs for minutes played and PPG, highlighting the typical range of player statistics.
- A box plot to identify scoring outliers, revealing that most players scored between 5-30 PPG.

## Streamlit App Introduction

To explore these insights interactively, I’ve created a Streamlit app that allows users to explore the data in more detail. The app includes:
- **Interactive visualizations**: Users can view relationships between minutes played and PPG for various players.
- **Filters**: Select specific players or adjust the range of minutes played to see how these factors affect scoring.
- **Player comparisons**: Compare different players’ statistics in an easy-to-understand format.

You can interact with the app [here](https://wfy8gwdejd7cnlmxqpoxwr.streamlit.app/), where you can explore the data and discover additional trends.

## Conclusion
This analysis emphasizes the importance of player efficiency, showing that while playing more minutes can lead to higher scoring, other factors like player role and team strategy must also be considered. The Streamlit app lets you explore these relationships in-depth, providing further insights into NBA performance.

For those interested in replicating the analysis or exploring the code behind it, check out my [GitHub repository](git@github.com:tannercamp/Blog-Repository-Code.git).

My App: https://wfy8gwdejd7cnlmxqpoxwr.streamlit.app/