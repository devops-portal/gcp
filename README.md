# Google Cloud data storage services
### why using a manged service? 
Using a manged service from Google as a distributed data storage system will save some effort to maintain consistency across multiple instances.

Modern cloud storage solutions scale your data layer automatically so you can focus on your application and not worry about whether your databases can keep up with the load.


## what are the types of storage that GCP provides?

### Relational Data / SQL
**[**Cloud SQL**](https://cloud.google.com/sql/):** Fully managed hosted service for MySQL or PostgreSQL databases. Google takes care of patches and updates, managing backups, handling failover and configuring replication. Data is automatically replicated across different regions.

[**Cloud Spanner**](https://cloud.google.com/spanner/): Relational SQL database provided by Google Cloud with built-in horizontal scaling capabilities that are automatically handled. Your data can scale up to petabytes in size and also support atomic transactions as with a traditional SQL database. Because of its ability to scale like a NoSQL database, Cloud Spanner comes with a higher price than Cloud SQL.

### Non-Relational Data / NoSQL

[**Cloud Datastore**](https://cloud.google.com/datastore/): NoSQL database which stores data in JSON documents (similar to MongoDB) which are automatically indexed so you can query on individual attributes. An interesting property of Cloud Datastore is that it supports atomic transactions, which means it can execute a set of operations where either all succeed, or none occur. This is similar to a relational database but with the advantage of horizontal scalability found in NoSQL databases. Cloud Datastore can store up to terabytes of data.

[**Cloud BigTable**](https://cloud.google.com/bigtable/): Fully managed wide-column database similar to HBase and Cassandra with automatic scaling up to petabytes of data and offer sub-10ms latency. BigTable Provides easy integration with open source big data tools like Hadoop and uses the popular HBase API. A multi-row atomic transaction is not available in BigTable, instead, atomicity is guaranteed only on per row (columns) basis.

### Data Analysis

[**BigQuery**](https://cloud.google.com/bigquery/): An ideal option when you need to run data analysis on an enormous data set. BigQuery provides extremely fast response when running complex SQL like queries up to petabytes of data.

### File Storage

[**Cloud Storage**](https://cloud.google.com/storage/): Use this option to store any kind of data from audio, video, images or other files. Cloud Storage has extremely high read and write speeds, and has nearly unlimited (exabytes) storage limit. Scaling is automatically taken care of, and files are replicated geo-redundantly on multi-region and dual-region locations for high availability and backup.

### Memory

[**Cloud Memorystore**](https://cloud.google.com/memorystore/): Redis compatible in-memory data store that is fully managed by Google enabling high availability, failover, patching, and monitoring. Cloud Memorystore provides extremely fast I/O and low latency of up to 300 GB per instance — ideal for storing application states, sessions, and data caching. You can easily achieve the sub-millisecond latency and throughput your applications need.

### Mobile Solutions

[**Cloud Storage for Firebase**](https://firebase.google.com/products/storage/): Provides direct access and easy integration with Cloud Storage via the Firebase mobile SDK for your iOS, Android, and web apps. The Firebase SDK handles security via Firebase Authentication and can perform efficiently even in poor network quality. Uploads and downloads can restart and resume from where they stop to save time and bandwidth. Files uploaded via the Firebase SDK can also be accessed from Google Cloud Storage.

[**Cloud Firestore**](https://firebase.google.com/products/firestore/): NoSQL database which stores data as document objects similar to Cloud Datastore, but provides powerful native mobile SDKs so that your iOS, Android, and web apps can access directly. Data is also cached locally to allow offline use and is synchronized to Cloud Firestore when the device comes online. Cloud Firestore has built-in security for mobile access via Firebase Authentication and Cloud Firestore Security Rules for iOS and Android.

![Image of GCP storage](https://github.com/lliquidvinall/gcp/images/GCP_storage.jpeg)

