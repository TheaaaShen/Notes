## Experiences

#### Autonomic

**One line summary**: Used Java to deploy Spring microservices to Kubernetes on AWS

- built several REST APIs for the ride-hailing application including getHistory, update waypoints ... with CQRS architecture
- grpc for proto
- receive live vehicle data via Kafka streams
- some minor tasks like: Conve rt json to protobuf and sent to kafka topic (server)
- Most difficult: getHistory
  - in different state, the data is stored in different stuctures, hard to get all the changes 
  - It goes to almost every part of the system, hard to sync



#### Sociabank

**One line summary**: Used java to support internal regulatory reporting system

- automate the process of daily fetching reports using Java
- In this position, most of the time I was doing a project management job for example, i keep track of every morning meeting and based on that, I created / updated tickets using kanban board JIRA and LeanKit. 



#### Chinese Academy of Sciences

**One line summary**: Optimize the algorithm for the Glycan Structure Identification Software

- rewrote and optimized the core data structure and algorithm for the software

- What it is: 

  - The software simulates a physical glycan identification experiementsΩ which is for a sample glycan structure, we cut randomly 1-3 edges each round and check for similarity with all known structures in the database, if there is no one with the possibility that we require (99%), we cut the fragments for another round. The experiments usually go at most 3 rounds.

- What it used to be: 

  - for one sample glycan,  we do all the cuttings (3 rounds) beforehand. Thus, all possible fragments are stored in a huge tree before any comparison. Carrying this huge data structure for the following numerous calculation is both time-consuming and space-consuming.

- What it is now:

  - basically simulate how the physical experiments goes, the glycon tree only grow when it actually needs another round of cuttings. 

- Why couldn't do this earlier




## Common questions

1. list 3 adj that your collegues may use to describe you
2. Why this company?
3. why would i hire you
4. STAR : 





can you tell me about the team ill be working with

typical day

pay

project of past intern finished