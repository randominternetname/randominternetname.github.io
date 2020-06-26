---
layout: post
title: Visualizing Allegations Against the NYPD
---
![Screenshot of Visualization]({{ site.url }}/images/strawberries.jpg)

[Link to my Tableau Dashboard](https://public.tableau.com/shared/DYHY72DXN?:display_count=y&:origin=viz_share_link)

# The Problem

Police brutality is an ongoing crisis in the United States. It's important for citizens to have access to transparent data if we're going to enact lasting change, and I decided to develop a user-friendly tool for New Yorkers.  Of the 17 different Law Enforcement Agencies in New York City[^fn-agencies], I dug into NYPD data to see what I could find.


### Crime Rates?

As seen in my dashboard, the crime rate has decreased by 13% since 2006.[^fn-crime-reports]  This tracks the national average over the same timespan, suggesting that the number of crimes are not dependant on the police budget nor on the population which only grew 2%.[^fn-population]  The number of civilian allegations against the NYPD varies greatly and does not seem to be related to the crime rate.[^fn-complaints1]<sup>,</sup> [^fn-complaints2]<sup>,</sup> [^fn-complaints3]


### Police Department Budgets?

The NYPD budget has nearly doubled from $3,400,000,000 to $6,000,000,000.[^fn-budget]  The number of civilian allegations against the NYPD also does not correlate with changes in the NYPD budget.


## Other Potential Impacts
### A few bad apples?

The [Citizens Police Data Project](https://beta.cpdp.co/) in Chicago has a really wonderful heat map of civilian complaints going back to 1988.  Because the disiplinary records of officers in Chicago are a matter of public record, complaints are tied directly to named officers.  The CPDP seems to have found that there is transmissibility of poor/violent behaviour.

The data available from NYC does not contain officer names and, in fact, disciplinary records were closed until recently.[^fn-discipline] Therefore, I cannot identify if specific officers within the NYPD are causing the majority of complaints. 


### Use of Force Limitations?

Organizations such as [8 Can't Wait](https://8cantwait.org/) suggest several limitations and guidelines on use of force to cut down on or eliminate instances of police brutality: 

* Forbidding chokeholds
* Requiring de-escalation when possible
* Forbidding shooting at/from moving vehicles, at people fleeing, or to protect property
* Forbidding the use of batons, tasers, pepperspray on passive resisters
* Requiring warning before using force
* Requiring reporting on all uses of force
* Requiring intervention when other officers use excessive force 

All of these guidelines have been in place for the NYPD since 2016, with some in place since the 1960's.[^fn-force]

### De-militarization?[^fn-militarization]<sup>,</sup> [^fn-militarization-research]

I find the militarization of the police really disturbing and was hoping to explore the relationship between increased police armaments and decreased community relationships with the police.  The [Marshall Project](https://www.themarshallproject.org/2014/12/03/the-pentagon-finally-details-its-weapons-for-cops-giveaway#dod-graphic) has an easy to use tool for equipment transferred from the start of the 1033 Program to 2014.  For the raw data, I found the [Defense Logistics Agency's Law Enforcement Support Office](https://www.dla.mil/DispositionServices/FOIA/EFOIALibrary/) which provides equipment through the 1033 Program.  However, there are only 1138 records from 1998 to mid 2018.  So either they are not the main supplier of military equipment to the NYPD or there are records which I don't have access to.  (I did see some crazy things in that data, like dozens of rifles being transferred to multiple state universities.)[^fn-abuses_ten_thirty-three]

### Increasing Community Investment?
One study of 264 cities found that for every ten communnity organizations there are significant reductions in crime (4% for property crimes, 6% for violent crimes, 9% for murders).[^fn-community]  

### Limiting Overtime Worked by Officers?
When officers work more than 40 hours per week, their use of excessive force has been found to increase exponentially.[^fn-overtime]
 
### DOJ Collaborative Reform?
The Department of Justice has two methods to address police departments struggling with high rates of excessive force.  Through either collaborative reform or a consent decree, the Justice Department’s Community Oriented Policing Services Office investigates and recommends policy updates.  When adopted, these reforms decrease police shootings by over 20%.[^fn-DOJ] 

## For More Information, I Recommend These Resources:
* [Open The Books - DLA map searchable by zip code](https://www.openthebooks.com/maps/?Map=1&MapType=Pin&Zip=20740)  
* [NYC Budget allocated to paying settlements against the NYPD](https://data.cityofnewyork.us/City-Government/Claims-Report-Underlying-Settlements-and-Claims-Fi/ex6k-ym48)  
* Samuel Sinyangwe, Founder of [Police Score Card](https://policescorecard.org/) has an amazing list of resources in this [Twitter thread](https://twitter.com/samswey/status/1180655701271732224)  
* [Police Misconduct Cases 2011-2015, PDFs acquired by BuzzFeed News](https://www.buzzfeednews.com/article/kendalltaggart/nypd-police-misconduct-database)  

[^fn-discipline]: [Law repealed that kept police disciplinary records hidden](https://brooklyneagle.com/articles/2020/06/10/new-york-passes-bill-to-unveil-police-discipline-records/)  
[^fn-agencies]: [NYC LEA](https://en.wikipedia.org/wiki/List_of_law_enforcement_agencies_in_New_York_(state)#New_York_City_agencies)
[^fn-crime-reports]: [Crime data as logged by the city](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i/data)  
[^fn-population]: [New York City's population by year](https://worldpopulationreview.com/us-cities/new-york-city-population/)  
[^fn-complaints1]: [Complaints received against the NYPD](https://data.cityofnewyork.us/Public-Safety/Civilian-Complaint-Review-Board-CCRB-Complaints-Re/63nx-cpi9)  
[^fn-complaints2]: [Complaints closed per year](https://data.cityofnewyork.us/Public-Safety/Civilian-Complaint-Review-Board-CCRB-Complaints-Cl/fx4z-5xg2)  
[^fn-complaints3]: [Allegations closed per year](https://data.cityofnewyork.us/Public-Safety/Civilian-Complaint-Review-Board-CCRB-Allegations-C/xyq2-jjkn) Note that allegations may contain multiple complaints.  
[^fn-budget]: [NYPD Budgets by Year](https://council.nyc.gov/budget/)  
[^fn-abuses_ten_thirty-three]: [Some instances of abuse](https://www.acfcs.org/from-warfighter-to-crimefighter-the-us-1033-program-and-the-risk-of-corruption-and-misuse-of-funds/)  
[^fn-militarization]: [OpenTheBooks.com Oversight Report](https://www.openthebooks.com/assets/1/7/Oversight_Report_-_The_Miltarization_of_America_-_Traditional_Law_Enforcement_Agencies_Raw_Data_Report.pdf )_  
[^fn-militarization-research]: [Research into the effects of militarization](https://www.pnas.org/content/115/37/9181)  
[^fn-force]: [NYPD Use of Force Guidelines](https://www1.nyc.gov/assets/ccrb/downloads/pdf/investigations_pdf/pg221-01-force-guidelines.pdf)  
[^fn-community]: [Community funding research](https://journals.sagepub.com/doi/abs/10.1177/0003122417736289)  
[^fn-overtime]: [King County Overtime Audit](https://www.kingcounty.gov/~/media/depts/auditor/new-web-docs/2017/kcao-overtime-2017/kcao-overtime-2017.ashx?la=en)  
[^fn-DOJ]: [DOJ collaborative reform](https://www.vice.com/en_us/article/kznagw/jeff-sessions-is-walking-away-from-the-best-way-to-reduce-police-shootings)  


## Tools
* Tableau
* pandas
* pickle
* html
* JavaScript