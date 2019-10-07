## How to be a good back-end dev

#### Tools

- Iterm2 (fancy addup)

- GitHub tab 

#### CQRS



#### Kubernetes 

- containerization
- Cheat sheet
  - usually config is yaml
  - `kubectl explain pods`
  - `kubectl describe pods my-pod`
  - `kubectl scale --replicas=3` scale pods up/down
  - `kubectl delete pod`
  - `kubectl logs -f my-pod`
  - `kcd/kcs/kcp alfa`

#### Db.rb (posgres)

- ./scripts/db.rc + database_name
- \dt all tables
- \d + table_name columns 
- select count(*) from table_name order by time desc;

#### gRPC

- open source remote procedure call system
  -  defining a service, specifying the methods that can be called remotely with their parameters and return types
- uses protocal buffer as the interface description language
- features like authentication, bidirectional streaming and flow control, blocking or nonblocking bindings, and cancellation and timeouts 
- Connect services
- blockingstub
- invokeWithRetry()

#### KAFKA

- A streaming platform has 3 key caps:
  - publish and subscribe to streams of records, similar to a message queue or enterprise messaging system
  - store streams of records in a fault-tolerant durable way
  - process streams of records as they occur
  - 
- kstream vs ktable vs globalktable
  -  ktable is partitioned over all kafkastream instance
  - globalktable is fully replicated per kafkastream instance

#### GDIA

#### Github

- if branch is some before some above; 
  - git rebase --hard origin/rc
  - git push
- if want to check specific commit from develop to rc
  - git cherry-pick SHA
  - git push -f
- git rebase -i
- 

#### Java Spring

- Dependency:
  - Hazelcast
    - let one pod to be the master pod and only master pod run scheduled jobs, other pods sharing the same data (map) instead of each grabbing its own data
  - lombok
    - @getter @setter
  - @slf4j
    - Log.info / log.debug
- Annotations
  - `@Bean`
  - `@Component`
  - `@ConfigurationProperties()`
  - `@Configuration`
  - `@profile`
  - `@scheduled`
    - FixedDelay / InitialDelay / FixedRate / CronExpression
  - @mockmvc
- Words?
  - `Serializable`
    - an object can be represented as a sequence of bytes that includes the object's data as well as information about the object's type and the types of data stored in the object
    - `serialVersionUID` used during deserialization to verify that the sender and receiver of a serialized object have loaded classes for that object that are compatible with respect to serialization
  - dead letter queue
  - 



#### What did i do

- Convert json to protobuf and sent to kafka topic (server)
- 