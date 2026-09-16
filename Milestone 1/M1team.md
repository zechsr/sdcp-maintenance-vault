*First, combine individual .md files*
![[M1spohnmg]]

![[M1zechsr]]
# Project Owner Conversation Summary
## Goal of this software
- Determine majors, year, etc. of students who plan to take courses what term, to get an idea of how many sections to offer.
- Handle the csv files as they come in.
## Known issues with the system
- Can't currently upload new csv data.
- Limited data viewing.
- ### Security:
	- Should be increased from "secret password", but not as important to Dr Boutell as additional functionality.
	- Servers had SSL certificates that were expiring, so they were taken down.
- Number of students on website is different from number in spreadsheet.
- The spreadsheet contains dummy classes that shouldn't be included.
- All(?) dependencies are out of date.
## Frequency of Use
- Really only used about three-four times each year. Once in particular, in the spring.
	- Used early in the quarter.
## Main features
- Take in a .csv file from the registrar that contains all student plans in DegreeWorks, and aggregate the data to determine.
- Presents the data in a useful manner.
- Determines how many sections of a class should be open based on DegreeWorks.
- Determine the importance of having sections open based on the years of the students who want to take it.
## Etc.
- Most important feature to Dr Boutell is **uploading .csv files**. Next is probably more filtering capabilities (filter by year).