# How is the dataset formatted?

**Warning: The first line of album-rankings.csv MUST remain unedited or else My Favorite Albums will not function.**

The dataset \`album-rankings.csv\` is a comma-separated value file. Each line represents a row (one album). Within each row each column entry is separated by a comma. The rows are first sorted by year, with albums with the oldest year first, and then within albums from the same year sorted by ranking, with the highest ranked album first. Below is a list of the columns:

* **Year**: the year of the album.  
* **Ranking**: a number representing how the user ranks the album compared to other albums in the same year (1 being the highest).  
* **Album**: the album title.  
* **Artist**: the band/artist name.  
* **Rating**: a number from 1-10 representing the users how much the user enjoyed the album, 10 being the highest.  
* **Vinyl**: either v or empty. v signifies that the user owns the album.  
* **EP**: either EP or empty. EP signifies that the album is an EP.

After the EP column a comma is required. A sample of the dataset (lines 1-4) is seen below:

![First few lines of album-rankings.csv](images/csv.png)  
The first line tells R the title of each column. 