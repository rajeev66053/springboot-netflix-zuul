# springboot-netflix-zuul

* API gateway providers for microservices:
    1. Netflix zuul
    2. Spring cloud gateway
    
* Advantages of API gateway
    1. Seperation between clients and microservices
    2. Simplified clients
    3. Any changes in location of microservices is not going to affects the clients.
    4. Optimal API for each client as per requirement.
    
* Drawbacks of API Gateway
    1. Complexity
    2. Latency
    3. One point failure

* In springboot 2.7.1 version the zuul gateway version doesnot match and throw error. To fix this issue we have create `ZuulConfiguration` configuration file to create a bean. Reference: https://gist.github.com/aldobongio/6a22f49863c7a777612f7887bbb8fd1d
* In zuul we can open doctor service using api gateway using:
	> http://localhost:8100/doctor-service/doctors
	
Here the first parameter `doctor-service` is from the api-gateway application.properties and second parameter `doctors` is form doctors GetMapping of doctors methods of MasinController in doctor service.

