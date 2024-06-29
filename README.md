## Requirements
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Start and build the docker-compose file
```bash
docker compose up
```

## Connect to pgAdmin
- Open a browser and go to http://localhost:5050
- Login with the credentials PGADMIN_DEFAULT_EMAIL and PGADMIN_DEFAULT_PASSWORD

## Retrieve the IP address to connect to the Postgres database for the configuration of pgAdmin
```bash
docker container ls
# Then get the container id of image postgres
docker inspect <container_id>
# Then get the IP address of the container (e.g. "IPAddress": "172.18.0.2")
```

## Create a new database
- Click on the "Add New Server" button.
- In Connection tab, fill in the IP address.
- Username will be POSTGRES_USER and Password POSTGRES_PASSWORD
- Database name will be POSTGRES_DB
- Click on "Save" button.