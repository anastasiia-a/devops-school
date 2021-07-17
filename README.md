# EPAM DevOps school final project

## Application (Common task)
Develop a simple (lightweight) 3-tire application (front-end, back-end, database). 
* `Back-end (collects data) must:`
  * Retrieve a portion of data from API (see in your Variant) and store it in a database 
  * Update data on demand 
  * Update DB schema if needed on app’s update

* `Front-end (outputs data) must:`
  * Display any portion of the data stored in the DB 
  * Provide a method to trigger data update process 

* `Database:`
  * Choose Database type and data scheme in a suitable manner.  
  * Data must be stored in a persistent way 
  * It’s better to use cloud native DB solutions like an RDS/AzureSQL/CloudSQL. 

## Individual task
Using API get all data about “Pink Floyd" and store it into your DB:
`kind`, `collectionName`, `trackName`, `collectionPrice`, `trackPrice`, `primaryGenreName`, `trackCount`, `trackNumber`, `releaseDate`.
Output the data for the year of releaseDate (the year is set) in the form of a table and sort them by trackPrice in descending order.

### Acceptance Criteria and presentation 
A short presentation (.ppt or other) which contains description of the solution should be prepared and sent to the commission before a demo session. 
The working application with the pipeline is to be demonstrated live on a “protection of the diploma” session for experts with comments and explanation of the details of the implementation, reasons of choosing tools and technologies. <br>
Detailed requirements/criteria: 

|№|Criteria|Requirements|Related Module|
|-|-|-|-|
|1|`SCM`|Application sources should be placed in Git repository. Branching strategy should be explained.|GIT|
|2|`Tests*`|CI pipeline may contain unit tests, smoke tests, linter check.|CI/CD|
|3|`Quality gate`|CI/CD pipeline should use some quality/vulnerability control tool like a Sonar or Anchore.|CI/CD|
|4|`IaC`|CI/CI and runtime infrastructure should be described as a code using Terraform, CloudFormation, or any similar tool. On the demonstration deployment procedure should be shown.|Cloud, Terraform, Ansible|
|5|`Orchestration`|All non cloud-native tools should be spinned up inside a K8S/OpenShift cluster inside a cloud. Application runtime environments should be inside the cluster too.|Kubernetes|
|6|`Logging`|Infrastructure should have centralized log collection/display system. Logs of the application components and infra components should be collected. |Monitoring and Logging|
|7|`Monitoring`|Infrastructure should have centralized metric collection/display system. Metrics of the application components and infra components should be collected.|Monitoring and Logging|
|8|`Runtime/Deployment`|Runtime infrastructure should have production and non production environments. Deploy/release strategy should be explained.|CI/CD|
|9|`Scalability/redundancy`|Scalability should be provided and demonstrated.|Kubernetes|
|10|`Cloud and Cost efficiency**`|Cloud resources and services must be used for the task. Report about the Cloud resource usage and the cost must be provided in the presentation. It should be efficient (minimal) – in accordance to the solving tasks. You can choose any cloud provider taking into account possible extra costs for the resources.|Cloud|

<i>* Nice to have – optional <br>
** Be careful with the Cloud resource usage and check the costs for not to exceed limits! Switch off your machines when you are not using them! </i>
