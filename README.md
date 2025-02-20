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
  * Traffic light displaying the health of the application and related entities based on indicators and thresholds :
    * Host : CPU usage : green <50%, orange <95%, red | Memory usage : green <50%, orange <95%, red 
    * Service : Availability (based on Failure rate) : green >98%, orange >90%, red
    * Database Service : Availability (based on Failure rate) : green >98%, orange >90%, red
    * Server : Availability : green >98%, orange >90%, red
    * Process : Availability : green >98%, orange >90%, red
    * Synthetic (HTTP monitors only) : Availability : green >98%, orange >90%, red
* Hypervisor Level 0 (based on indicators)
  * Traffic light displaying the health of the applications => thresholds and tiles to be adjusted (add or remove), depending on the monitored applications

# Deployment
Steps to deploy the Hypervisor dashboard
* Step 1 : download the JSON file
* Step 2 : upload to your Dynatrace environnement
* Step 3 : adapt the dashboard depending on the monitored applications especially Hypervisor Level 0
* Step 4 : adapt the thresholds for the Hypervisor dashboards based on indicators => modification of the thresholds in the DQL queries
