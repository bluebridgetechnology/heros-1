# heros 

### Heros is a mobile-friendly web application that works by showing Incident Commanders the floorplan to a building prior to their team arriving to the scene of an emergency. 

Our web application development process, under the direction of Architecting I/O's scrum master (@ladyluxx on GitHub) conforms to the Scaled Agile Framework® (SAFe®), which is a set of organization and workflow patterns for implementing agile practices at enterprise scale. Our prioritization model of Weighted Shortest Job First (WSJF) enabled us to implement the MVP in order to convince stakeholders our application development project was worth investing in so that the employees and independent contractors working for Rescunomics LLC could scale the application from mere proof-of-concept to county to statewide to nationwide and beyond. 

Oluwaseun "Seun" Kolawole (bluebridgetechnology@outlook.com or seun@bluebridgetechnology.com), a Nigerian developer, was originally part of the cybersecurity team as an IT Admin to Rescunomics LLC, but since he is not an American citizen nor does he have a visa nor any loyalty to protect confidential U.S. intel, we informed him he was not eligible to work as an IT Admin on any backend portion of this project because sensitive, confidential, and classified government building blueprints to muncipal structures are involved. He had no business using a former HFD firefighter's login credentials to browse Harris County building blueprints, a serious abuse of power and priviledge that was entrusted to Emmanual Joel before he was suspended from the Houston Fire Department. Oluwaseun Kolawole retaliated by denying anyone access to managing the Admin Panel, preventing the rest of the hired dev team from analyzing the userbase. Later, Oluwaseun Kolawole admitted he's worked on this project for the past few years for Emmanuel Joel, has never been paid nor compensated for any of his time/work/labor, and never signed any written contractual agreement for his countless hours worth of development services rendered to the Rescunomics LLC CEO Emmanuel Joel. 

An entirely seperate version of the MVP for this app is currently being built-out from scratch as specified in the SOW between SVS (Softeq Venture Studios) and Rescunomics LLC per the 2022 Softeq accelerator program cohort's SEAD (Solutions Engineering Application Development) team. 

Architecting I/O used the Notion scaled agile development framework as opposed to Atlassian Jira for this development. Building floorplans were converted from PDFs to CAD .dwgs and compressed by eliminating unnecessary labels and graphics. The blueprints were then saved according to the following naming conventions, which spell addresses backwards, taking query speed into account: 
SS#####CityStreetName_BuildingName_floor##
The first two characters are the code name abbreviation for state and numbers 2 thru 7 in the title's string indicate the 5-digit U.S. zip code.

Using Autodesk AutoCAD and ESRI ArcMap Pro GIS software solutions, Architecting I/O was able to upload the 1:1 scaled vector CAD .dwg plans into the ArcGIS program to georeference the files and preserve their accurate/actual dimensions. The extension pack / extended suite of tools was utilized to project the blueprints atop a basemap in a method that ensured the preservation of metadata (proprietary trade secrets detailed in >75-pages of tutorials in Rescunomics' Notion account. Only through the meticulous reformatting process within ArcGIS could a future-proof file be exported as a lightweight GeoJSON (.geojson file). In the future, WebGL will be employed as a Google Maps Dev tool in order to showcase multiple stories of a building simultaneously as envisioned by the Project Manger (2D floorplans displayed flat and stacked in a 3-dimensional isometric Point-of-View with space between each level according to the multistory building's ceiling height). 

For demonstration purposes, the beginning middle and end files to the main floor of The Ion building are included in this repository:
TX22002MainStreet4201_TheIon.pdf
TX77002MainStreet4201_TheIon_1.dwg
TX77002MainStreet4201_TheIon_1.geojson

theIon.geojson file uploaded Monday, September 26th is not projected, whereas
theIon.geojson file uploaded Thursday, September 22nd, 2022 is projected -- on the WGS 1984 Coordinate System.
Use the most recent theIon.geojson for stairwell Alt testing for FRST Challenge trials so that the beacon displays accurately in the isometric perspective.

### INDOOR GEOLOCATION TRACKING FEATURE: To access the indoor geolocation tracking feature independently of the UI/UX, go to: https://rescunomics.github.io/heros with a Google Pixel6a Android using the Chrome browser from your smartphone.

The indoor geolocation tracking feature was compiled by Architecting I/O's Ryan Leach (@leachandryan on GitHub) to display a smartphone user's Lat Lng Alt (x, y, z) location in the bottom left hand corner of the screen. The z-values are in meters and are not a reflection of elevation nor height above terrain, but show a change in value between floors as you move up/down the storys of a building. For instance: 
-Going from floor 1 to floor 2 in a building whose ceilings are 7m (or 21' tall), will show a change in Alt values of +7m. Our z-values are accurate to within <1m. 
-Going from floor 2 to floor 1 in a building whose ceilings are 3m (or 9' tall), will show a change in Alt values of -3m. Our z-values are accurate to within <1m. 

We had originally planned to employ the NextNav API in conjunction with Google Maps dev tools, but we realized that we could just build out our own using the Google Pixel6a's IMU that has a built-in barometer, gyroscope, accelerometer, and magnetometer. 

For Google Pixel6a Android smartphone users on Incident Commander teams, Geolocation must be enabled on both devices and "Share my location" must be configured in order to display the user's x, y, z position to the Incident Commander's account from his laptop. This software is compatible with the 2010 and 2022 Windows 10 operating systems on a Panasonic Toughbook laptop computer; Windows 11 not yet tested. For demonstration purposes, search for "The Ion" building or "Hyde Park Condos", or either of those addresses to demo each building's associated GeoJSON (.geojson file) atop the map's baselayer, and toggle on/off the 45-degree isometric view of any given property. 

Google Maps Developers tools were used to arrive at this live geolocation tracking solution, which tested accurately to within 1m using the Chrome app on a Google Pixel6a smartphone running the latest version of the Android operating system. Accessing the same link using the Chrome app on an Apple iPhone 12 (iOS operating system) resulted in less accurate x, y, z locations and did not display any GeoJSON files, which is why the Google Pixel6a Android smartphone was selected for testing purposes, solely for its superior IMU performance. The Google Pixel6a Android smartphone was used to test the accuracy of this live-tracking feature to within 1m and 1s in various scenarios at the 2 locations where the GeoJSON files are displayted on the map. We've included the video files and screenshots as proof that our solution conforms to this degree of accuracy in a test-run where we walked in a triangle 3x and logged the data every 1s. The results can be viewed here: https://docs.google.com/spreadsheets/d/15rotqoqODwrfliVLoksETpXr4EpQvfAq9ab0VA_N1aE/edit?usp=sharing 

(c) September 22, 2022 RESCUNOMICS LLC. All Rights Reserved. USPTO Patent #
Do not share or distribute without permission. 
Source code property of Rescunomics LLC.
Contact CEO: emmanuel@rescunomics.com

>The files in this directory were compiled by Architecting I/O LLC for Rescunomics LLC.
>OUTSTANDING BALANCE: $37,890 OWED TO ARCHITECTING I/O LLC BY RESCUNOMICS LLC AND
>$25,000 OWED TO NIGERIAN WEB DEVELOPER OLUWASEUN KOLAWOLE. WARNING TO PAID DEVELOPERS! 
>DO NOT BECOME A VICTIM! DO NOT TRUST THE CEO OF RESCUNOMICS LLC EMMANUEL JOEL, HE IS A LIAR!
>Civil and criminal proceedings to follow. FOR MORE INFORMATION, CONTACT THE FORMER CTO OF RESCUNOMICS LLC: ezra@architectingio.com
