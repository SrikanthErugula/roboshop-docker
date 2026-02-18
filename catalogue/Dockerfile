#sess 55
FROM node:20.19.5-alpine3.21 AS build
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# # this may add extra cache memory
# RUN npm install 


WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
CMD ["node", "server.js"]
#CMD ["sleep", "10000"]





#ses- 54 
# # https://hub.docker.com/_/node   ---> image comes from here for base OS

# FROM node:20 
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# ENV MONGO="true" \
#     MONGO_URL="mongodb://mongodb:27017/catalogue"
# CMD ["node", "server.js"]
# #CMD ["sleep", "10000"]