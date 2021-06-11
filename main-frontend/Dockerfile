FROM alpine:latest

# create new directory for container
RUN mkdir /main
WORKDIR /main

# get codebase
RUN apk update
RUN apk add bash vim git curl nodejs npm
RUN git clone https://github.com/FCOGSS/main-frontend.git

# install packages
RUN npm i -g @angular/cli
RUN cd main-frontend/main-frontend && npm i

# specify HTTPS port and provide entrypoint
EXPOSE 443
ENTRYPOINT ["/bin/bash"]