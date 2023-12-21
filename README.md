# apache_airflow

# Steps to install and run Apache Airflow Using Docker in Windows 11

Install Docker Desktop
Install VScode

# Open CMD run following commands

docker --version
docker-compose --version

#to check installations and their versions within user account

mkdir airflow-docker
cd airflow-docker
code .

# https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html

or google airflow docker compose
# fetching docker-compose.yaml
# copy curl command 

# curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.8.0/docker-compose.yaml'
# but in windows copy link only
# in vscode terminal powershell type

curl 'https://airflow.apache.org/docs/apache-airflow/2.8.0/docker-compose.yaml' -o 'docker-compose.yaml'
# this will download docker-compose.yaml file in current workspace

# now create local repositories
mkdir dags
mkdir logs
mkdir plugins

docker compose up airflow-init
docker compose up
# ignore warnings (if any)
# this will start all 

# open a new powershell terminal, run command to see if all containers are up (starting and healthy)
docker ps

# open browser
localhost:8080
enter both username and password: airflow

# to end service it will stop containers
docker compose down

# if refresh browser, it will be closed!
