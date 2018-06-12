# Microservices-with-spring-boot-example

LOAD BALANCING : 
   Like JVM which runs a bytecode(.class file) file there are web containers which will have web server and apllication server.
   All java programs go to application server and all the html,css,js files will go to web server. there would so many web servers 
   and application servers. "A" load abalancer will be in front all these server which will route the client requests to various servers.
   here, Load balancers act as a traffic cop:-)
   
   thus,Load BAlancing is something which will efficiently distrub the traffic network across backend servers.
   for eg,  When we go for a gmail... there will be millions of users using gmail, let's consider 3 people in sam eplace is usiing gmail
   1 person will compose . 2nd will load inbox. 3rd will delete few mails. Every requests comes to mail server so this load balancer will route 
   each and every request to the server.
   
   https://www.nginx.com/resources/glossary/load-balancing/
    

--------------------------------------------------------------------------------------------------------------------------------

there are two applications in this project 1. book store(which runs in 8098) 2. service registry(which runs in 8099).


to get localhost:8761 page, you need to run the service regitry as mvn spring-boot: run

the page that comes under localhost:8671, SPRING EUREKA is from spring actuator,

SPRING ACTUATOR : 

this is something which monitors the data everytime, when there is a change, it will give the status what has been changed immediately. spring actuator is always active.
               
---------------------------------------------------------------------------------------------------------------------------------



TO run: 
    1 cmd,    1. cd serviceregistry 2. mvn spring=boot:run
    2nd cmd,  1. cd bookstore-service 2. mvn spring-boot:run -Drun.arguments="--PORT=8098"
    3rd cmd,  1. cd bookstore-service 2. mvn spring-boot:run -Drun.arguments="--PORT=8099" 
    
    
 in localhost:8671 you will find two instances in your status with port 8098 and 8099 in ds replicas. this means there are two instances 
 in same project which is handled by microservices.you can open those two port and see.A single project holds two instances is the 
 benefit in microservice.
 
 
    
    
    
   
