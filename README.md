# South Shore First Church of God

## Deployment Instructions
### Building Application Locally
0. Ensure you have Docker Desktop installed and running on your computer
1. Clone this repository
1. `cd main-frontend`
1. `docker build -t fcogss .`
1. `docker run -itd -p <port1>:<port2> --name fcogss fcogss`
1. `docker start fcogss`
1. `docker exec -it fcogss bash`

## Pushing to DockerHub
1. `docker login` (use credentials)
2. `docker tag fcogss:latest fcogss/main:latest`
3. `docker push fcogss/main:latest`

## EC2
1. `sudo su`
2. `yum update -y`
3. `yum install docker -y`
4. `Service docker start`
5. `docker login` (use credentials)
6. `docker pull fcogss/main:latest`
7. `docker run -itd -p 443:443 --name fcogss fcogss/main:latest`
8. `docker start fcogss`
9. `docker exec -it fcogss bash`
10. `cd main-frontend/main-frontend`