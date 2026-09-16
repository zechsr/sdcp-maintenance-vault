# Student Demand-Based Course Planner
## Summary
The goal of this system is to provide a tool to department heads and anyone else involved in planning course sections for upcoming quarters, by analyzing all plans that students have in DegreeWorks and providing ***"critical insights"***.
### Stakeholders
This system will have an impact on many groups at Rose-Hulman, including the Department Heads, the Registrar's Office, and indirectly the students and faculty who will be in the sections scheduled.
#### Users
Department heads use this data for estimating course demand and planning sections. I expect that the Registrar's Office could also be a user, as well as any faculty or staff who assist the dept. heads in determining section scheduling.
## Components
### Frontend Server
- The frontend server uses Next.js, React, and TypeScript
- Several packages are behind. Next.js is on version 15
- The frontend stores the shared api key in `auth-provider.tsx`. This is very problematic.
- I was unable to find any evidence of any tests for the frontend component.
- Anything else
### Backend Server (Spring Boot/Java)
- The backend server uses primarily Java 17, Spring Boot, and PostgreSQL
- Versioning is unclear in the POM, and out-of-date Spring Boot causes build failures.
- The application doesn't register authentication at all if `API_KEY` is missing or empty, which makes all API routes unauthenticated. It prints `Authorization is DISABLED.` and continues running completely exposed.
- Testing Status
	- Tests are under `sdcp-backend/src/test/java` and seem to be substantial.
## Containerization Status
**The system is currently not containerized.** No docker or similar files were easily discovered.
## Deployment Status
The system is not currently deployed.