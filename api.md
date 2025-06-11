# API/Function Reference

## `number_one_album`

Usage: **`number_one_album(start_year, end_year)`**  
Filters the top ranked album for every year in the range

Parameters:  

* **`start_year`**: a number (`int`) representing the start year of the range (inclusive).  
* **`end_year`**: a number (`int`) representing the end year of the range (inclusive).

Returns:

A filtered data frame containing only the highest ranked album for each year in the range, sorted in ascending order.

## `albums_by_bands`

Usage: **`albums_by_bands(band_name)`**  
Returns all ranked albums by the specified band. Filters entire dataset and returns a filtered data frame of albums only by `band_name`.

Parameter:

* **`band_name`**: a string (`char`) representing the band\_name to filter on.

Returns:

A filtered data frame containing only the albums for which the artist column matches \<band\_name\>.

## `band_album_count`

Usage: **`band_album_count(band_name)`**  
Returns the number of ranked albums by the band.

Parameter:

* **`band_name`**: a string (`char)` representing the name of a band.

Returns:  
An integer (`int`) representing the number of albums in the data frame for which the artist column matches \<band\_name\>.
## `band_mean_rating`

Usage: **`band_mean_rating(band_name)`**  
Calculates the average album ranking for a band.

Parameter:

* **`band_name`**: a string (`char`) representing the name of a band.

Returns:

A number (`numeric`) representing the average album ranking for albums whose artist column matches \<band\_name\>.

## `year_albums`

Usage: **`year_albums(year)`**  
Returns the top rated albums from a year, sorted by ranking

Parameter:

* : a number (`int`) representing a year.

Returns:

A data frame of all albums whose year column matches \<year\> sorted in descending order.

## `missing_vinyl`

Usage: **`missing_vinyl()`**  
Finds all albums ranked 9/10 or better that the user does not currently own on vinyl.

Parameter:

* None

Returns:

A data frame containing all albums whose rank column is \>= 9 and vinyl column is empty.

## `year_most_vinyl`

Usage: **`year_most_vinyl()`**  
Returns what year the user has the most vinyl from.

Parameter:

* None

Returns:

A number (`int`) representing the year which is included in the most rows whose vinyl column contains “v”. 

## `band_album_comparison_chart`

Usage: **`band_album_comparison_chart(band1, band2)`**  
Generates a graph of ranking vs. year of all the albums for band1 and band2

Parameters:

* `band1`: a string (`char`) representing a band.  
* `band2`: a string (`char`) representing a band.

Returns:

A ggplot line chart with two entries that has Year on the x-axis and Rating on the y-axis, with each datapoint in a band’s line being an album in the data frame by the band.
