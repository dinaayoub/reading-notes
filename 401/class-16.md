# Read: Class 16 - AWS: Cloud Servers

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue? a standard queue works first in first out (FIFO) so they are one and the same. However if you're asking about the AWS FIFO Queues - those are for items that are processed only once. [src](https://aws.amazon.com/about-aws/whats-new/2016/11/amazon-sqs-introduces-fifo-queues-with-exactly-once-processing-and-lower-prices-for-standard-queues/#:~:text=FIFO%20queues%20have%20essentially%20the,being%20received%20by%20message%20consumers.)
2. How can the server be assured a message was properly received? When the client emits a received event for that particular message.
3. What classic design pattern is best represented by event driven programming? I still don't know the answer to this. Is it singleton?
4. How do you test an event driven system? test the functions that are called, which is better than testing the events since that would require running a server.

## Vocabulary Terms

* Server: computer or software that serves up information to clients
* Pub/Sub: an async messaging service that decouples services that produce events from services that process events. (repeated from class 14 notes) [src](https://cloud.google.com/pubsub/docs/overview)
* WRRC: web request response cycle which describes how communication from a web client to a server works.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
3. What are you most excited about trying to implement or see how it works?

## Preparation Materials

[Virtual Machines (Bookmark This)](https://www.youtube.com/watch?v=yIVXjl4SwVo&ab_channel=VictorDozal)
[VMS and the Cloud (Bookmark This)](https://www.youtube.com/watch?v=l0DfHUWMjsU&ab_channel=DavidBecker)
[AWS EC2](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc)
[EC2 For Humans](https://www.youtube.com/watch?v=lZMkgOMYYIg&ab_channel=Academind)
[Elastic Beanstalk](https://www.youtube.com/watch?v=SrwxAScdyT0&ab_channel=AmazonWebServices)