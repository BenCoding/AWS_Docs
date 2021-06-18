# Messaging & Events

## Options

| Element                   | Description                                | Azure Equivalent    |
| ------------------------- | ------------------------------------------ | ------------------- |
| 1. SQS Standard           | Standard Queue (may duplicate)             | Service Bus         |
| 2. SQS FIFO               | 1x processed per msg (First in, First Out) | Queue Storage (ASQ) |
| 3. Kinesis Data Streams   | Persistence & Durability                   |                     |
| 4. MQ                     |                                            |                     |
| 5. SNS                    | Notifications                              | Azure Notifications |
| 6. Amazon EventBridge     | Formerly CloudWatch ChronJob               | Event Grid          |
| 7. SES                    |                                            |                     |
| 8. Kinesis Data Firehose  | Persistence & Durability                   |                     |
| 9. Kinesis Data Analytics | Persistence & Durability                   |                     |
| 10. DynamoDB Streams      | Slam Dunk                                  |                     |

## How to decide?

abc

## Architecture Patterns

| Element                    | Notes                   | Use Case                             |
| -------------------------- | ----------------------- | ------------------------------------ |
| Fan-out, message-filtering | Async,Too much time     | Submit a ride completion             |
| Topic-queue-chaining       | queues as buffering LBs | Submit a ride completion             |
| Scatter-Gather             |                         | Instant ride RFQ (request for quote) |
| Saga orchestration         |                         | Fare collection                      |
