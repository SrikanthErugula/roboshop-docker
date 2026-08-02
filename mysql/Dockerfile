# FROM mysql:8.0
# ENV MYSQL_ROOT_PASSWORD="RoboShop@1"
# COPY db/ /docker-entrypoint-initdb.d


# if u learn docker then u need un-comment the above steps


#sess 71


FROM mysql:8.0
COPY db/ /docker-entrypoint-initdb.d
COPY custum-script.sh /usr/local/bin/custum-script.sh   
COPY chmod +x /usr/local/bin/custum-script.sh
ENTRYPOINT ["/usr/local/bin/custum-script.sh"]

