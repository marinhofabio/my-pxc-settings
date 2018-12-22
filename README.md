#### What is Percona Server for MySQL® ?
Percona Server for MySQL® is a free, fully compatible, enhanced and open source drop-in replacement for any MySQL database. It provides superior performance, scalability and instrumentation.

#### Percona Server for MySQL® provides:
* Faster and more consistently run queries;
* Enhanced security with binary log (binlog) encryption and data-at-rest encryption;
* Improved efficiency with server consolidation;
* Delayed or completely avoided sharding;
* Better ROI through lower hosting fees and power usage;
* Percona Server for MySQL;
* Cloud-ready support;

#### What is Percona XtraDB Cluster?
Percona XtraDB Cluster is an open source, cost-effective, and robust MySQL® clustering solution for businesses.

#### Percona XtraDB Cluster provides the following MySQL cluster advantages:
* Cost-effective HA and scalability for MySQL;
* Higher availability;
* ProxySQL load balancer;
* Multi-master replication;
* Increased read/write scalability;
* Zero data Loss;
* ProxySQL-assisted Percona XtraDB Cluster maintenance mode;
* Automatic node provisioning;
* Percona XtraDB Cluster "strict-mode";
* Percona Monitoring and Management compatibility;
* True Multi-master, Active-Active Cluster, Read and write to any node at any time;
* Synchronous Replication, No slave lag, no data is lost at node crash;
* Tightly Coupled All nodes hold the same state. No diverged data between nodes allowed;
* Multi-threaded Slave For better performance. For any workload;
* No Master-Slave Failover Operations or Use of VIP;
* Hot Standby, No downtime during failover (since there is no failover);
* Automatic Node Provisioning. No need to manually back up the database and copy it to the new node;
* Supports InnoDB;
* Transparent to Applications. Required no (or minimal changes) to the application;
* No Read and Write Splitting Needed;
* Easy to Use and Deploy.

#### my-pxc-settings
These are the configuration files of my 5 nodes Percona XtraDB Cluster.
I am able to handle 50.000 concurrent connections on each node and the total that this cluster can handle reaches 250.000 concurrent connections.

I'm running this cluster on 5 Dell PowerEdge m630 servers with 48cpu + 128GB of memory.


