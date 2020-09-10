# Python_Microservices
## Requirements
We are going to build a microservice to index rooms information coming from another service (crawler). This service will be responsible for indexing the information into Elasticsearch.

The indexing will be a process of:

Validate and sanitize the data
Get some metadata from the room information like geolocalization
Upload the given images URL to Amazon S3
Send an event to RabbitMQ every time a new room has been indexed serializing the payload with Avro.
Endpoints:
