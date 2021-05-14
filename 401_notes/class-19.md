# Class 19

**Resources:**

- [Amazon DynamoDB](https://www.trustradius.com/products/amazon-dynamodb/reviews?qs=pros-and-cons)
- [AWS SQS FIFO Complete Guide: What is it and When to use it](https://www.learnaws.org/2020/12/21/aws-sqs-fifo-deep-dive/#:~:text=A%20standard%20queue%20tries%20to,and%20received%20in%20strict%20order.)
- [What is Serverless Architecture? What are its Pros and Cons?](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)
- [Invoking AWS Lambda functions](https://docs.aws.amazon.com/lambda/latest/dg/lambda-invocation.html)
- [DynamoDB vs MongoDB](https://www.xplenty.com/blog/dynamodb-vs-mongodb-differences/#:~:text=DynamoDB%20is%20a%20fully%20managed,fully%20managed%20with%20MongoDB%20Atlas.&text=DynamoDB%20uses%20tables%2C%20items%20and,and%20has%20fewer%20size%20restrictions.)

## Review, Research, and Discussion

1. Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
    - API Gateway creates RESTful APIs, Lambda functions take care of CRUD actions and this is all happenning in the cloud. All the same we did building ExpressJS Server from scratch.

2. List the AWS Database offerings and talk about the pros and cons of each
    - Aurora, Relational Database Service, RDS on VMware, ElastCache, Neptune, Quantum Ledger Database, DynamoDB, Timestream, DocumentDB
    - **PROS DynamoDB**
      - Great performance even with large scale applications.
      - We don't need to manage any backend servers, everything is a one-click solution in their dashboard.
      - Support great reliability and scalability while supporting ACID transactions.
    - **CONS DynamoDB**
      - The costs can be huge if the resource is not monitored properly. We had to crank it down during off-peak hours and again increase the throughput during high usage intervals.
      - While the time of usage, DynomoDB did not support different region backup. The backups were only within the same region.
      - Best suited for key-value type of operations only. Won't work particularly great for relational operations.

3. What’s the difference between a FIFO and a standard queue?

  - A **standard queue** tries to preserve the order of messages (best-effort), but there is a possibility of a message being delivered out of order. In a **FIFO queue**, messages are grouped into “Message groups” and all messages within a message group are sent and received in strict order.

4. How can the server be assured a message was properly received?
    - `res.status(200)`

## Vocabulary Terms

1. Serverless API
    - Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. 
2. Triggers
    - A trigger is a Lambda resource or a resource in another service that developer configures to invoke function in response to lifecycle events, external requests, or on a schedule.
3. Dynamo vs Mongo
    - MongoDB is vendor agnostic, Open Source, and can be deployed anywhere. DynamoDB is only available on AWS.
    - DynamoDB is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas.
    - DynamoDB as an integrated AWS service makes it easier to develop end to end solutions.
    - DynamoDB uses tables, items and attributes, MongoDB uses JSON-like documents.
    - DynamoDB supports limited data types and smaller item sizes; MongoDB supports more data types and has fewer size restrictions.
4. Dynamoose vs Mongoose
    - Dynamoose is a modeling tool for Amazon's DynamoDB (inspired by Mongoose).Dynobase helps to accelerate DynamoDB workflow with code generation.