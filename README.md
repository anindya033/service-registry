Planned Micro-service Architecture:
URL: https://www.youtube.com/watch?v=HFl2dzhVuUo&t=2208s

Service Registry
•	Description: A discovery server (using Netflix Eureka) that allows services to register themselves and discover others.
•	Purpose: Enables service discovery for dynamic scalability and load balancing.
•	Interaction: Tracks the instances of Department Service and Employee Service.
 

All Description
This is a micro-services architecture built using the Spring Boot framework and Netflix OSS components. Here's a breakdown of each service:
1.	Config Server
•	Description: Acts as a central configuration repository for the micro-services. It allows dynamic configuration changes without redeploying the services.
•	Purpose: Ensures consistent configuration management across all services.
•	Interaction: Provides configurations to Department Service, Employee Service, and other components.
2.	API Gateway
•	Description: A central entry point for all client requests, providing routing, security, and load balancing.
•	Purpose: Acts as a single point of communication between the client and micro-services.
•	Interaction: Routes requests to Department Service and Employee Service
Service Registry
•	Description: A discovery server (using Netflix Eureka) that allows services to register themselves and discover others.
•	Purpose: Enables service discovery for dynamic scalability and load balancing.
•	Interaction: Tracks the instances of Department Service and Employee Service.
4. Department Service
•	Description: A microservice responsible for handling department-related functionality.
•	Purpose: Manages department data and operations.
•	Interaction: Communicates with Employee Service for cross-service coordination. Sends tracing information to Zipkin.
5. Employee Service
•	Description: A microservice dedicated to employee-related functionality.
•	Purpose: Manages employee data and operations.
•	Interaction: May depend on Department Service for department-specific details. Sends tracing information to Zipkin.
6. Zipkin
•	Description: A distributed tracing tool for visualizing and troubleshooting latency issues.
•	Purpose: Captures and monitors traces (logs) from Department Service and Employee Service.
•	Interaction: Collects trace data from services to analyse inter-service calls and performance


