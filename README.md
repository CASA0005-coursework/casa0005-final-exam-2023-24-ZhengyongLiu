# Instructions

## Submission

On clicking the exam link a new repository has been created for you in the exam classroom. You should now clone this repository into a new RStudio project then **commit and push** to GitHub as usual. 

GitHub takes a snapshot of your **local git** repository at the deadline so **commit and push often**, as you should do in all spatial data science projects. The deadline is based on your last commit, but we expect the repository to be pushed to GitHub very soon after. 

## Before you begin: 

* Go to the top of the `exam_response.Rmd` RMarkdown document and edit the name and student number fields (at the top of the `.Rmd`).

* Complete the originality declaration

## Task

You have six hours to complete this open book exam. You must select and undertake **only one** of the research questions below. Links to the data for each question have been provided and you are free to source additional data for extension analysis, but everything you need is provided.

* You must write your response in the `exam_response.Rmd`, under the originality declaration.

* You may use any resource to assist you but the work must be your own and you are required to sign a originality statement within the exam. 

* Questions about the exam must be asked on the open Slack GIS channel. 

* You can use RStudio visual markdown editor if you wish.

* If you copy a section of code from an online source please provide a relevant link or acknowledgment.

Marks are awarded as per the marking scheme. It's important to note there is no 'right' answer, even if your findings are inconclusive or not as expected, you are awarded marks for how you approach the problem.  

## Within your work you must:

* Provide an initial project scope in bullet point form. Your project scope should include:

    * If you intend to propose a variation of the original question (e.g. selecting a specific year of data to analyse), this must be based on appropriate reasoning and clearly stated.
  * A brief evaluation of your main research dataset(s) as well as an assessment of any data processing tasks that will be required or additional data that might be required to complete your analysis.
  * A brief explanation of the data wangling and analysis you intend to undertake, prior to starting the analysis. This may include research questions or hypotheses you identify as relevant. 
  * You may also wish to identify any constraints (around the data you have been instructed to analyse) or obvious omissions from the set task that could limit what will be produced in this short project. These could relate to spatial or temporal limitations in the dataset, what you decide is reasonable to analyse or anything else that is relevant. 

* Produce a well commented and fully explained RMarkdown document that attempts to answer the research question.

* Create at least one graphical output and at least one mapped output.

* Critically reflect on the results you have produced. 

## Tips:

* In the time you have, prioritise good solid analysis over innovative analysis that uses advanced techniques.

* Structure your RMarkdown document with titles and subtitles. 

* Comment and explain your working throughout.

* State assumptions and describe limitations.

* In most questions some administrative boundary data has been provided, use this to assist guiding recommendations and outputs.

* Provide critical commentary about the data you are using and the analysis you are undertaking throughout.

* Plan your time. We suggest 1 hour for data exploration, 2-3 hours for analysis, 1 hour for visualisations, 1 hour for interpretation and reflection. 

# Final exam questions

## E-scooter casualties 

The London Mayor is reviewing the use of e-scooters within the City and wants to understand where e-scooter accidents happen. You have been enlisted as a consultant and tasked to conduct an analysis of their data.

You should use appropriate data processing and analysis methods to produce an overview report which summarises the patterns revealed in the data. It is expected that at least some of the methods you use will relate to the spatial dimensions of the data.

Your report should include a brief introduction including relevant contextual information at the beginning and a critical review of your findings at the end. You must include at least one map. 

### Data

All the road accident data can be downloaded from: https://www.data.gov.uk/dataset/cb7ae6f0-4be6-4935-9277-47e5ce24a11f/road-safety-data You will need to click show more. The following datasets (from the above website) may be useful:

* 2020-2022 E Scooter accident data
* Road collision data per year (containing latitude and longitude) that can be joined to other data. 
* Road casualty data containing a row for each casualty in a collision (e.g. if a collision has two casualties there will be two rows, one for each person, with the same accident index).
* Road Safety Open Dataset Data Guide -2022, at the very bottom of the webpage
* London LSOA boundaries: https://data.london.gov.uk/dataset/statistical-gis-boundary-files-london 

You may wish to use open street map data, although it is not necessary to answer the question. 

* London shapefile (big data!): https://download.geofabrik.de/europe/united-kingdom/england/greater-london.html 

## Stanford Open Policing Racial Disparities

The Stanford Open Policing Project collected police data on traffic stops to identify racial bias in policing. Some of the data is located using latitude and longitude, but wasn't effectively used within the study.

You have been enlisted by the City of Columbus as a consultant and tasked to conduct an analysis to explore if there is any evidence of racial bias in police stops and how this may play out spatially in the city. You may wish to focus on particular aspects of the data such as the ‘hit rate’ which is defined as the proportion of successful stops.

You should use appropriate data processing and analysis methods to produce an overview report which summarises the patterns revealed in the data in this year. It is expected that at least some of the methods you use will relate to the spatial dimensions of the data.

Your report should include a brief introduction including relevant contextual information at the beginning and a critical review of your findings at the end. You must include at least one map.

### Data

I recommend using the state name (Ohio) to search for a relevant local projected coordinate reference system to do your analysis in.

* Police Precincts boundary shapefile https://opendata.columbus.gov/datasets/6ba31931272b481887655231c361f1ee/explore?location=39.986565%2C-83.018021%2C11.68 
* Columbus traffic stop data: https://openpolicing.stanford.edu/data/  

Depending on the question you have proposed you may wish to use census data:

* Census data (for Ohio) can be accessed in the same manner as the practice question on graffiti mitigation. Searching for race and ethnicity, income, poverty status will bring up relevant data: https://data.census.gov/cedsci/advanced
* Census tracts, search for Ohio: https://www.census.gov/cgi-bin/geo/shapefiles/index.php 
* Alternatively you may want to use the tidycensus package as shown in week 9.
* The corporate boundary of Columbus, meaning the area maintained by the City, although it is the same as the Police Precincts boundary: https://opendata.columbus.gov/datasets/corporate-boundary/explore 

## School grades in South Africa 

The South African Government wants to explore factors that influence students passing matriculation (also known as grade 12 or matric). This qualification is required to enter university. They have appointed you as a consultant to investigate this question.

You should use appropriate data processing and analysis methods to produce an overview report which summarises the patterns revealed in the data. It is expected that at least some of the methods you use will relate to the spatial dimensions of the data.

Your report should include a brief introduction including relevant contextual information at the beginning and a critical review of your findings at the end. You must include at least one map.

### Data

#### Spatial data

* South African Municipal boundaries, select 2018 as 2016 is in a file geodatabase: https://dataportal-mdb-sa.opendata.arcgis.com/datasets/215cfd521e64452d8edeff1d83b89c76/about 

#### Education/ socioeconomic data

Follow the instructions carefully to extract the data. The first link below will take you to a page with the education level data at the municipality level. The spatial level of municipalities has been set in the left hand side of the page under “selected geographies”. In the top right of the webpage you can download the data. **Note** the file path names are long! Place it on your desktop to unzip it > rename the folder > place it in your R Project data folder.

* Highest education level for people 20 and older per municipality: https://wazimap.co.za/data/table/?table=HIGHESTEDUCATIONALLEVEL20&geo_ids=municipality|country-ZA&release=latest 

You will need extra data! Explore this link to get an idea of what data can be downloaded from this website https://wazimap.co.za/profiles/province-NW-north-west/ 

Going back to the first webpage (education data) change table under the table explorer. Search for another dataset (examples below) and make sure the geographies (under selected geographies) is still municipalities in South Africa.

* Examples of other data:
  * Annual household income
  * Electricity 
  * Employment 
  * Internet access