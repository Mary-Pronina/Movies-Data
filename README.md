# Movies Data Analysis Project

## Table of Content
 - [Project Overview](#project-overview)
 - [Data Sourses](#data-sourses)
 - [Tools](#tools)
 - [Data Ckeaning and Preparation](#data-cleaning-and-preparation)
 - [Exploratory Data Analysis](#exploratory-data-analysis)
 - [Results and Findings](#results-and-findings)
 - [Challenges in Analysis](#challenges-in-analysis)

## Project Overview

This data analysis project focuses on uncovering insights into the performance and trends of movies released between 2012 and 2016. By examining various aspects of the movie data, we aim to identify patterns, provide data-driven recommendations, and gain a deeper understanding of the industry's dynamics.

## Data Sourses
For this analysis, the primary dataset is the "Movie Data Project.xlsx" file. It contains detailed information on each movie's performance, including data on actors, directors, genres and other relevant details.
[Movies Data Homework.xlsx](https://github.com/user-attachments/files/16415861/Movies.Data.Homework.xlsx)

### Tools
-Power Query- I used Power Query for Data Cleaning
-Excel, Pivot Table- I used them for Data Analysis, Crating reports and Visualisation

### Data Cleaning and Preparation
In the initial data preparation phase, we perfomed the following tasks:
-Data loading and inspection.
-Handling errors, missing values.
-Data Cleaning and formatting.

### Exploratory Data Analysis
During the exploratory data analysis phase, we addressed several key questions:
-Which genres were the most profitable during these years?
-Which actors achieved the most success?
-How did the budget and return on investment (ROI) impact the movies' performance?
-What trends can be observed in the box office revenues?
-Which directors consistently delivered high-grossing movies?
-How did the release dates affect the movies' box office success?

### Results and Findings

As an example:
Best profitable movie was with Budget of

![Best Movie](https://github.com/user-attachments/assets/4743f645-2d5e-4c8c-8c08-6e2ead403f14)

Best genre of this movie was 


The best actor was




### Challenges in Analysis
#### M Language
One of the interesting features/challenges I worked on involved using M Language to group and combine genres for future analysis. Initially, I had two columns for genres, but I needed to merge them into a single column with a consistent format (e.g., action/comedy) and ensure the genres were listed in alphabetical order.

```= Table.Group(#"Renamed Columns1", {"Movie Title"}, {{"Combined Genre", each Text.Combine ([Concat Genre], " / "), type text}, {"All Rows", each _, type table [Release Date=nullable date, Wikipedia URL=nullable text, Concat Genre=nullable text, Director=nullable text, Actor=nullable text, Actor.1=nullable text, Actor.2=nullable text, Actor.3=nullable text, #".Actor.4"=nullable text, #"Budget ($)"=nullable number, #"Box Office Revenue ($)"=nullable number]}})```
