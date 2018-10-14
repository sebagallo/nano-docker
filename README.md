# Docker-Compose for example full App

This `docker-compose.yml` creates:
* mongodb instance (not visible to the outside)
* express.js server (exposed on port 8085)
* react client (exposed on port 8086)

## Configuration
* MONGO_INITDB_ROOT_USERNAME / DB_USER
* MONGO_INITDB_ROOT_PASSWORD / DB_PASS
* REACT_APP_API_URL

Is is important to change the REACT_APP_API_URL parameter if you aren't going to run this docker-compose in your local machine.
If you're running this on a remote server, change the REACT_APP_API_URL with that of the server.

## Running

If you didn't recursively clone this repo, run :
* `git submodule init`
* `git submodule update`

After this is done, you can run: 
* `docker-compose up` to start building the images and attach yourself to the logs

__OR__
* `docker-compose up -d` to build & detach, running the docker containers in the background