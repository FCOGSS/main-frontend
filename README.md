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