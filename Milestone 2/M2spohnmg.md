# Support Scripts

## Backend scripts
+ init-db.bat
+ psql.bat
## Project Scripts
## Backend
init-db.bat

Path: /dev-config/mk-vscode-win/init-db.bat
Parameters: none
What/Why: This script configures the database for testing, it creates the database, grants permissions, and sets the testing port for the database.
Who runs: Developers

psql.bat

Path: /dev-config/mk-vscode-win
Parameters: none
What/Why: This script starts postgres sql.
Who runs: Developers

## Framework-Specific Scripts
### Backend Scripts
+ .github/workflows/ci.yml

### Frontend Scripts
+ .github/workflows/ci.yml
+ package.json
+ package-lock.json


a