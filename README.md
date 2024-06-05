
# Kickstarter Data Importer

The Kickstarter Data Importer, a crucial component of our project, is responsible for importing monthly scraped data from Kickstarter, which is readily available from Webrobots [here](https://webrobots.io/kickstarter-datasets/). I have personally utilized this method for my job market paper, underscoring its significance in our collective work.

The general steps for the code are:
1. Import the first available data for each year into a PySpark session, performing data validity checks.
2. Examine additional data for schema changes.
3. Merge the data with the respective year if there are no schema changes.

The code requires downloading data to a physical drive and organizing it into year-level folders. However, future iterations aim to use a more efficient method using urllib requests, significantly reducing physical drive space.

Data concerns include:
1. Inconsistent JSON formats (uneven UTF-8 encoding)
2. New columns were added by the scraper in December 2015, requiring changes in data import.
3. Earlier data scraped in groups requiring the "explode" command in Python for project-level arrangement.