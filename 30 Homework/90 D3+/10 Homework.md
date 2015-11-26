# D3+

Fot this week's homework you will create a dashboard in D3 consisting of at least two interactive visualisations.
You can find many examples of dashboards online, here is one that comes close to what you will be designing in this assignment:
https://public.tableau.com/s/gallery/asylum-seekers-europe. This is merely an example, be critical in your own design!

## Step 1
The idea is to find a data set that has data (more then one variable) for each country (or most countries) in the world and use that data to make a map and another interactive graph. Data you could use are again the number of inhabitants, the GDP, or the population density. If necessary write a python script to scrape/process the data and create a JSON or CSV file.
Whether you use JSON or CSV is up to you, as long as you load them from a separate file using the proper 
D3 functions.

## Step 2
You dashboard must consist of an interactive map and another interactive visualisation. As long as it makes sense, you can reuse your map and line graph from last week.
Your map should encode one variable, for example in color.
Your second interactive graph should represent another variable from the dataset and should be interactive as well (eg. add tooltip to bar-chart/scatterplot or crosshair to line graph).
If you would like to make another visualisation instead of a map, discuss it with the instructors first.

## Step 3
The two interactive visualisations should be connected with each other. That means that interaction on the map should cause an update of you second visualisation (or other way around). You can, for example, select a country on the map and update your line graph accordingly (so that it shows data for the selected country).

## Step 4
Add another interactive element to your visualisation. You can either add a third visualisation, an interactive table, or another html element, that adds interactivity to the dashboard (ex. dropdown menu to change a variable).  


## Step 5
Write a short description of your data and the story that you want to tell with it. Describe the design process, and for each step all your design choices.


## Check before submitting: 
* Each of your visualisations should have all the necessary ingredients (title, axes, names, etc.).
* Design of your visualisations is important, also the overall design of your dashboard and webpage will be graded.
* Think about all the design principles that were mentioned during the course and whether your dashboard is designed according to those.
* Pay attention to the storytelling aspect of your dashboard.
  

## Submit instructions

1. Create folder D3+ in your master branch and push all the files that you have created.
2. Push any libraries used, including d3 if linked to a local copy.
3. Push the PDF in which you describe the design process and justify your design choices.
