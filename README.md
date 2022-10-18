# LabVIEW Data Aquisition - Example VIs
Repository for LabVIEW Templates, Examples &amp; Notes

#Tasks
_How to accomplish basic IO Tasks with LabVIEW VI's_

## Data Aquisition
### Using NI Hardware
![image](https://user-images.githubusercontent.com/97303986/194306769-392716a5-fabf-4ded-ae17-2e05306cdc13.png)

### Using Non NI Hardware

## Signal Generation


## Writing to File
### Including Data Aquisition
![image](https://user-images.githubusercontent.com/97303986/194360677-766b887f-db46-428a-b47b-8f9b2afa268f.png)


## Reading From File



# Topologies
_Reference for Different LabVIEW Code Topologies_

### Single Looped Task
Uses:
- Basic I.O. Testing
- Data Aquisition of =< ~2 datapoints.

### State Machine 
Uses:
- More complex control and automation setup
- Processes with decision trees using data aquired from sensors

### Producer Consumer
Uses:
- Seperation of processes which produce data and consume data at different rates

_LabVIEW has built-in Queue Operation VIs found in the Functions palette >> Data Communication >> Queue Operations._

_Queues are based on the first-in/first-out theory. In the Producer/Consumer design pattern, queues can be initialized outside both the producer and consumer loops. Because the producer loop produces data for the consumer loop, it will be adding data to the queue (adding data to a queue is called “enqueue”)._

_The consumer loop will be removing data from that queue (removing data from a queue is called “dequeue”). Because queues are first-in/first-out, the data will always be analyzed by the consumer in the same order as they were placed into the queue by the producer. Figure 1 illustrates how the Producer/Consumer design pattern can be created in LabVIEW._

![image](https://user-images.githubusercontent.com/97303986/195037373-165fc5dd-34dc-4019-84d6-5642431be564.png) <br>
[Code Snippit](https://ni.scene7.com/is/image/ni/ProducerConsumer%20Design%20Pattern?scl=1)


### Queued Message Handler (QMH)
Uses:
- Nessissary step for implementing robust user interfaces without relying on sensor polling.
- Events based topology

### Delacor QHM (DQMH)
Uses:
- Same as QMH


## Case Study - Counter Program with Different Topologies
https://labviewwiki.org/wiki/Design_Pattern_Case_Study:_A_Simple_Counter


### Writing to TDMS Files
https://knowledge.ni.com/KnowledgeArticleDetails?id=kA03q000000x4PcCAI&l=en-GB
