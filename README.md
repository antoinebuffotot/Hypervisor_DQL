![image](https://github.com/user-attachments/assets/28bd66ba-767b-431b-8c6d-c3fdea51b965)

![image](https://github.com/user-attachments/assets/754ac0ca-e96b-41f3-abd9-ddb7cce166ca)

![image](https://github.com/user-attachments/assets/4f60ade2-ad2b-4574-a363-aec50f1e413e)

# Objectives:
These are Hypervisor type dashboards to understand the health of monitred applications displayed as a traffic light.
The project has 2 levels of information :
* Level 0 : overall health of applications as traffic light and based on Level 1 health
* Level 1 : health of the different entities

# Prerequisites:
To make it works, you needs to have the following prerequisites
* Dynatrace SaaS Environnements, data in Grail, version 307+(february 2025) => dashboard not working for Dynatrace Managed Classic
* Segments configured similar as Management Zone ie 1 Segment by Application gathering all entities : Hosts, Processes, Services, Applications, Synthetic
  * See the following good example of Segment implementation : https://github.com/dynatrace-ace-services/simply_smarter_4_platform

# Dashboards
This project contains 3 dashboards:
* Hypervisor Level 0 & 1 - Problem
  * Traffic light displaying the health of the application and related entities based on Problems
 
* Hypervisor Level 0 & 1 (based on indicators) => thresholds to be adjusted 
  * Traffic light displaying the health of the application and related entities based on indicators and thresholds to be selected as Variables:
    * Host : CPU usage : default values green <50%, orange <95%, red | Memory usage : green <50%, orange <95%, red 
    * Service : Availability (based on Failure rate) : default values green >98%, orange >90%, red
    * Database Service : Availability (based on Failure rate) : default values green >98%, orange >90%, red
    * Server : Availability : default values green >98%, orange >90%, red
    * Process : Availability : default values green >98%, orange >90%, red
    * Synthetic (HTTP monitors only) : Availability : default values green >98%, orange >90%, red
* Hypervisor Level 0 (based on indicators)
  * Traffic light displaying the health of the applications => thresholds and tiles to be adjusted (add or remove), depending on the monitored applications

# Deployment
Steps to deploy the Hypervisor dashboard
* Step 1 : download the JSON file
* Step 2 : upload to your Dynatrace environnement
* Step 3 : adapt the dashboard depending on the monitored applications especially Hypervisor Level 0
* Step 4 : adapt the thresholds for the Hypervisor dashboards based on indicators => modification of the Dashboard variables, display them and select the values 


![image](https://github.com/user-attachments/assets/9bda8e2a-5965-4312-80ca-19f344f5b9ee)
