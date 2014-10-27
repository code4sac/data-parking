data files about parking
============

These files were downloaded from gov websites then cleaned up to make them more user-friendly.

Here's some information about where they came from:

##about street-parking-sac.csv

* original file name: 80139-locations-of-public-parking-spaces.csv
* what it is: details about on-street parking spots in the City of Sacramento
* where it came from: http://data.cityofsacramento.org/datastreams/80139/locations-of-public-parking-spaces/
* last update by city: 9 Jan 2014
* date accessed by code4sac: 7 Feb 2014
* grain: each row in the file describes one parking spot

####Column descriptions
(coming soon)


##about parki_space_parki_space.sql

contributed by Jay Venti
8 Feb 2014
notes from Jay: 

In case it's too much of a bother to run the utilities I have a MySQL dump of the parking data.
It may not be perfect if you find anything funky about it let me know. Also you may need to add 
indexes for your specific purpose it's a freshly imported item.

##about parking_final.json

contributed by Andy Axton
4 Feb 2014




##more resources

Kaleb and Jay worked on some scripts to scrub up data from the Sac City portal... 
jrcsv2gncsv.py takes the street parking data file and converts it to a tidy .csv!
find the code here:
https://github.com/code4sac/city-data-portal-conversion

###about transforms_for_open_refine.json

contributed by hailey pate
26 Oct 2014

[OpenRefine](http://openrefine.org) is a free and awesome tool for cleaning up messy data. It's great for programmers and non-programmers alike. Once you've cleaned up a data file in OpenRefine, it's easy to export a list of the steps you took and then share those steps with others. No programming or command line use required. 

Hailey used OpenRefine to do a quick and dirty clean up of the parking data file. The recipe she used is outlined in [this json file](https://github.com/code4sac/data-parking/transforms_for_open_refine.json). If you've got [OpenRefine](http://openrefine.org) installed and you've downloaded the parking file from the City's data portal, take these steps to clean up that parking data in a jiffy:

1. Start the OpenRefine app on your computer. It might be labeled with its former name, GoogleRefine. This should open a new tab in your web browser and display the app's landing page. 

2. From the menu on the left, choose _Create Project_. 

3. Choose the parking data file you downloaded and click _Next_. 

4. This takes you to the parsing options. There shouldn't be a need to mess with anything here. Change the name of your project in the upper right corner if you like, i.e. "Sac Parking Data Cleanup". Then click _Create Project_.

5. This takes you to the main working page. In the left sidebar, you'll see two tab options: _Facet / Filter_ and _Undo / Redo_. Click on _Undo / Redo_, then click the _Apply..._ button. 

6. This opens a pop-up window titled "Apply Operation History". Copy the contents of `transforms_for_open_refine.json` and paste them into the box in this window. Click the button at the bottom to apply the transforms, then wait for the magic...

7. When it's done working, you'll see the first 10 lines of a much happier data table. Click the export button on the upper right to export the data in the file format of your choice. 

Bon apetite! 








