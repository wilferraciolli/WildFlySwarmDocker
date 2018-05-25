## How to run this micro service

- Firstly do a `mvn clean install`
 - Followed by `mvn wildfly-swarm:run`
 - Or `java -jar target/forge-test-swarm.jar`
 
 Then this will allow to test the endpoint oin localhost:8080/greet
 
 Lastly, it has a docker file which allows to create a container and set some env vars.
 
 To build the image type the following `docker build -t wildfly/swarm .` This will create the docker image based on the dockerFile defined.
 Then you can run the image as follow `docker run -d -p 8080:8080 wildfly/swarm`
 
Then if you want to see the logs for wildFly type the following (where the long id is the container image id) `docker logs -f f117b18b251b7e0fc3ca6456b6214800e0f85da1312f8c21524555cbc54236c9`
   
