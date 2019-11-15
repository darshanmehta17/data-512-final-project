# Analysis of Crime Incident Reports - Boston

> Authored by ***Darshan Mehta*** on ***Nov 6, 2019***.


## Motivation

Crime has become so common these days that people are starting to see it as a part of society. The entire collection of movies and TV shows under DC comics depict crime to be deeply rooted in the civilization. There are an endless number of movies and shows which are centered around crime. It has become so commonplace that some even go as far to claim it to be *"an integral part of a healthy society"* [1]. According to Durkheim [1], the amount of deviance in crime remains relatively stable over time. I find that statement a little suspectful. Just considering mass shootings, the crime rate went up by 24% since the last year. The average mass shooting in 2018 was 0.88 per day [2] and bumped up to 1.24 per day in 2019 [3]. While this doesn't negate Durkheim's hypothesis, but it is contradicting enough to spark some curiosity. So, I have taken it upon myself to *investigate* <span style="font-size:30px;">️️️🕵</span> some of the many facets of crime by analysing the reports. Apart from the seasonality, given the data, there are many questions that seem interesting, such as the geopraphical distribution of the incidents, the rate of change according to time-of-day, etc.


## Dataset

For this project, I plan to explore the Crime Incident Reports dataset [4]that is published by the Boston Police Department on all the crimes which were reported between Aug 2015 and Oct 2019. It is a very rich city-level dataset which provides detailed categorization of the crimes along with the time and location of the incident. The dataset can either be collected using the API provided by the Boston Police Department or by directly downloading the CSV file present on their website [4]. For this analysis, we go with the latter. The dataset is release under the Open Data Commons Public Domain Dedication and License (PDDL) [4].


## Ethical Considerations
The dataset provides only the street information and doesn't narrow it down any further to the building number, etc. Hence, I feel that there are no ethical considerations with this dataset. This information should be released publicly so that people can be aware of what is happening in their neighbourhood and city. One shouldn't have to file a Freedom of Information Act (FOIA) request again and again to keep themselves posted of their surroundings. It is credit to this information that the public can find out and take action when they feel that the crime is rising and the law isn't doing enough.


## License

The code for this analysis is released under [MIT License](/LICENSE).

The license of the data source can be found on the download page linked below in the [References](#references) section.


## References

[1] The Normality of Crime - [http://www.d.umn.edu/cla/faculty/jhamlin/4111/Durkheim%20-%20Division%20of%20Labor_files/The%20Normality%20of%20Crime.pdf](http://www.d.umn.edu/cla/faculty/jhamlin/4111/Durkheim%20-%20Division%20of%20Labor_files/The%20Normality%20of%20Crime.pdf)

[2] List of mass shootings in the United States in 2018 - [https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2018](https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2018)

[3] List of mass shootings in the United States in 2019 - [https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2019](https://en.wikipedia.org/wiki/List_of_mass_shootings_in_the_United_States_in_2019)

[4] Crime Incident Reports - [https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system](https://data.boston.gov/dataset/crime-incident-reports-august-2015-to-date-source-new-system)