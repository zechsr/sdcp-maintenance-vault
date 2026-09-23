# Support Scripts

### Backend scripts
+ `init-db.bat
+ `psql.bat
## Project Scripts
### Backend

### `init-db.bat
#### Script details
##### Path: 
`/dev-config/mk-vscode-win/init-db.bat

##### Required Parameters: 
none

##### What the script does: 
This script configures the database for testing, it creates the database, grants permissions, and sets the testing port for the database.

##### When it should be run:
Only during development to start a test database.

##### Who runs the script:
Developers

## `psql.bat
#### Script details
##### Path: 
`/dev-config/mk-vscode-win/psql.bat

##### Required Parameters: 
none

##### What the script does: 
This script starts postgres sql and ensures that the connection is in UTF-8 or UTF-7.

##### When it should be run: 
Only during development.

##### Who runs the script:
Developers

## Framework-Specific Scripts
### Backend Scripts
+ .`github/workflows/ci.yml
+ `mvnw.cmd

### Frontend Scripts
+ `.github/workflows/ci.yml
+ `package.json
+ `package-lock.json
