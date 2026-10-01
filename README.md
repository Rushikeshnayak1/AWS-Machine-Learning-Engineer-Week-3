# AWS Machine Learning Engineer – Associate | Week 3

## Biweekly Learning Artifact (BLA)

**Student:** Rushikesh Nayak  
**Instructor:** Dr. Victor Govindaswamy  
**Learning Path:** AWS Certification Path  
**Certification:** AWS Machine Learning Engineer – Associate  

---

## About This BLA

This repository contains my Week 3 learning work for the AWS Machine Learning Engineer – Associate certification path.

During this week, I continued learning about AWS storage services and moved into event-driven processing, S3 performance optimization, file systems, and real-time streaming data.

I divided my learning into three presentations so I could understand each group of topics separately and explain them in a simple way.

---

## Part 1 – Amazon S3 Storage Classes, Replication & Lifecycle Management

In the first presentation, I focused on how Amazon S3 stores, protects, copies, archives, and manages data over time.

### Topics I Learned

- Amazon S3 Replication
- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)
- S3 replication rules
- S3 Storage Classes
- S3 Standard
- Standard-IA
- One Zone-IA
- Glacier storage classes
- Durability vs. Availability
- S3 Lifecycle Rules
- Transition and expiration actions
- Recovering deleted objects with versioning
- S3 Analytics – Storage Class Analysis

One important thing I learned is that choosing an S3 storage option depends on the requirement. I need to think about how frequently the data is accessed, how quickly it needs to be retrieved, how long it needs to remain available, and the cost.

---

## Part 2 – S3 Event Notifications & Performance Optimization

The second presentation helped me understand that Amazon S3 is more than just a place to store files. S3 can also become part of an automated workflow when something happens to an object.

### Topics I Learned

- S3 Event Notifications
- ObjectCreated events
- ObjectRemoved events
- ObjectRestore events
- Object-name filtering
- AWS Lambda as an event destination
- Amazon SQS
- Amazon SNS
- IAM permissions for event destinations
- Amazon EventBridge
- S3 request performance
- S3 prefixes
- Multipart Upload
- S3 Transfer Acceleration
- Byte-Range Fetches

### Example Workflow

A simple ML image-processing workflow I studied was:

New Image Upload  
→ Amazon S3  
→ ObjectCreated Event  
→ AWS Lambda  
→ Amazon SQS  
→ ML Processing

This example helped me understand how different AWS services can work together automatically when new data arrives.

---

## Part 3 – Amazon FSx & Amazon Kinesis

In the third presentation, I continued with AWS storage concepts and then started learning about real-time streaming data.

### Amazon FSx Topics

- FSx for Lustre
- Scratch file systems
- Persistent file systems
- FSx for NetApp ONTAP
- FSx for OpenZFS

I learned that FSx for Lustre Scratch is useful for temporary and high-performance processing, while Persistent is designed for longer-term workloads where file-system data needs to remain available.

### Amazon Kinesis Topics

- Amazon Kinesis Data Streams
- Producers and consumers
- Streaming records
- Data retention and replay
- Partitioning and ordering
- Provisioned capacity
- On-Demand capacity
- Amazon Data Firehose
- Data Streams vs. Data Firehose
- Kinesis troubleshooting

I also learned that Kinesis Data Streams and Data Firehose solve different problems.

**Kinesis Data Streams:** useful when applications need consumers, processing, retention, or replay.

**Amazon Data Firehose:** useful when streaming data needs managed delivery to destinations such as Amazon S3, Amazon Redshift, or Amazon OpenSearch Service.

---

## AWS Services and Technologies Covered

- Amazon S3
- S3 Replication
- S3 Lifecycle Management
- S3 Analytics
- AWS Lambda
- Amazon SQS
- Amazon SNS
- Amazon EventBridge
- Amazon FSx for Lustre
- Amazon FSx for NetApp ONTAP
- Amazon FSx for OpenZFS
- Amazon Kinesis Data Streams
- Amazon Data Firehose
- AWS KMS

