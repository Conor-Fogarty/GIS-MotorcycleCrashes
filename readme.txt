Motorcycle crash data were sent by Jenn Gazzillo, MassDOT Coordinator, gazzillo@ecs.umass.edu
metadata written by Bethany Bradley 2/21/19

X,Y coordinates are labeled 'X' and 'Y'.  These data are in the Mass State Plane projection (NAD_1983_StatePlane_Massachusetts_Mainland_FIPS_2001)

Open the CSV file in Excel to see the original column heading names (you can also rename them in Excel or delete columns you don't want)
ArcMap will cut off column headings


Some ideas for analysis:
- People complain about reckless motorcycle driving on highways, but are highway accidents more common than
local roads?  Use the attributes of road type to find out and make a map of accidents across the state.

- What is the cause of motorcycle accidents, and does that vary spatially across the state?

- See if there are spatial patterns associated with any of the attributes that interest you in the CSV file.


Some things to consider:
It probably makes sense to conduct the analysis at the town level.  Towns in this layer might not join neatly
with towns from MassGIS, so I'd recommend first using a spatial join to extract Town info from a Towns polygon
you download from MassGIS.  Then, summarize the data based on town and whatever attribute(s) you're interested 
in (e.g., summarize by town, and sum the number of fatal accidents).  After that, you can join the summary
table back to Towns to visualize it.

You should normalize (divide) any crash data by town population...larger towns will have more motorcycles and therefore
more accidents. The towns data that you download from MassGIS likely has population from the 2010 census.

You can download roads for visualization purposes from MassGIS.