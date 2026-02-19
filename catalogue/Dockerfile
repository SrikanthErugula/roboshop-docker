#sess 55
FROM node:20.19.5-alpine3.21 AS build
WORKDIR /opt/server
COPY package.json .
COPY *.js .
# this may add extra cache memory
RUN npm install 


FROM node:20.19.5-alpine3.21
# Create a group and user
WORKDIR /opt/server
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
EXPOSE 8080
# this label content in maven style lo vundi
LABEL com.project="roboshop" \
      component="catalogue" \
      created_by="sivakumar"
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
    
# ikkada developer change cheste change avuthundhi so last rasam 
COPY --from=build /opt/server /opt/server
USER roboshop

# these will not work in build time so ekkada pettina okkate
CMD ["server.js"]
ENTRYPOINT ["node"]





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