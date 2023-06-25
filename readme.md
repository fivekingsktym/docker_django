# Docker Django Application


### running docker
```bash 
docker compose up --build
```

### manual docker running
```bash 
# syntax
docker run <port> 8000:8000 <image_name_or_id>

# example
docker run -p 8000:8000 django-docker:0.0.1
```
or
```bash 
docker run -p 8000:8000 bd7ef9bf5d08
```

### manually running pip, django commands inside the container
```bash
# syntax
docker exec -it running_container_name_or_id pip install django

# example
docker exec -it 1f5827f71caf pip install Pillow

docker exec -it 1f5827f71caf python manage.py makemigrations
docker exec -it 1f5827f71caf python manage.py migrate
docker exec -it 1f5827f71caf python manage.py startapp appname
docker exec -it 1f5827f71caf python manage.py createsuperuser


# showing inside folder stuctuer of the container 
docker exec -it 1f5827f71caf -c "ls /app/"

```

### Docker commands
```bash
docker images

docker container ls #both are same
docker ps #both are same


# creating a docker image in the root folder like env
docker save -o filename.tar image_name
docker load -i filename.tar
docker run hello-world:latest


# removing a docker image file
docker rmi --force image_name_or_id
```
