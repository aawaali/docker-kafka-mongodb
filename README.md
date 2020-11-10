# docker-kafka-mongodb
a simple docker compose file for running a kafka node, a zookeeper node, and mongodb. (used for dev puropose) <br>
both kafka and zookeeper docker images are built from a basic official alpine image, and have nothing insalled except oppenjdk8, kafka or zookeeper.
# prerequisites
before running the services, make sure you have both docker and docker-compose installed.
# start
to start the nodes, follow below steps :<br>
  1- in your machine create the directory /data/db in wich mongodb will persist its datas, it allows you to keep the database datas after shutting down the container.<br>
  2- git clone https://github.com/aawaali/docker-kafka-mongodb.git<br>
  3- $ cd docker-kafka-mongodb<br>
  4- $ docker-compose up -d   // this might take a while the first time because it will pull(download) the images in your local repo<br>
  5- add the below line in your /etc/hosts file:<br>
    <pre>127.0.0.1 kafka</pre>
and voila, your kafka and mongodb nodes are up and running, kafka is listening in localhost:9092 , mongodb in localhost:27017<br>
  # stop
  you can stop your kafka and mongodb nodes by typing the below command from docker-kafka-mongodb folder
  <pre>docker-compose down -v</pre>
