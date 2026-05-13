## Data analysis notebooks for COMM3180 Group Data Project

* This folder should contain the a series of Jupyter notebooks you create to do the data analysis.

* Update this `README.md` file to document the notebooks and give a short description of what each one does.

1. oscar_demographics_analysis

In this file, you'll be able to see several graphs relating to a demographic anlaysis of Oscar winners and nominees. The majority of these graphs will be included in our final project, as they provide valuable insight into the ceremony's disproportionate favoring of white men.

2. **oscars_box_office**
   This notebook examines the relationship between Oscar nominations, lead actor/actress race, and box office performance from 2000 to present. It uses two datasets: `oscars_demographics_comprehensive_2.csv` (nominee demographics across all ceremonies) and `box_office.csv` (domestic and worldwide gross for the top 200 grossing films per year). The notebook is organized into three analysis blocks:

   - **Nomination Diversity Over Time:** Tracks the percentage of POC nominees in acting and directing categories by decade (historical baseline) and year by year from 2000 to present. Runs a chi-square test to assess whether the shift in POC nominations after the 2016 #OscarsSoWhite campaign is statistically significant.

   - **Box Office Performance & Lead Race:** Compares domestic and worldwide gross for Best Picture nominees split by lead race (POC vs. White) and era (pre-2016 vs. post-2016). Includes Mann-Whitney U tests and an OLS regression with a `POC × post-2016` interaction term to assess whether diverse-led films earned differently after the Academy's diversity reforms.

   - **All Major Categories & Commercial Gap:** Extends the gross-by-race comparison across all major award categories (Best Picture, Actor/Actress in Leading and Supporting roles, Directing). Also includes a year-by-year comparison of Best Picture nominee median gross versus the top 10 highest-grossing films each year, showing whether Oscar films track or diverge from mainstream commercial blockbusters and whether that gap changed after 2016.
  
3. #OscarsSoWhite Audience Discussion

This notebook analyzes public discourse around the #OscarsSoWhite movement using a sample of tweets collected between 2015 and 2022 (oscarssowhite_tweets_2015-2022.csv). It uses a hybrid human + AI content coding approach to categorize tweets by stance, then visualizes how that discourse evolved over time. The notebook is organized into two main blocks:

4.  example_twitter_sample_data.ipynb
This notebook demonstrates how to work with exports from the ASC/Wharton Historical Twitter Archive — a daily 1% random sample of all tweets posted between 2012 and 2022 — to build tweet volume timelines relevant to the Oscars and #OscarsSoWhite. It uses two data sources: data/example_twitter_timeline_OSCARS.csv (daily counts of any tweet containing oscars, 2017–2022) and data/oscarssowhite_timeline_2015-2022.csv (daily counts of tweets containing oscarssowhite, 2015–2022), plus the full tweet text file oscarssowhite_tweets_2015-2022.csv (~12,000 tweets). The notebook is organized into three blocks.