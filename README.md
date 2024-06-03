## Docker
```powershell
docker pull nginx
docker images
docker run nginx
docker container ls/ docker ps
docker stop CONTAINER_ID/ NAMES
docker start CONTAINER_ID/ NAMES
docker rm CONTAINER_ID
docker rm -f $(docker ps -aq) #remove all container but running container then -> -f
docker run --name NAME -d -p 8080:80 -p 3000:80 nginx:latest
$FORMAT="ID`t{{.ID}}`nNAME`t{{.Names}}`nIMAGE`t{{.Image}}`nPORTS`t{{.Ports}}`nCOMMAND`t{{.Command}}`nCREATED`t{{.CreatedAt}}`nSTATUS`t{{.Status}}`n"
docker ps --format=$FORMAT
docker run --name Queries -v ${PWD}:/usr/share/nginx/html:ro -d -p 8080:80 nginx
docker exec -it Name bash
docker run --name bootstrap2 --volumes-from Queries -d -p 8081:80 nginx
docker build --tag website:latest .
```
