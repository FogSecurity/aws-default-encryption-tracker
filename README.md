# Secure By Default: Encrypted by Default in AWS Tracker

Fog Security: https://www.fogsecurity.io/ \
Accompanying Blog Post: www.fogsecurity.io/blog/are-my-aws-resources-encrypted-or-unencrypted-by-default 

Contact info@fogsecurity.io for help and feedback.  Please feel free to submit additions or feedback here as well.

The following is a tracker for Encryption by Default (At Rest) for AWS Resources.  We researched 51 types of resources across 43 AWS services including compute, database, storage, AI and machine learning, management and governance.  These include EC2, Sagemaker, DynamoDB, S3, Secrets Manager, CloudWatch, RDS, and more.

Not all AWS Resources are default encrypted at rest.  

- Encryption can offer an additional layer of access control and security.
- Not all encryption mechanisms in AWS [are created equally in KMS](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#kms_keys).  AWS Managed Keys, AWS Customer Managed Keys, AWS Owned Keys all have different access implications.
- AWS Managed Keys are used only for your AWS Account.  AWS Owned Keys are used in multiple AWS Accounts (can be across many customers).
- Depending on your organization's security and compliance guardrails, certain encryption mechanisms or resources must be encrypted.  Check with your organization's security best practices and ensure compliance requirements such as HIPPA, PCI, GDPR, and more are met.
- We recommend checking resources and their encryption status for security and compliance.
- We also recommend where possible, to encrypt all resources by default.

More research on cloud encryption management to come. 

## Total Numbers (As of July 2024)

Encrypted by Default: 39 (76.47%) \
Unencrypted by Default: 12 (23.53%) \
Default AWS Owned: 22 \
Default AWS Managed: 17 \
AWS Services Covered: 43 \
Total Resources: 51

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
| Replication Instance | Data Migration Service (DMS) | Yes | AWS Managed |
| Kinesis Video Stream | Kinesis Video | Yes | AWS Managed |
| File System | FSx | Yes | AWS Managed | 
| AppFlow Flow | AppFlow | Yes | AWS Owned |
| DAX Cluster | DynamoDB Accelerator (DAX) | Yes | AWS Managed |
| CodeArtifact Domain | CodeArtifact | Yes | AWS Managed |
| CodeCommit Repository | CodeCommit | Yes | AWS Managed |
| HealthLake DataStore | HealthLake | Yes | AWS Owned |
| MWAA Environment | Managed WorkFlows for Apache Airflow (MWAA) | Yes | AWS Owned |
| EMR Serverless Application Managed Logs | EMR Serverless | Yes | AWS Owned |
| Amazon Q Business Application | Amazon Q | Yes | AWS Owned |

## Methodology

To validate the above resources, the following methods and process were used:
- Many resources were created with the [AWS CLI](https://awscli.amazonaws.com/v2/documentation/api/latest/index.html).
- Default encryption and encryption type were validated with the [AWS CLI](https://awscli.amazonaws.com/v2/documentation/api/latest/index.html) Describe/Get calls.
- Additional validation of default encryption was performed via the AWS Console.
- CLI Documentation and [AWS Documentation](https://docs.aws.amazon.com/) was referenced to validate default encryption and encryption type as well. 

Note: Encryption results may be misleading.  See [our Quantum Ledger Database (QLDB) research here](https://www.fogsecurity.io/blog/encryption-state-of-amazon-qldb) for an example of misleading reporting on encryption status.

Contact info@fogsecurity.io for help and feedback.
