# Mission1
# https://hub.docker.com/r/jupyter/base-notebook/
mkdir mission

cd mission

mkdir mission1

cd mission1

# create a file docker-compose.yml and edit

version: '3'
services:
  jupyter-tutorial:
    image: jupyter/base-notebook
    container_name: mission1-jupyter-notebook
    ports:
      - "8888:8888"
    volumes:
      - ./work:/home/jovyan/work/
    command: start-notebook.sh --NotebookApp.token=''

# use docker-compose

docker-compose up -d

# go to web

192.168.114.10:8888
