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
    
    
