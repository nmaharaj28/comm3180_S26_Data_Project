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