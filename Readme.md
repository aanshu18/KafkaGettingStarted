Configure DNS of local to 8.8.8.8

docker-compose -f kafka-single-node.yml up -d 
 
docker-compose -f kafka-single-node.yml down 

 docker exec -it kafka-broker /bin/bash 
