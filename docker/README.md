### REQUIREMENT BEFORE RUNNING DOCKER COMPOSE FILES
- Must have docker installed
- Make two environment files: .env.*.docker and .env.mysql. And put this in this folder

### RUN DOCKER-COMPOSE.DEV-ENVIROMENT.YML
docker compose -f docker/docker-compose.dev-environment.yml --env-file docker/.env.mysql -p dev-environment up -d --build



### RUN DOCKER-COMPOSE.BACKEND.BASE.YML
docker compose -f docker/docker-compose.backend.base.yml --env-file docker/.env.mysql up --build

### RUN DOCKER-COMPOSE.NGINX.YML
docker compose -f docker/docker-compose.backend.nginx.yml --env-file docker/.env.mysql up --build


