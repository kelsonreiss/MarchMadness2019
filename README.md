

## Overview
This repo contains my work for the 2019 Kaggle March Madness competition - research, practice Jupyter notebooks, and code creating final model for submission. I entered this competition to learn and practice ML programming, focusing on something that I was interested in - college basketball. I ended up placing in the **top 25%** of all submissions. A link to the competition can be found [here](https://www.kaggle.com/c/mens-machine-learning-competition-2019/overview). 

## Model Info
Model #1 - found in Seeds_and_Ordinals.ipynb - was an XGBoost classifier trained on tournament seed and Massey Ordinal data. I chose these variables primarily for their simplicity. Massey Ordinals are based on a ranking methodology pioneered by Kenneth Massey that take into account a team's strength of schedule that allow for head to head statistical comparisons by assigning each team a rating. By using the ordinals + the seeds, I wanted to combine basketball experts' knowledge with data analysis.

Model #2 - found in Weighted_Massey.ipynb - was a statistical approach using only Massey Ordinals. I found a [post] (https://www.kaggle.com/c/march-machine-learning-mania-2014/discussion/6777) by Jeff Sonas that details applying his Chessmetrics rating system to college basketball. The goal behind the formula can be glimpsed from this quote by Sonas:

> It is important to acknowledge that not all points are created equal - the difference between a two-point win and a two-point loss, is surely more meaningful than the difference between a 34-point win and a 30-point win. 

I implemented this formula to generate my predictions. This was actually the best performing model, achieving a **0.47682** LogLoss value (for comparison, 0.46007 was the cutoff for top 10%). 

