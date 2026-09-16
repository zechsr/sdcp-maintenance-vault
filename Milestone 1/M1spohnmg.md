# SDCP
## Summary

### Stakeholders
 Dr. Boutell - project owner.
 Dr. Mohan - interested in the output of the project.
 Students - don't actually interact with the SDCP, but they rely on it for the final class offerings.
 #### Users
 Dr. Mohan - so he can optimize the course offerings based off of student data.

## Components
The system's backend interacts with a PostgreSQL database with Java, Spring Boot, and Maven. The system's frontend is web based, and relies on npm and Node.js.
 ### Frontend
 #### Technology it uses: 
 The frontend mostly written in typescript. There are a few scss files as well.
 #### Out-of-Date dependencies:
    Package                            Current   Wanted  Latest  Location  Depended by
    @fortawesome/fontawesome-svg-core  MISSING    6.7.2   7.3.1  -         sdcp-frontend-web
    @fortawesome/free-solid-svg-icons  MISSING    6.7.2   7.3.1  -         sdcp-frontend-web
    @fortawesome/react-fontawesome     MISSING    0.2.6   3.5.0  -         sdcp-frontend-web
    @mkacct/ts-util                    MISSING    3.0.3   5.3.0  -         sdcp-frontend-web
    csv-stringify                      MISSING    6.8.3   6.8.3  -         sdcp-frontend-web
    file-saver                         MISSING    2.0.5   2.0.5  -         sdcp-frontend-web
    http-status-codes                  MISSING    2.3.0   2.3.0  -         sdcp-frontend-web
    next                               MISSING  15.5.25  16.3.5  -         sdcp-frontend-web
    normalize.css                      MISSING    8.0.1   8.0.1  -         sdcp-frontend-web
    react                              MISSING   19.3.0  19.3.0  -         sdcp-frontend-web
    react-dom                          MISSING   19.3.0  19.3.0  -         sdcp-frontend-web

    This is every dependency in the frontend
#### Known security issues
 In the frontend there are 13 vulnerabilities (1 low, 2 moderate, 9 high, 1 critical).

#### Testing Status
    It appears that no tests exist for the frontend.
### Backend
#### Technology it uses:
The backend  uses PostgreSQL, flyaway, Java, Java Maven, and Spring boot.
#### Out-of-Date dependencies:
Every dependency was out of date. The report is too long to paste here, but here is a small snippet:
[INFO] The following dependencies in Dependency Management have newer versions:
[INFO]   ch.qos.logback:logback-classic ....................... 1.5.20 -> 1.6.3
[INFO]   ch.qos.logback:logback-core .......................... 1.5.20 -> 1.6.3
[INFO]   co.elastic.clients:elasticsearch-java ................. 9.2.0 -> 9.5.4
[INFO]   co.elastic.clients:elasticsearch-rest5-client ......... 9.2.0 -> 9.5.4
[INFO]   com.couchbase.client:java-client ..................... 3.9.2 -> 3.12.3
[INFO]   com.datastax.oss:native-protocol ...................... 1.5.1 -> 1.5.2
[INFO]   com.fasterxml:classmate ............................... 1.7.1 -> 1.7.3
[INFO]   com.fasterxml.jackson.core:jackson-annotations ....... 2.20 -> 3.0-rc5
[INFO]   com.fasterxml.jackson.core:jackson-core ............. 2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.core:jackson-databind ......... 2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-avro ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-cbor ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-csv ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-ion ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-properties ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-protobuf ...
[INFO]                                                         2.20.1 -> 2.22.2
[INFO]   com.fasterxml.jackson.dataformat:jackson-dataformat-smile ...
[INFO]                                                         2.20.1 -> 2.22.2
#### Known Security Issues
Security issues cannot be tested without setting up the full environment, but based on how many dependencies were out of date, I imagine there are several. There are also several vulnerabilities associated with Java 17, and since that is what the backened was written with, we can safely assume there are at least 30+. Additionally, even with a missing api key the server still runs and attempts to pass it both ways.
#### Testing Status
 There are tests for the backend.

## Containerization Status
There is an app.yml file in the backend and a .github/workflows/ci.yml in both the front and backend.

## Deployment Status
The system is currently deployed but with a limited number of users.