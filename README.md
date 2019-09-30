# POSTGRESQL REPLICATION BY USING PHP FRAMEWORK

  SilverStripe is used exclusively by the New Zealand government, multiple Australian and UK government entities and broadly in business worldwide is a PHP framework. Currently, it is connected to one database for all its records which prevents further scaling. Our project is to scale up this database horizontally and to create database for replication. We are using postgresql database for replication of master and slave in docker.
 

# PREREQUISITES
    docker toolbox 
    docker compose
    virtual box machine



# HOW TO CREATE DOCKER ENVIRONMENT
After installing docker toolbox start docker toolbox with command: docker start and before running containers give command: docker ps for showing all running containers in docker toolbox.Before start running containers check docker toolbox version for latest to prevent issues by giving command: docker version.


# CREATION OF DOCKER COMPOSE.YML FILE
Create docker compose file by making directory in docker toolbox program files.To create docker compose folder in program files give command: cd (folder name)/.

For making directory give command: mkdir (folder name)/

For creating file name give command: Touch (file name.yml)

create yml.file with version of docker and services used are php,apache,postgresql giving ports for each services.
give volume and environment for each service.




# RUNNING DOCKER COMPOSE FILE
 
 For running docker-compose.yml file 
        command: docker-compose.yml up -d/
 
 To stop running containers
        command: docker-compose.yml down


# REPLICATION POSTGRESQL 

For scaling postgresql database.
        command: Docker-compose.yml up –d –scale database=2
 
# Credentials
php does use SQL server credential, please check the corresponding server image for information how it is setup.

The official postgreSQL use following environment variables to define these:

postgreSQL_ROOT_PASSWORD - This variable is mandatory and specifies the password that will be set for the root superuser account.

postgreSQL_USER, postgreSQL_PASSWORD - These variables are optional, used in conjunction to create a new user and to set that user's password.
