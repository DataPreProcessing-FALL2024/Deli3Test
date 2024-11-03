# Deli3Test

## This is my third deliverable.
The cleaning and formatting were both done in R Studio. I included the code for both datasets in CleaningAndFormattingCode-Deliv3.qmd.

You can see the vertical concatenation/merge code here- https://datapreprocessing-fall2024.github.io/Deli3Test/.

### Kitchen Nightmares Data
I made this messy dataset from a more polished dataset I created. The information found in the data was aggregated from multiple sources, including but not limited to:

- https://en.wikipedia.org/wiki/Kitchen_Nightmares
- https://www.realitytvrevisited.com/2013/01/list-of-all-episodes-posts.html
- https://www.kitchennightmaresupdates.com/p/all-kitchen-nightmares-updates.html.

#### Data Set Info
VARIABLES:
* 'SEASON' : Season #
* 'EPISODE' : Episode #
* 'RESTAURANT' : Restaurant name
* 'CITY' : City restaurant is located in
* 'STATE' : State restaurant is located in
* 'AIR_DATE' : Original air date
* 'STATUS' : Status of restaurant- open or closed?
* 'FILM_MONTH' : Original film month and year
* 'CLOSE_YEAR' : Year the restaurant closed
* 'CUISINE' : Type of cuisine served at restaurant
* 'REVISITED' : Yes if restaurant was revisited in later episode, no if not
* 'TWO_PARTS' : Yes if restaurant was featured in two separate episodes, no if not

### Hotel Hell Data
I made this messy dataset from a more polished dataset I created. The information found in the data was aggregated from multiple sources, including but not limited to:

- https://en.wikipedia.org/wiki/Hotel_Hell
- https://www.realitytvrevisited.com/2013/06/hotel-hell-open-or-closed.html.

#### Data Set Info
VARIABLES:
* 'SEASON' : Season #
* 'EPISODE' : Episode #
* 'HOTEL' : Hotel name
* 'CITY' : City hotel is located in
* 'STATE' : State hotel is located in
* 'AIR_DATE' : Original air date
* 'STATUS' : Status of hotel- open or closed?
* 'FILM_MONTH' : Original film month and year
* 'CLOSE_YEAR' : Year the hotel closed
* 'TWO_PARTS' : Yes if hotel was featured in two separate episodes, no if not

### Merging/Concatenation Steps
1. Read in cleaned/formatted Kitchen Nightmares data from Github link.
2. Read in cleaned/formatted Hotel Hell data from Github link.
3. Rename 'restaurant' and 'hotel' columns to 'name' in both data frames.
4. Remove 'cuisine' and 'revisited' columns in KN data.
5. Create a 'show' column in both data frames where the value is always 'kitchen nightmares' for rows in KN data or 'hotel hell' for rows in HH data.
6. Compare column names to make sure everything is the same across both data frames.
7. Vertical merge using rbind()
8. Check the head() and tail() of the combined data frame to make sure merge worked as intended.
9. Save combined data frame to an RDS file.
