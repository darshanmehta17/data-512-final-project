# Analysis of Crime Incident Reports - Boston

> Authored by ***Darshan Mehta*** on ***Nov 14, 2019***.


## Motivation

Crime has become so common these days that people are starting to see it as a part of society. The entire collection of movies and TV shows under DC comics depict crime to be deeply rooted in the civilization. There are an endless number of movies and shows which are centered around crime. It has become so commonplace that some even go as far to claim it to be *"an integral part of a healthy society"* [1]. According to Durkheim [1], the amount of deviance in crime remains relatively stable over time. I find that statement a little suspectful. Just considering mass shootings in the United States, the crime rate went up by 24% since the last year. The average mass shooting in 2018 was 0.88 per day [2] and bumped up to 1.24 per day in 2019 [3]. While this doesn't negate Durkheim's hypothesis, but it is contradicting enough to spark some curiosity. 

For this analysis, a major reason behind picking Boston for the analysis was that I was looking to move to the East Coast for work after graduating. And as part of my basic search, understanding the crime statistics of the cities was an imporant factor. There have been some analysis done in the past such as that in [5], [6], and [7] which bring to light some interesting facts such as Friday being the most common day for crimes and 5 PM a popular time for motor accidents [5]. A common issue, however, in these studies was there was little to no documentation on the process. No description of when and how the data was collected and processed, what the plots implied etc. And judging by the dates present in the page, they seem to be fairly old. The questions asked by [6] are, however, very interesting and would form the basis of a lot of my questions. The page, however, lacks documentation completely. Even the name of the dataset or the link to it is missing, which makes it very skeptical. 


## Dataset

For this project, I plan to explore the Crime Incident Reports dataset [4] that is published by the Boston Police Department on all the crimes which were reported between Aug 2015 and Oct 2019. It is a very rich city-level dataset which provides detailed categorization of the crimes along with the time and location of the incident. The dataset can either be collected using the API provided by the Boston Police Department or by directly downloading the CSV file present on their website [4]. For this analysis, we go with the latter. The dataset is release under the Open Data Commons Public Domain Dedication and License (PDDL) [4].

The dataset consists of three files which can be downloaded from [4]:

- **raw_data.csv**
This dataset is located at [data/raw_data.csv](data/raw_data.csv). It is the most important file in this analysis which contains details on what crime happened when and where. A detail description of the columns is present in the table below. Note, this description is partially present in one of the files [data/rmscrimeincidentfieldexplanation.xlsx](data/rmscrimeincidentfieldexplanation.xlsx) provided by the BPD. This file is ~78.6 MB in size.

| Column | Description |
|--------|-------------|
| INCIDENT_NUMBER | Internal BPD report number |
| OFFENSE_CODE | Numerical code of offense description |
| OFFENSE_CODE_GROUP | Internal categorization of OFFENSE_DESCRIPTION |
| OFFENSE_DESCRIPTION | Primary descriptor of incident |
| DISTRICT | What district the crime was reported in |
| REPORTING_AREA | RA number associated with the where the crime was reported from. |
| SHOOTING | Indicated a shooting took place. |
| OCCURRED_ON_DATE | Earliest date and time the incident could have taken place |
| YEAR | Year component of OCCURRED_ON_DATE |
| MONTH | Month component of OCCURRED_ON_DATE |
| DAY_OF_WEEK | Day of Week component of OCCURRED_ON_DATE |
| HOUR | Hour component of OCCURRED_ON_DATE |
| UCR_PART | Universal Crime Reporting Part number (1, 2, 3) |
| STREET | Street name the incident took place |
| Lat | Latitude where the incident took place |
| Long | Longitude where the incident took place |
| Location | Latitude and Longitude where the incident took place |

- **rmscrimeincidentfieldexplanation.xlsx**
This dataset is located at [data/rmscrimeincidentfieldexplanation.xlsx](data/rmscrimeincidentfieldexplanation.xlsx). It contains decriptions of some of the main columns in [data/raw_data.csv](data/raw_data.csv). Note that this file misses the description of some columns which self explanatory. Description of the columns is present in the table below:

| Column | Description |
|--------|-------------|
| Field Name, Data Type Required | Name of the column in raw_data.csv along with its datatype and the NULL value constraint |
| Description | Description of the column |

- **rmsoffensecodes.xlsx**
This dataset is located at [data/rmsoffensecodes.xlsx](data/rmsoffensecodes.xlsx). It contains a list of all the offense codes along with a description of what they stand for. Description of the columns is present in the table below:

| Column | Description |
|--------|-------------|
| CODE | Offense code value |
| NAME | Name of the offense corresponding to the CODE |


## Research Questions

## Ethical Considerations
The dataset provides only the street information and doesn't narrow it down any further to the building number, etc. Hence, I feel that there are no ethical considerations with this dataset. This information should be released publicly so that people can be aware of what is happening in their neighbourhood and city. One shouldn't have to file a Freedom of Information Act (FOIA) request again and again to keep themselves posted of their surroundings. It is credit to this information that the public can find out and take action when they feel that the crime is rising and the law isn't doing enough.


## Human-Centered Considerations

This project could be very useful for someone who plans move to the Boston city or is already staying there. It contains the most recent data possible (see Limitations). It could help someone understand the crime statistics of the city such as the main places and times where these crimes happen, etc. and help make better decisions about where to stay and which places to avoid in order to stay safe. Survival instinct is one of the most basic instincts to all kinds of life and hopefully this work could help someone improve their chances of getting hurt.

It could be the case that this analysis might result in showing that certain parts of the city are more common for certain crimes. And many-a-times, the areas could be tied down to a certain community but that is not the intent of the study and hence the mapping is not a part of this study or the dataset. The intent here is just to provide information for people to make smarter choices in order to stay safe and I do not wish for any service provider to alter their services based on this information. Moreover, this information is public and provided by the government and could anyway be misused if so were the intentions of people. This project does not aim to aid misuse of any form.


## License

The code for this analysis is released under [MIT License](/LICENSE).

The license of the data source can be found on the download page linked below in the [References](#references) section.


## References

[1] The Normality of Crime - [http://www.d.umn.edu/cla/faculty/jhamlin/4111/Durkheim%20-%20Division%20of%20Labor_files/The%20Normality%20of%20Crime.pdf](http://www.d.umn.edu/cla/faculty/jhamlin/4111/Durkheim%20-%20Division%20of%20Labor_files/The%20Normality%20of%20Crime.pdf)

[2] List of mass shootings in the United States in 2018 - [https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2018](https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2018)

[3] List of mass shootings in the United States in 2019 - [https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2019](https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2019)

[4] Crime Incident Reports - [https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system](https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system)

[5] Boston-Crime-Analysis - [https://github.com/MehtaShruti/Boston-Crime-Analysis](https://github.com/MehtaShruti/Boston-Crime-Analysis)

[6] Boston Crime Analyis | Kaggle - [https://www.kaggle.com/cnchandroo/boston-crime-analysis](https://www.kaggle.com/cnchandroo/boston-crime-analysis)

[7] Workbook: Boston Crime Data Analysis | [https://public.tableau.com/views/Bostoncrimedataanalysis/Story1](https://public.tableau.com/views/Bostoncrimedataanalysis/Story1)
