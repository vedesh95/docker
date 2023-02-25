docker create hello-world
docker start -a container-id
docker run hello-world
docker ps
docker ps --all

docker system prune
docker logs container-id

docker stop container-id
docker kill container-id

docker exec -it <container-id> <command>
docker exec -i -t <container-id> <command>
-i //connect to stdin  -t //nice formatting 

docker exec -it <container-id> sh //full terminal access inside the context of terminal and sh is a program

docker run -it busybox sh


Dockerfile
FROM alpine
# Step 2: Download and install dependency
RUN apk add --update redis
# Step 3: Tell the image what to do when it starts as container
CMD ["redis-server"]

docker build .
docker run <container-id>
