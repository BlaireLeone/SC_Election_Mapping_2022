# SC_Election_Mapping_2022

<img src="https://cms.lookout.co/_preview?_cms.db.previewId=00000185-07fd-da20-afed-1ffdc0d80000&_date=" style= "height=60; width=60" >  

This is a repo with 2022 midterm election maps from Santa Cruz County created for Lookout Santa Cruz, a digital newsroom covering Santa Cruz County, California. Maps can be found [here](https://lookout.co/santacruz/election-2022/story/2022-12-09/santa-cruz-how-did-your-neighborhood-vote-in-these-three-2022-races) and [here](https://lookout.co/santacruz/election-2022/story/2022-11-28/voter-turnout-fell-by-10-points-in-santa-cruz-county-and-more-in-surrounding-counties). The election results data were provided by the [Santa Cruz County Elections Department](https://www.votescount.us/). Throughout the mapping process, I communicated with the Clerk's office to resolve discrepancies apparent after analysis, such as understanding the difference between registration and voting precincts and clarifying same day registration vote counts. These were the steps I followed:

1.) Ingested data

 - The County Elections Department released election results daily from November 8 until December 6 when races were finalized. Daily results were released via PDFs which initially required using ABBYY Fine Reader's Optical Character Resolution functionality to ingest the data before reformatting and aggregating vote percentages and differentials within voting precincts in Excel. 

2.) Generated geospatial precinct boundaries

 - The precinct maps I created using the election precinct map from the county's [GIS website](https://gis.santacruzcounty.us/), joined in QGIS with special elecion precincts, called voting precincts, created specifically for every election. After dissolving the registration precincts into their consolidated voting precincts, I joined the election results data to the new maps and exported them. The voting precinct table I created by ingesting PDFs created by the county Elections Department, again using ABBYY Fine Reader's Optical Character Resolution functionality.  

3.) Created final election maps

- I made the first iteration of the maps in Datawrapper, however as Lookout's needs changed, I turned to MapBox for the program's greater flexibility and customizability. Once the maps were uploaded and stylized in MapBox using colors that fit with Lookout's theme, I rendered a legend and hoverability using MapBox GL JS.

- Since MapBox doesn't allow interactivity through iframes, I made additional adjustments via HTML, JavaScript, and CSS to fit into Lookout's CMS, called Graphene. In Graphene, I created a blank html page to host the maps and added the weblink for that page into the iframe provided by MapBox, so viewers could enjoy interactivity with the maps, and the maps could adjust whether on a phone or computer. 
