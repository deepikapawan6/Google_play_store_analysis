# Google_play_store_analysis
Analysis of the google play store apps.
# Data_Set
The data contains two CSV files, the first CSV has 13 columns and more than 10,000 rows and the other CSV has 5 columns and about 64,000 rows.
# Why I choose this Data 
The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market.
# Cleaning
1. The first part of cleaning is extracting the columns that are important for the analysis. The columns that I'm interested in are: App, Category, Type, Ratings, Reviews, Instals, Size and Content rating.
2. Next I did is converting the data type into numeric, filling the null values and replacing the unwanted objects.
    a). Reviews - converting the data type into numeric by manually determining the position of a string and removing it.
    b). Type - filling the nan value with "free".
    c). Content rating - did the value count.
    d). Size -  replacing "K" by ".5M" and then removing "M" and then did the value count.
    e). Installs - removing "+" and "," and then did the value count.
    f). Rating - did the value count.
# Analysis
For analysis I define a function named "Analysis" that takes in the column name as an input, illustrating the Absolute Frequency and did the plotting using barplot.
1. Type : "Free" apps are more predominant than the "Paid" apps.The difference is too much, it means the customers want free apps rather than paid apps, developers should keep this in mind while designing an app.
2. Content Rating : Developers tends to develop apps for "Everyone". This is because the overall population has variations in interests and needs.
3. Installs : So, what we have here are ups and downs. For all apps, I think that is because users often don't update their mobile versions so when a new version or update of the app releases, when they open their app again ,crashes occurs. This leades to uninstalling application.
4. Rating : Due to probability of violation in rating apps, It appears as if you try to improve the image of an application to get more reviews or more downloads.
# Loading the new dataset into a database
After doing the analysis, I loaded the dataset into PostgreSQL, and create a new database named "ETL_Project_DB". For this, first we have to establish a connection to the server and then create an engine to connect to the server. Once we have our table into the postres, we can do the queries in the postgres.
