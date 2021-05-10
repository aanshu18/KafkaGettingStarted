Configure DNS of local to 8.8.8.8

docker-compose -f kafka-single-node.yml up -d 
 
docker-compose -f kafka-single-node.yml down 

docker exec -it kafka-broker /bin/bash 
 
docker exec -it zookeeper /bin/bash 

//loggiing in zk client
cd /opt/bitnami/zookeeper/bin
.zkCli.sh  


//kafka creates various zk nodes,  
ls / gives all nodes

ls brokers/ids
get /brokers/ids/1001
ls /brokers/topics/
get /brokers/topics/topicName
