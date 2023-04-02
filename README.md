# ckan-wakeua docker-compose fro production

## Usage

### Install 
- Docker: https://docs.docker.com/get-docker/

### Configure
Inside *prod* folder we can configure environment variables and other services options.

### Run
Download and build the corresponding images
```
git clone https://github.com/docpad/dockerfile.git

cd prod

docker-compose up -d
```

### Create user
Create an user to start uploading data.
```docker exec -it ckan /usr/local/bin/ckan -c /etc/ckan/production.ini sysadmin add newuser```
Log in the web and generate an 
### Services

| Service    | Port | Description                                                   |
|------------|------|---------------------------------------------------------------|
| CKAN       | 5000 | CKAN with standard extensions                                 |
| solr       |      | A pre-built SolR image set up for CKAN.                       |
| postgres   |      | CKAN’s database, later also running CKAN’s datastore database |
| redis      |      | A pre-built Redis image                                       |
| datapusher | 8800 | A pre-built CKAN Datapusher image                             |

