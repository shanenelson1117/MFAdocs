# Structure of My Favorite Albums

For experienced programmers, it is necessary to understand the underlying architecture of My Favorite Albums in order to make changes. **app.R** is the top level R file which calls the server and UI (backend and frontend) logic. **app\_ui.R,** built on Shiny UI, controls the frontend of the shiny app and **app\_server.R** controls the backend by calling all necessary functions. **data/album-rankings.csv** is the entire dataset for the project, however, this file can be amended and external data can be used if needed. User input is handled reactively by the Shiny UI framework, which drives changes to the site. Helper functions are in their own R files and work with **album-rankings.csv** directly. These helper functions are:

* **number\_one\_album(start\_year, end\_year)**  
  Filters the top ranked album for every year in the range  
* **albums\_by\_bands(band\_name)**  
  Returns all ranked albums by the specified band  
* **band\_album\_count(band\_name)**  
  Returns the number of ranked albums by the band  
* **band\_mean\_rating(band\_name)**  
  Calculates the average album ranking for a band  
* **year\_albums(year)**  
  Returns the top rated albums from a year, sorted by ranking  
* **missing\_vinyl()**  
  Finds all albums ranked 9/10 or better that the user does not currently own on vinyl  
* **year\_most\_vinyl()**  
  Returns what year the user has the most vinyl from  
* **band\_album\_comparison\_chart(band1, band2)**  
  Generates a graph of ranking vs. year of all the albums for band1 and band2

More functions of this manner to interface with an increased data set can be implemented.

# Key Dependencies 

Developers must have the following software and packages installed to run My Favorite Albums,

* **shiny** (package)  
* **dyplr** (package)  
* **ggplot2** (package)  
* [**R**](https://cran.r-project.org)  
* [**RStudio**](https://posit.co/download/rstudio-desktop)

Both packages can be easily downloaded by running **install.packages(c("shiny", "dplyr"))** in an R-Studio terminal. Users must also download the My Favorite Albums codebase from [https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/](https://github.com/UW-Example-Student/MyFavoriteAlbums/blob/main/README.md). 