# AWS Machine Learning Engineer – Week 3 Study Notes

## Overview

During Week 3, I continued studying for the AWS Machine Learning Engineer – Associate certification. My main focus was Amazon S3 data management and performance, Amazon FSx, and Amazon Kinesis.

---

## Amazon S3 Replication

I learned that S3 Replication can automatically copy eligible objects from one bucket to another.

### Cross-Region Replication (CRR)
- Copies objects to a bucket in another AWS Region.
- Can be useful for disaster recovery, compliance, and regional access.

### Same-Region Replication (SRR)
- Copies objects to another bucket in the same AWS Region.
- Can be useful for log aggregation, account separation, and organizational requirements.

Versioning must be enabled on both the source and destination buckets.

---

## S3 Storage Classes

I studied different storage classes and when they can be useful.

- **S3 Standard** – frequently accessed data.
- **Standard-IA** – infrequently accessed data that still requires rapid access.
- **One Zone-IA** – lower-cost option for infrequently accessed and recreatable data.
- **Glacier Instant Retrieval** – archive data that still requires fast retrieval.
- **Glacier Flexible Retrieval** – archival storage with flexible retrieval.
- **Glacier Deep Archive** – very rarely accessed long-term data.

I learned that the storage class should be selected based on access frequency, retrieval requirements, availability needs, and cost.

---

## S3 Lifecycle Management

Lifecycle rules can automatically manage objects as they become older.

For example:

S3 Standard → Standard-IA → Glacier

Lifecycle rules can also expire objects, remove old versions, and delete incomplete multipart uploads.

---

## S3 Event Notifications

Amazon S3 can generate events when something happens to an object.

Examples include:

- ObjectCreated
- ObjectRemoved
- ObjectRestore
- Replication-related events

These events can be sent to services such as:

- AWS Lambda
- Amazon SQS
- Amazon SNS

Amazon EventBridge can provide more advanced event filtering and routing.

---

## S3 Performance

I learned that Amazon S3 automatically scales to high request rates.

Performance can scale across multiple prefixes.

I also studied three important techniques for large objects:

### Multipart Upload
Divides a large file into smaller parts that can be uploaded independently and in parallel.

### S3 Transfer Acceleration
Can improve transfers over long geographic distances by using AWS edge locations and the AWS network.

### Byte-Range Fetches
Allows an application to retrieve only specific sections of an object or download multiple ranges in parallel.

---

## Amazon FSx

I studied several Amazon FSx options.

### FSx for Lustre

**Scratch**
- Temporary storage.
- Designed for short-term processing and high burst performance.

**Persistent**
- Designed for longer-term processing.
- Data is replicated within the same Availability Zone.

I also reviewed:

- FSx for NetApp ONTAP
- FSx for OpenZFS

---

## Amazon Kinesis Data Streams

Kinesis Data Streams can collect continuously arriving data in real time.

Examples include:

- Application events
- Logs
- IoT data
- Click streams
- Metrics

The basic workflow is:

Producer → Kinesis Data Stream → Consumer

I also learned about Provisioned and On-Demand capacity modes.

---

## Kinesis Data Streams vs. Data Firehose

### Kinesis Data Streams

Useful when an application needs:

- Consumers
- Real-time processing
- Data retention
- Replay

### Amazon Data Firehose

Useful when streaming data needs managed delivery to destinations such as:

- Amazon S3
- Amazon Redshift
- Amazon OpenSearch Service
- HTTP endpoints

A simple way I remember the difference is:

**Data Streams = process, consume, retain, and replay**

**Data Firehose = managed delivery**

---

## Troubleshooting Notes

For Kinesis producer problems, I learned to check:

- Throughput limits
- Throttling
- Partition-key distribution
- Hot shards
- Retry behavior

For consumer problems, I learned to check:

- Shard capacity
- Consumer lag
- CPU and memory
- Application processing speed
- Lambda permissions and throttling

---

## Week 3 Takeaway

My biggest takeaway from Week 3 is that AWS questions often describe a requirement instead of directly giving the service name.

I am trying to understand why each AWS service or feature is used instead of only memorizing its name.
