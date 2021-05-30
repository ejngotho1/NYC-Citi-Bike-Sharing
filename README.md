# NYC-Citi-Bike-Sharing

### Overview of Project

Now that we've gotten a good idea of how to create our story, there is still some more work to be done to convince investors that a bike-sharing program in Des Moines is a solid business proposal. To solidify the proposal, one of the key stakeholders would like to see a bike trip analysis.
For this analysis, you’ll use Pandas to change the "tripduration" column from an integer to a datetime datatype. Then, using the converted datatype, you’ll create a set of visualizations to:
Show the length of time that bikes are checked out for all riders and genders Show the number of bike trips for all riders and genders for each hour of each day of the week Show the number of bike trips for each type of user and gender for each day of the week. Finally, you’ll add these new visualizations to the two you created in this module for your final presentation and analysis to pitch to investors.
1.	Deliverable 1: Change Trip Duration to a Datetime Format
2.	Deliverable 2: Create Visualizations for the Trip Analysis
3.	Deliverable 3: Create a Story and Report for the Final Presentation
4.	Extra: A written report on Des Moines - Bike Sharing Project Analysis README.md.
Resources and Before Start Notes:
•	Data Source: NYC_CitiBike_Challenge_starter_code.ipynb, NYC_Citibike_Challenge.ipynb and 201908-citibike-tripdata.csv
•	Data Tools: Jupyter Notebook, CSV, Tableau and IO (Web Server)
•	Software: Jupyter Notebook.
Download Tableau Public
First, go to the Tableau website and enter your email. You will also be required to enter some contact information, but you can always unsubscribe from communications.
Install Tableau Public
Once you have downloaded Tableau Public, we can start the process of installing Tableau Public. The process of installing Tableau Public is very similar to installing most other programs.
After it's finished downloading, click to open the file and then follow the on-screen instructions. This is the first screen you will see as part of the installation. Go ahead and click "Continue."

### Having installed tableau its time to move to the challenge

Deliverable 1:
Change Trip Duration to a Datetime Format
Deliverable Requirements:
Using Python and Pandas functions, we will convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After converting the "tripduration" column to a datetime dataytpe, we’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2.

### Steps

#### Read csv and convert to dataframe, change data types and them export as new csv file

import pandas as pd

##### 1. Create a DataFrame for the 201908-citibike-tripdata data. 

citibike_data = "201908-citibike-tripdata.csv"

citibike_df = pd.read_csv(citibike_data)

##### 2. Check the datatypes of your columns. 

citibike_df.info()

##### 3. Convert the 'tripduration' column to datetime datatype.

citibike_df['tripdur_orig'] = citibike_df['tripduration']

citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='m')

citibike_df.head()

![Results](https://user-images.githubusercontent.com/57301554/120095281-be266680-c0ea-11eb-9b06-dd5d381d89e7.PNG)

##### 4. Check the datatypes of your columns. 

citibike_df.info()

![Results1](https://user-images.githubusercontent.com/57301554/120095284-c1215700-c0ea-11eb-9f7b-d3dcd064f17c.PNG)

# Deliverable 2:

#### Create Visualizations for the Trip Analysis
##### Deliverable Requirements:
###### Using Tableau, create visualizations that show:

How long bikes are checked out for all riders and genders.
How many trips are taken by the hour for each day of the week, for all riders and genders.
A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.
Create the Checkout Times for Users Viz

### Ccheckout times for users

#### Line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.

![Results2](https://user-images.githubusercontent.com/57301554/120095285-c41c4780-c0ea-11eb-85e9-d3cfb7827470.PNG)

### Trips by weekday

![Results3](https://user-images.githubusercontent.com/57301554/120095288-c7173800-c0ea-11eb-8acb-f1addee2a5b5.PNG)

### Checkout times by Gender

#### Line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.

![Checkout Times By Gender](https://user-images.githubusercontent.com/57301554/120095593-5cff9280-c0ec-11eb-8a5e-bf149493a73f.PNG)

### Trips by Gender Weekend by Hour

#### A heatmap showing the number of bike trips for each hour of each day of the week.

![Trips by Gender Weekend by hour](https://user-images.githubusercontent.com/57301554/120095598-64bf3700-c0ec-11eb-9301-9e195dc9c63f.PNG)

### Trip by Gender by Weekday
#### A heatmap showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.

![Trip by Gender by Weekday](https://user-images.githubusercontent.com/57301554/120095600-6ab51800-c0ec-11eb-8e4d-8f1590921bb0.PNG)






 












