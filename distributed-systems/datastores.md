## Summary of Tech to Study

* AWS (389)
    * http://www.amazon.com/Amazon-Services-Action-Andreas-Wittig/dp/1617292885/
    * Bought.
* MongoDB (200)
    * Very popular, believe it or not...
    * http://www.amazon.com/MongoDB-Definitive-Guide-Kristina-Chodorow/dp/1449344682
* Redis (144)
    * http://www.amazon.com/Redis-Action-Josiah-L-Carlson/dp/1617290858
    * Bought.
* Docker (135)
    * http://www.amazon.com/Docker-Up-Running-Karl-Matthias/dp/1491917571/
* ElasticSearch (106)
    * http://www.amazon.com/Elasticsearch-Action-Radu-Gheorghe/dp/1617291625
    * People also like: http://www.amazon.com/Elasticsearch-Definitive-Guide-Clinton-Gormley/dp/1449358543/
* Cassandra (89)
    * Prolly can ignore HBase then.
    * http://www.amazon.com/Learning-Apache-Cassandra-Tolerant-Real-Time/dp/1783989203
* Kafka (82), or maybe RabbitMQ (66)
    * http://www.amazon.com/RabbitMQ-Action-Distributed-Messaging-Everyone/dp/1935182978
    * No respected Kafka books...
* Neo4j (13)
    * http://www.amazon.com/Neo4j-Action-Aleksa-Vukotic/dp/1617290769/
* Spanner/F1

## Google Tech

* BigTable (== HBase (57))
    * Uses LSM trees to build a distributed DB on top of GFS.
    * No transactionality outside the row level.
* Borg (== YARN (14), Mesos (35))
    * Cluster management system.
    * TODO: what's the difference between YARN and Mesos.
* Caffeine/Percolator: continuous indexing system.
* Chubby (~= Zookeeper (32))
    * Basically their Paxos implementation. Used for locks.
* Dremel (== Apache Drill (5), Cloudera Impala (11))
    * Interactive querying of huge datasets.
* F1
    * Distributed SQL database on top of Spanner.
* FlumeJava (~= Cascading (7), Cascalog (0), Scalding (1))
    * Makes it easier to build MR workflows.
    * Cascalog and Scalding are built on top of Cascading.
    * Cascalog is for Clojure, Scalding for Scala.
* GFS/Colossus/Megastore (== HDFS (17))
    * GFS is the distributed FS, has a master, uses multiple replicas.
    * Optimizes for append-only behavior.
    * TODO: Not sure how Colossus/Megastore improve on GFS.
* MapReduce (== Hadoop (175))
    * Simple distributed batch computation.
* Pregel
    * Graph processing framework. Not a lot of interest in this.
* Sawzall (~= Pig (35), Hive (55))
    * Simpler query language.
* Spanner (semi-relational)
    * I think that the big idea is global distributed transactions.
    * I believe that CockroachDB is a copy of this?

## Other

* Amazon Dynamo (== Cassandra (89); Riak (7))
    * DHT basically. Basically an implementation of Chord.
    * No transactions; always available. Eventually consistent in face
      of partition.
    * Riak appears more true to Dynamo, while Cassandra hybridizes
      ideas from BigTable.
* Datomic (0)
    * Not widely used, but a DB which is "fact"-based. Immutable rows;
      records all history.
* Docker (135)
    * TODO
* ElasticSearch (106) (Solr (41)/Lucene (20))
    * Basically a search index. Distributed. Incremental indexing.
* Kafka (82)
    * This is basically a distributed message queue. But it also keeps
      a log of all messages (subject to limited retention), so clients
      can play back from any point.
* Memcached (42)
    * In-memory key-value store. Distributed.
* MongoDB (200)
    * This is a distributed document store. I'm not sure why people
      really like this one so much.
* Neo4j (13)
    * Graph database.
    * I guess Facebook TAO would be an alternative?
* RabbitMQ (66)
    * TODO
* Redis (144)
    * In memory key-value store (with some durability).
    * Mainly used as a cache, but has provides datastructures and
      primitives, which are a little different.
* Spark (119)
    * Basically just a new version of Hadoop with more features.
    * Much easier to build networks of jobs.
    * Integrates HiveQL as SparkSQL.
    * Tries to be in-memory, so faster for iterative algorithms,
      ad-hoc queries.
    * Builds in a streaming ability to compete with Storm.
    * Focused on ML, in particular, by giving you in-memory datasets.
* Storm (46)
    * An event processing framework. Events filter through a topology;
      at the end, results are typically written to a DB like
      Cassandra.

## Randos

None of these seem hyper-popular. Not very knowledgable about any, and
kinda don't care.

* Aerospike (2)
* C-Store (1)
* CitusDB (0)
    * TODO
* CouchDB (10)
* FoundationDB (0) (An F1 clone? Acquired by Apple.)
* Greenplum (5)
* InfiniDB (0)
* InfiniSQL (0)
* InfluxDB (1)
* LevelDB (0)
    * Google project. An LSM implementation.
* MemSQL (1) (in memory DB, plays nice with flash)
* Redshift (33)
* RethinkDB (4) (document store with joins and group by)
* RocksDB (0)
    * A fork of LevelDB optimized for SSD I think.
* Samza (3)
    * A competitor to Storm. Basically a one-to-one competitor;
      differences appear minor.
    * Most significant difference may be it tries to preserve
      processor state, so that if a stream processor fails, its local
      state can be recovered.
* TokuDB (0)
    * I believe this is just a fork of MySQL with the fractal tree
      trick.
* Vertica (11)
* Voldemort (0)
    * This competes with HBase/Cassandra, but is not widely used and
      not that interesting to me.
* VoltDB (0)

There are also a bunch of AWS services that I ignored.

## Resources

* https://github.com/onurakpolat/awesome-bigdata

## Other Randoms

Don't know that I care about these, but they were correlated with data
science jobs.

* Ansible (88)
* Tableau (25)
* Kubernetes (18)
