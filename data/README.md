## Data files for COMM3180 Group Project

* DATA: oscars.csv
* 
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
    
