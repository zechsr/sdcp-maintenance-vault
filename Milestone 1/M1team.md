# Student Demand-Based Course Planner
## Summary
The goal of this system is to provide a tool to department heads and anyone else involved in planning course sections for upcoming quarters, by analyzing students' plans to take CSSE courses in DegreeWorks and providing digestible data.
### Stakeholders
- Dr. Boutell
	- Project owner.
- Dr. Mohan
	- Interested in the output of the project.
- Students
	- They don't actually interact with the SDCP, but they rely on it for the final class offerings.
- Other Department Heads
	- The project could be expanded to work with other departments and their course offerings.
#### Users
- CSSE department head
	- The CSSE department head is the currently targeted user. This is because they need to be able to plan for the year and each quarter to determine course offerings.
- CSSE Professors
	- Other professors in the CSSE Department will also be using this software for the same purposes.
## Components
The system's backend interacts with a PostgreSQL database with Java, Spring Boot, and Maven. The system's frontend is web based, and relies on npm and Node.js.
### Frontend
#### Technology it uses:
The frontend server uses Next.js, React, and TypeScript.
#### Out-of-Date dependencies:
Most of the packages in the frontend are a few versions behind. These are the out-of-packages that the system requires:

    Package                            Wanted  Latest  Location  Depended by
    @fortawesome/fontawesome-svg-core  6.7.2   7.3.1  -         sdcp-frontend-web
    @fortawesome/free-solid-svg-icons  6.7.2   7.3.1  -         sdcp-frontend-web
    @fortawesome/react-fontawesome     0.2.6   3.5.0  -         sdcp-frontend-web
    @mkacct/ts-util                    3.0.3   5.3.0  -         sdcp-frontend-web
    next                               15.5.25  16.3.5  -         sdcp-frontend-web
#### Known security issues
- In the frontend there are 13 vulnerabilities (1 low, 2 moderate, 9 high, 1 critical).
- The frontend stores the shared api key in `auth-provider.tsx`. This is very problematic.
#### Testing Status
There are no tests for the frontend.
### Backend
#### Technology it uses:
The backend  uses PostgreSQL, Flyaway, Java, Java Maven, and Spring boot.
#### Out-of-Date dependencies:
Every dependency was out of date. Versioning in the `pom.xml` is potentially unclear.
#### Known Security Issues
Security issues cannot be tested without setting up the full environment, but based on how many dependencies were out of date, I imagine there are several.
- There are also several vulnerabilities associated with Java 17, and since that is what the backend was written with, we can safely assume there are at least 30+.
- Additionally, even with a missing api key the server still runs and attempts to pass it both ways.
#### Testing Status
Tests are under `sdcp-backend/src/test/java` and seem to be substantial.
## Containerization Status
**The system is currently not containerized.** No docker or similar files were easily discovered.
## Deployment Status
The system is currently deployed on the Rose-Hulman CSSE server.
	The production server is accessible at [this url](https://sdcp.csse.rose-hulman.edu).
- The system is staged at [this url](https://sdcp-stage.csse.rose-hulman.edu).
## Project Owner Conversation Summary
### Goal of this software
- Assists faculty in determining majors, year, etc. of students who plan to take courses what term, in order to get an idea of how many sections to offer.
- It needs to be able to easily accept new `.csv` files and operate on them.
### Known issues with the system
- We can't currently upload new `.csv` data from the frontend ui.
- Dr Boutell is dissatisfied with the lack of information the system provides.
- #### Security:
	- Should be increased from "secret password", but not as important to Dr Boutell as additional functionality.
	- Servers had SSL certificates that were expiring, so they were taken down.
- Number of students on website is different from number in spreadsheet.
- The spreadsheet contains dummy classes that shouldn't be included.
- All(?) dependencies are out of date.
### Frequency of Use
- Sees infrequent use except for a heavy load four times each year.
	- Used early in the quarter every quarter, and again after advisor meetings in the spring.
### Main features
- The software receives a `.csv` file and runs a basic algorithm to determine how many students of what years are planning to take any given CSSE course.
- Presents the data in a comprehensive manner.
### Etc.
- Most important new feature to Dr Boutell is **uploading .csv files**. Next is probably additional filtering capabilities (filter by student year and quarter).
	- This will unfortunately be deprioritized until the system is standardized.