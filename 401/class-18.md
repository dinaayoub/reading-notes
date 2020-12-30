# Class 18 - Read: AWS: API, Dynamo and Lambda

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?AWS FIFO Queues are for items that are processed only once whereas standard queues can have items processed more than once. [src](https://aws.amazon.com/about-aws/whats-new/2016/11/
2. How can the server be assured a message was properly received? When it receives an acknowledgement event from the client.
3. What classic design pattern is best represented by event driven programming? Singleton?
4. How do you test an event driven system? by testing all the functions in it. Manually you can trigger the events instead.

## Vocabulary Terms

* Serverless Functions: a function that can run on its own on something like AWS lambda - it can be run without setting up an entire server in the cloud.
* Cloud Storage: allows you to store data in the cloud, such as S3 buckets, or mongo db clusters from atlas (?) without having to run a local server with storage.
* CDN: content delivery networks that can host and deliver static content to clients (such as css, html, images) faster than the server can as they are located geographically closer to the client.

## Preparation Materials

[AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway)
[AWS API Gateway](https://aws.amazon.com/api-gateway/)
[AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)
[AWS DynamoDB](https://aws.amazon.com/dynamodb/)
[Dynamoose](https://dynamoosejs.com/getting_started/Introduction)
