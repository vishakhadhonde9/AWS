# AWS Kinesis-
- Amazon Kinesis is a fully managed, scalable, and real-time cloud service for collecting, processing, and analyzing streaming data.
- It provides capabilities to collect, process, and analyze large streams of data, enabling real-time insights and applications.

# Services in the Kinesis Family:
- The Kinesis suite is composed of four main services, each designed for a specific part of the streaming data workflow::

## 1]Kinesis Data Streams (KDS)-
- Collects and stores real-time data streams.
- Data is divided into shards (like parallel pipelines).
- Producers (e.g., web servers, IoT devices, mobile apps) write data records into a Kinesis Data Stream. These records are stored shards (the base throughput units of a stream) for a default of 24 hours (configurable up to 365 days).
- Consumers (e.g., EC2 instances, Lambda functions, Kinesis Data Firehose) can then read and process these records in real-time.
- Provides multiple consumers to process the same data simultaneously.

## 2]Kinesis Data Firehose-
- This is the simplest way to load streaming data into data stores and analytics tools. It is a fully managed service that requires no ongoing administration.
- Delivers streaming data to destinations like S3, Redshift, Elasticsearch, Splunk.
- No need to manage servers, it auto-scales.

## 3]Kinesis Data Analytics-
- Lets you run SQL queries on real-time streaming data.
- This service allows you to process and analyze streaming data with standard SQL or Apache Flink.
- 
## 4]Kinesis Video Streams-
- This service is specifically designed to ingest and process streaming video and audio data from millions of devices like security cameras, smartphone live streams, and body cams.
- Streams and stores video/audio from devices (like CCTV cameras, IoT devices).
