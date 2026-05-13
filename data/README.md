## Data files for COMM3180 Group Project

* 1: oscars.csv

Source: https://github.com/DLu/oscar_data
A curated dataset of Academy Award nominations with IMDb unique identifiers.  Contains all Oscar ceremonies from the 1st through the most recent, including every nomination and win across all categories.  One row per nomination.

Key fields:
  Ceremony         - Ordinal ceremony number (1 = first ever)
  Year             - Film year(s) being honored
  Class            - Broad category group (Acting, Directing, Writing, Music, etc.)
  CanonicalCategory- Standardized category name across years
  Film / FilmId    - Title and IMDb title ID (tt...)
  Name             - Nominee as listed by the Academy
  Nominees /
  NomineeIds       - Cleaned nominee name(s) and IMDb person/company IDs (nm...)
  Winner           - Boolean: True if the award was won
  Detail           - Extra info (character name, song title, etc.)

Notes:
  - Fields like Film, Nominees, and NomineeIds can contain multiple
    pipe-separated values (|) when a nomination involves multiple entities.
  - Unknown IMDb IDs are represented with a question mark (?).
  - Race/ethnicity is not included.

* 2: oscars_demographics.csv

Source: https://www.kaggle.com/code/roqeeb/racial-diversity-of-the-oscars/input
Academy awards nominations and winners, with race and gender of all.

Key Fields:
  year_ceremony
  Category
  gender
  name
  Race
  film
  winner (TRUE or FALSE)

Notes:
  - Missing data after 2020

* 3: oscars_demographics_comprehensive.csv

Source: Combinaiton of oscars.csv and oscars_demographics using claude.ai

Key Fields:
  year_ceremony
  Category
  gender
  name
  Race
  film
  winner (TRUE or FALSE)

Notes:
  - Using Claude, we brought the winners and nominees from the 2020s into the dataset containing demographic information
  - Then, using an Anthropic AI API, Claude searched for and filled in the gender- and race- related information into this new spreadsheet
  - Middle Eastern individuals are classified as White
  - ** A sample of X number of rows filled in by Claude will be hand-checked for accuracy

* 4: oscars_religion_orientation.csv
A supplementary dataset of 441 Oscar winners (1927–2014) crowd-coded via CrowdFlower, containing additional demographic attributes not found in the main nominations file: religion, sexual_orientation, race_ethnicity, birthplace, and date_of_birth. Each attribute includes a :confidence score reflecting inter-coder agreement. Religions recorded include Roman Catholic, Jewish, Atheist, and Baptist; orientations include Straight, Bisexual, Gay, and Lesbian. Note this dataset covers winners only, not all nominees, and ends at 2014 — treat it as supplementary context rather than a primary analysis dataset.

* 5: enhanced_box_office_data_2000-2024_u.csv
Box office performance data for the top 200 grossing films per year from 2000–2024 (5,000 rows). Columns include Release Group, $Worldwide, $Domestic, $Foreign (and their percentage splits), Year, Genres, Rating, Vote_Count, Original_Language, and Production_Countries. Used in oscars_box_office.ipynb to join against Oscar nominee records by film title and compare the commercial performance of nominated films against mainstream blockbusters.

* 6: oscarssowhite_tweets_2015-2022.csv
The full tweet-level dataset: 11,724 tweets containing oscarssowhite collected from the ASC/Wharton 1% daily Twitter sample between January 2015 and September 2022. Contains 63 columns including full tweet text (extended_full_text and text), user metadata (user_screen_name, user_followers_count, user_verified, user_location), engagement metrics (retweet_count, favorite_count, reply_count), retweet fields (rt_extended_full_text, rt_user_name), and parsed date fields (year, month, day, hour). This is the source file for the content coding and sentiment analysis in _OscarsSoWhite_Audience_Discussion.ipynb.

* 7: oscarssowhite_timeline_2015-2022.csv
A daily aggregated count of tweets containing oscarssowhite from the 1% Twitter sample, covering 709 sampled days between 2015 and 2022 (11,724 total tweets across those days). Columns: year, month, day, date, count. Used to plot the timeline of campaign activity and annotate spikes against real-world Oscar events. Derived from the same archive as the full tweet file above but pre-aggregated for easier time series plotting.

* 8: example_twitter_timeline_OSCARS.csv
A daily count of tweets containing the broader string oscars (not oscarssowhite) from the 1% Twitter sample, covering 2,115 days from 2017–2022. Columns: year, month, day, date, count. Used in example_twitter_sample_data.ipynb as a demonstration of how to work with the archive's date-structured CSV exports. Because the search term is general, this file captures all Oscar-adjacent discussion — ceremonies, nominations, controversies, celebrity coverage — not just diversity-related tweets. Treat it as a measure of overall Oscar public attention rather than #OscarsSoWhite engagement specifically.