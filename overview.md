I want to create a youtube tutorial about data cleansing. I want to create a csv file that contains examples of dirty data for us to clean. The sceneario is that a class of pupils has gone out to do some manual data collection and come back to add this to a spreadsheet. However, the data has lots of problems we need to fix - the car colour may include multiple entries for the same car, with different spellings or abbreviations (e.g. "red", "Red", "rEd", "redd", "rd"). We also need to fix issues with missing values, such as some pupils forgetting to record the car colour at all.

The time and date will also have inconsistencies, such as different formats (e.g. "2023-03-15", "15/03/2023", "March 15, 2023") or missing values. Or simply just 'monday', 'mon', or 'm'.

the number of occupants is also recorded, but that might be missing or recorded as text (e.g. "two", "3", "four", or mispelt completly).

the make and model of car are also recorded with similar issues.

some pupiles will also have recorded cyclists and motorbikes, as the make or model or car and we need to fix that too.

Generate 3 csv files with simliar issues, with 100 entries each as Comma separated value files.

Write pretend instructions for the pupils to follow, and purposefully make it vague so that we can come back to that later too to see why the issues occured.

The lets build some examples of how we can clean this data in python using pandas, and then how to plot the data with matplotlib. We'l do this in a jupyter lab notebook.