---

## Major Steps Completed

1. Studied the Week 3 AWS certification topics.
2. Organized the topics into three separate presentations.
3. Reviewed important AWS concepts and use cases.
4. Connected the AWS services with Machine Learning examples.
5. Created presentation slides for each topic.
6. Recorded three explanation videos.
7. Published the videos on YouTube.
8. Organized the supporting learning materials in GitHub.
9. Documented my learning and key takeaways in this repository.

---

## Troubleshooting and Challenges

Some topics required more attention because several AWS services can appear similar at first.

One area I focused on was understanding when to use different S3 performance features. Multipart Upload is useful for large-file uploads, while Transfer Acceleration focuses on long-distance transfers, and Byte-Range Fetches can help with parallel or partial downloads.

I also spent time understanding the difference between Kinesis Data Streams and Data Firehose. Comparing their purposes helped me remember that Data Streams focuses more on streaming applications, consumers, retention, and replay, while Firehose focuses on managed delivery.

---

## Results

After completing these topics, I have a better understanding of how AWS can:

- Store and manage data using different S3 storage options.
- Replicate and protect S3 objects.
- Automatically manage older data with lifecycle rules.
- Start workflows when new objects arrive in S3.
- Improve large-file upload and download performance.
- Provide managed file-system options through Amazon FSx.
- Process continuously arriving data using Amazon Kinesis.
- Deliver streaming data to AWS destinations using Data Firehose.

---

## What I Learned

The biggest lesson from Week 3 was that choosing an AWS service should start with understanding the requirement.

Instead of only memorizing service names, I am trying to understand what problem each service solves.

For example:

- Need another copy of S3 data → Replication
- Need automatic movement of older data → Lifecycle Rules
- Need processing after a new S3 object arrives → Event Notification
- Need to upload a very large file → Multipart Upload
- Need long-distance S3 transfer → Transfer Acceleration
- Need real-time streaming with consumers and replay → Kinesis Data Streams
- Need managed streaming delivery → Data Firehose

---

## Reflection

This week helped me connect storage, automation, performance, and streaming concepts together.

At first, some services looked similar because they all work with data, but after studying their individual purposes and examples, the differences became clearer.

Creating the presentations and explaining the topics in my own words also helped me review the concepts instead of only reading them.

I will continue practicing these AWS services and focus on understanding scenario-based questions for the AWS Machine Learning Engineer – Associate certification.

---

## YouTube Videos

### Video 1
**Amazon S3 Storage Classes, Replication & Lifecycle Management**

YouTube: https://youtu.be/sj8M8WMFbiQ?si=3wDrBDQvUEZs-sXo

### Video 2
**Amazon S3 Event Notifications & Performance Optimization**

YouTube: https://youtu.be/DTPTJtdROnc?si=S3eqCtBzddmJYlcW

### Video 3
**FSx Deployment Options & Amazon Kinesis**

YouTube: https://youtu.be/ELWF_vGvlR4?si=s1xqgotikA38bE2w

---

## LinkedIn Posts

LinkedIn posts will be added after publication.

- Part 1: https://lnkd.in/p/grq_Xcj9
- Part 2: [ADD LINKEDIN LINK]
- Part 3: [ADD LINKEDIN LINK]

---

## Presentation Materials

The presentation materials for all three parts are included in this repository.

1. S3 Storage Classes, Replication & Lifecycle Management
2. S3 Event Notifications & Performance Optimization
3. FSx Deployment Options & Amazon Kinesis

---

## References and Learning Resources

- AWS Machine Learning Engineer – Associate certification study materials
- AWS learning materials used during Week 3
- Course materials and instructor guidance

---

## Acknowledgment

Special thanks to **Dr. Victor Govindaswamy** for his guidance and support throughout this learning process.

---

**Presented by Rushikesh Nayak**
