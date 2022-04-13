# Audubon in Action: Creative Approaches to Data 

## Intro 

In this session, come test emerging technologies and digital methods to enhance the impact of the Penn's collections. Experiment with the latest project, Birds of Philadelphia, which uses high-resolution images of Audubon's plates from The Birds of America alongside crowdsourced observation data to consider the depiction of wildlife data through visual, aural, and interactive components. Participants will find creative ways to amplify, build on, and disseminate data from environmental collections and crowdsourced projects. Read more about this project [here](). 

This workshop was hosted as part of [Earth Week Data Jam](https://www.library.upenn.edu/about/exhibits-events/earth-week-data-jam), a week of working and playing with enviornmental data with the Center for Research Data and Digital Scholarship (RDDS) at Penn Libraries.  

## Process
Plate images from Audubon's *Birds of America* were downloaded from Nathan Buchar's GitHub repository, compiled from the [Audubon Foundation](https://www.audubon.org/birds-of-america). Observation data was exported from the [Birds of Philadelphia](https://www.inaturalist.org/projects/birds-of-philadelphia) project on iNaturalist, filtered for only those observations posted with a license. 

For any observation data with an associated image or sound, these files were exported and saved to a folder named for the corresponding common bird name. Additional sound files were downloaded via the [xeno-canto](https://xeno-canto.org/explore/api) API, querying based on the common bird names. Birds were then matched, by common name, to the corresponding plate images - only those that were matched were included in the project. 

Photomosaics were created using a script by [Data Dolittle](https://datadolittle.com/).Display posts were created using Pillow (Python Imaging Library), including the common name, scientific name, and information about the number of observations and last observation recorded on iNaturalist. 

The sonification of the observation data was created using Pydub, where 1 second is the equivalent of 1 day of observations. For any day when birds were observed, a random sound file for the corresponding bird was appended to the file. (Datasets for individual bird sounds that were downloaded for this project are labeled with the common name of the bird and available in the *sounds* folder.) Individual citations for each sound file can be generated from those datasets.) Silence means no birds were observed on that day.

# Credits

Created by [Emily Esten](https://www.library.upenn.edu/people/staff/emily-esten). 

The Center for Research Data and Digital Scholarship facilitates data-driven and data-literate research and scholarship across the disciplines in order to foster informed and ethical data communities at Penn. Interested in data, computational research, digital humanities, or open and public scholarship? Find us on the [Penn Libraries website](https://www.library.upenn.edu/help-with/research-data-digital-scholarship). 


## Citations

Nathan Buchar, Audubon Bird Plates, (2022), GitHub repository, https://github.com/nathanbuchar/audubon-bird-plates. Images of Audubon plates available courtesy of the John James Audubon Center at Mill Grove, Montgomery County Audubon Collection, and Zebra Publishing.

Data DoLittle, Photo Mosaic using Python, (2021), GitHub repository, https://github.com/Datadolittle/Photo_Mosaic. Released via [an MIT License](https://github.com/Datadolittle/Photo_Mosaic/blob/master/LICENSE). 

iNaturalist contributors, iNaturalist (2022). Birds of Philadelphia. iNaturalist.org. Occurrence dataset http://www.inaturalist.org/observations/export?has%5B%5D=photos&quality_grade=research&identifications=any&verifiable=true&projects%5B%5D=birds-of-philadelphia accessed via iNaturalist.org on 2022-04-18.

Vellinga W (2022). Xeno-canto - Bird sounds from around the world. Xeno-canto Foundation for Nature Sounds. Occurrence dataset https://doi.org/10.15468/qv0ksn accessed via GBIF.org on 2022-04-04. (Datasets for individual bird sounds that were downloaded for this project are labeled with the common name of the bird and available in the *sounds* folder.)