# Support Scripts
- `init-db.bat`
- `psql.bat`
## Project Scripts
- `sdcp-backend\dev-config\mk-vscode-win\init-db.bat`
- `sdcp-backend\dev-config\mk-vscode-win\psql.bat`
## `init-db.bat`
##### Path:
`sdcp-backend\dev-config\mk-vscode-win\init-db.bat`
##### Required Parameters:
None
##### What the script does:
This script initializes the database, and then calls the `mvnw.cmd` script that launches the rest of the application. I'm fairly confident that it's for testing only, as the url is a localhost.
##### When it should be run:
Presumably when initializing a test database.
##### Who runs the script:
Developers, while developing
## `psql.bat`
##### Path:
`sdcp-backend\dev-config\mk-vscode-win\psql.bat`
##### Required Parameters:
None
##### What the script does:
Ensures that the connection is encoded.
##### When it should be run:
In development only, as far as I can tell.
##### Who runs the script:
Developers, while developing
## Frameworks-Specific Script Types
- `sdcp-backend\.github\workflows\ci.yml`
### `sdcp-frontend`
- `sdcp-frontend-web\.github\workflows\ci.yml`
- `sdcp-frontend-web\package.json`
- `sdcp-frontend-web\package-lock.json`