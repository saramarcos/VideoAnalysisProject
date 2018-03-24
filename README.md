# VideoAnalysisProject
Code to merge and explore data for Video Analysis

Video Analysis - data manipulation in Python
Datasets:
1). GA Data. Variables:
ga:pageTitle (Title)
ga:eventAction (variable that needs to go into columns: 25%, 50%, 75%)
Ga:dimension27 (Tag)
ga:totalEvents (number that should go into ga:eventAction)
2). Looker Data
MCP Videos Title (Title)
MCP Videos File Duration (Minutes)
MCP Videos Released Time (date and time)
MCP Videos Metrics - Daily By Position and Play Type Video Content Start (Content_Start)
MCP Videos Metrics - Daily By Position and Play Type Video Content 100% (Content_100%)
MCP Videos Metrics - Daily By Position and Play Type Video Load (Video_load)
Completion Rate (Completion_rate%)
Data Preparation
1. Dataset “GA”: transpose variable event-action into 3 columns (25%, 50% and 75%) with
the variable title into indexes and the value of the events into the column.
1.1. Change variable name “ga:dimension45” into “Title”
1.2. Change variable name “ga:dimension27” into “Tag”
2. Dataset “Looker”:
2.1. Change variable name “MCP Videos Title” into “Title”
2.2. Change variable “MCP Videos File Duration” into “Minutes”
2.3. Change variable “MCP Videos Released Time” into “Date_Time”
2.3.1. Extract day of the week, month, date, hour (into columns)
2.4. Change vble “MCP Videos Metrics - Daily By Position and Play Type Video Content
Start” into “Content_Start”
2.5. Change vble name “MCP Videos Metrics - Daily By Position and Play Type Video
Content 100%” into “100%”
2.6. Change vble name “MCP Videos Metrics - Daily By Position and Play Type Video
Load” into “Video_load”
2.7. Change vble name “MCP Videos Metrics - Daily By Position and Play Type Video
Load” into “Video_load”
3. Join both GA and Looker datasets matching by title.
4. Clean duplicates.
Variables aggregation (in columns):
5. Minutes video watched​ (calculating by the length of the file and the percentage
watched - 25, 50, 75)
6. Completion ratio​ (calculating with completion 100% and start video variables)
7. Video content start ratio​ (calculating with video start and total number of videos)
8. Video content load ratio​ (calculating with video load and total number of videos)
9. Get 25% view ratio​ (calculating 25% and total videos), same for 50 and 75%.
Data Analysis
10. Do some plot analysis (scatter plot, box plot) to see relations, outliers. How is the data.
11. Get a summary table of the total amount of 25% viewed videos and its percentage, for
50%, 75, video load, video start and video completed.
a. Per month
b. Per day of the week
c. Per hour of the day
d. Per tag
12. Get top 5 most watched -longer (in minutes - after calculating which videos were
watched for longer)
a. Per month
b. Per day of the week
c. Per hour of the day
d. Per tag
13. Correlation Matrix
