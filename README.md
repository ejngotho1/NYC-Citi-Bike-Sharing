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

#### Read csv and convert to dataframe

citibike_data = "201908-citibike-tripdata.csv"
citibike_df = pd.read_csv(citibike_data)
citibike_df.head()

#### Change datatypes
citibike_df['tripduration1'] = citibike_df['tripduration']
citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='m')
citibike_df.head()

#   Column                   Dtype         
---  ------                   -----         
 0   tripduration             datetime64[ns]
 












