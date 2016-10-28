# D3 Linked Views

For this week's homework you will create a linked views visualization in D3 consisting of at least two interactive visualizations.
You can find many examples of linked views online, here is one that comes close to what you will be designing in this assignment [Asylum Seekers Europe]. This is merely an example, be critical in your own design!
 
[Asylum Seekers Europe]: https://public.tableau.com/s/gallery/asylum-seekers-europe

## Step 1
The idea is to find a data set that has data (more then one variable) for each country (or most countries) in the world and use that data to make a map and another interactive graph. Data you could use are again the number of inhabitants, the GDP, or the population density. If necessary write a python script to scrape/process the data and create a JSON or CSV.
Whether you use JSON or CSV is up to you, as long as you load them from a separate file using the proper 
D3 functions.

If you are running out of time finding your own data, please have a look here: [Happy Planet Index], [Better Life Index], [Quality of Life].

[Happy Planet Index]: http://happyplanetindex.org/
[Better Life Index]: http://stats.oecd.org/Index.aspx?DataSetCode=BLI
[Quality of Life]: http://www.numbeo.com/quality-of-life/rankings_by_country.jsp

## Step 2
Your dashboard must consist of an interactive map and another interactive visualization. You can reuse your map from the previous assignment but the second visualizations should be something new, that you have not implemented yet (if you choose for a barchart, it should be either stacked or grouped barchart; line plot is not permitted).

Your map should encode one variable, for example in color.
Your second interactive graph should represent another variable from the dataset and should be interactive as well (eg. add tooltip to scatterplot).
If you would like to make another visualization instead of a map, discuss it with the instructors first.

## Step 3
The two interactive visualizations should be connected with each other. That means that interaction on the map should cause an update of your second visualization (or other way around). You can, for example, select a country on the map and update your e.g. scatterplot accordingly (so that it shows data for the selected country).

## Step 4
Add another interactive element to your visualization. You can either add a third visualization, an interactive table, or another html element, that adds interactivity to the dashboard (ex. dropdown menu to change a variable).  


## Step 5
Write a short description of your data and the story that you want to tell with it. Describe the design process, and for each step all your design choices.


## Check before submitting: 
* Each of your visualizations should have all the necessary ingredients (title, axes, names, etc.).
* Design of your visualizations is important, also the overall design of your webpage will be graded.
* Think about all the design principles that were mentioned during the course and whether your visualizations are designed according to those.
* Pay attention to the storytelling aspect of your visualizations.
  

## Submit instructions

1. Create folder D3LinkedViews in your master branch and push all the files that you have created.
2. Push any libraries used, including d3 if linked to a local copy.
3. Push the PDF in which you describe the design process and justify your design choices.
