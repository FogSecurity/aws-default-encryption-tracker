# Secure By Default: Encrypted by Default in AWS Tracker

Fog Security: https://www.fogsecurity.io/ \
Accompanying Blog Post: 

Contact info@fogsecurity.io for help and feedback.  Please feel free to submit additions or feedback here as well.

The following is a tracker for Encryption by Default (At Rest) for AWS Resources.  We researched 47 types of resources across 39 AWS services including compute, database, storage, machine learning, management and governance.  These include EC2, Sagemaker, DynamoDB, S3, Secrets Manager, CloudWatch, RDS, and more.


## Total Numbers (As of July 2024)

Encrypted by Default: 35 \
Unencrypted by Default: 12 \
Default AWS Owned: 18 \
Default AWS Managed: 17 \
Total Resources: 47 

## AWS Resource Encrypted by Default Table

| AWS Resource  | AWS Service | Encrypted by Default (API/CLI) | Default Encryption Type | 
| ------------- | ----------- | ------------- | ------------------ |
| S3 Bucket  | Simple Storage Service (S3) | Yes | AWS Owned | 
| DynamoDB Table  | DynamoDB  |	Yes | AWS Owned |
| RDS Database Instance | RDS | Yes | AWS Managed |
| EFS File System | EFS | Yes | AWS Managed |
| Redshift Cluster | Redshift | No | - |
| Aurora Instance | Aurora | Yes | AWS Managed |
| Redis Cache | ElastiCache | Yes | AWS Owned |
| Memcached Cache | ElastiCache | Yes | AWS Owned |
| Global Datastore (Cluster) | Elasticache | No | - |
| Keyspaces Table | Keyspaces (Cassandra) | Yes | AWS Owned |
| MemoryDB Database | MemoryDB for Redis | Yes | AWS Owned |
| Neptune Instance | Neptune | Yes | AWS Managed |
| QLDB Ledger | Quantum Ledger Database (QLDB) | Yes | AWS Owned | 
| LiveAnalytics Database | Timestream | Yes | AWS Managed |
| Lightsail Managed DB | Lightsail | Yes | AWS Managed |
| Secret | Secrets Manager | Yes | AWS Managed |
| SecureString Parameter | Systems Manager Parameter Store | Yes | AWS Managed |
| String Parameter | Systems Manager Parameter Store | No | - |
| StringList Parameter | Systems Manager Parameter Store | No | - |
| EBS Volume | Elastic Block Store (EBS) | No | - |
| Lambda Envrionment Variables | Lambda | Yes | AWS Managed |
| Location Trackers | Location Service | Yes | AWS Owned |
| Location Geofence Collection | Location Service | Yes | AWS Owned |
| SQS Queue | Simple Queue Service (SQS) | Yes | AWS Owned | 
| SNS Topic | Simple Notification Service (SNS) | No | - |
| CloudWatch Log Group | CloudWatch | No | - |
| Prometheus Workgroup | Prometheus | Yes | AWS Owned |
| Glue Data Catalog Connection Passwords | Glue | No | - |
| Glue Data Catalog Metadata | Glue | No | - | 
| Firehose Stream | Kinesis | No | - |
| MSK Cluster | Managed Streaming for Apache Kafka (MSK) | Yes | AWS Managed |
| SageMaker Notebook Instance | SageMaker | Yes | AWS Owned |
| Comprehend Analysis Job | Comprehend | No | - |
| Traces | X-Ray | Yes | AWS Managed | 
| OpenSearch Domain | OpenSearch | No | - |
| OpenSearch Collection | OpenSearch | Yes | AWS Owned |
| ActiveMQ Broker | MQ | Yes | AWS Owned | 
| RabbitMQ Broker | MQ | Yes | AWS Owned |
| Kendra Index | Kendra | Yes | AWS Owned | 
| ECR Repository | ECR | Yes | AWS Owned | 
| Replication Instance | DMS | Yes | AWS Managed |
| Kinesis Video Stream | Kinesis Video | Yes | AWS Managed |
| File System | FSx | Yes | AWS Managed | 
| AppFlow Flow | AppFlow | Yes | AWS Owned |
| DAX Cluster | DynamoDB Accelerator (DAX) | Yes | AWS Managed |
| CodeArtifact Domain | CodeArtifact | Yes | AWS Managed |
| CodeCommit Repository | CodeCommit | Yes | AWS Managed |

## Methodology

For the resources above, most were created with the (AWS CLI)[https://awscli.amazonaws.com/v2/documentation/api/latest/index.html].  CLI Documentation and (AWS Documentation)[https://docs.aws.amazon.com/] was referenced to validate default encryption, encryption types as well.  

Contact info@fogsecurity.io for help and feedback.

