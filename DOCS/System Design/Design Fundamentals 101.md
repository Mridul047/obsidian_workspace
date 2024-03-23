### Foundational System design Knowledge
	Client-Server Model
	Networking Protocols

### Key characteristics of system
	Scalability
	Availablity

### Actual components of system

### Actual tools used to build system
	etcd
	elastic search
	aws s3

### Basic terminologies
	Client Server Model
	Network Protocols
	Storage
	Latency & Throughput
	Availability
	Caching (Write through cache, Write back cache) 
		Cache eviction -> LRU , LFU , FIFO
	Proxies
	Load Balancer (Server selection strategies)
	Hashing (Consistent Hashing , Rendezvous hasing )
	RDBM (SQL, ACID, DB Index)
		Atomacity -> All unit tasks should be successfull or rolledback
		Consistency -> No stale state
		Isolation -> 
		Durability -> Data stored on disk
	Key-Value Store (etcd, redis, zookeeper mostly used for caching / leader election)
	Other Storage Paradigms
		Blob store -> Used to store massive amount of imgage/video/file (GCS , S3)
		Time series DB -> Used for monitoring (InfluxDB , Prometheus)
		Graph DB -> Used when entity has to many relationships (Neo4J)
		Spatial DB -> Used to store geography info.
	Replication and Sharding
		