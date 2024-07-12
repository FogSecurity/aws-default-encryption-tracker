# aws-encryption-tracker
Tracker for Encryption by Default (At Rest) for AWS Resources

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
| Secret | Secrets Mnaager | Yes | AWS Managed |
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








Contact info@fogsecurity.io for help and feedback.
