I AM STRUGGLING TO CONNECT TO THIS WITH HTTPS

Rather just use HTTP

this is the port setting in the docker-compose.yml file
ports:
      - "0.0.0.0:3000:3000"

so to connect use

http://server ip:3000

for instance
http://192.168.0.171:3000


If you have changed the docker-compose.yml file youhave to restart the container to apply the new config

#stop the container
docker-compose down
# start the container
docker-compose up -d
# verify the new config is being used
docker-compose ps

