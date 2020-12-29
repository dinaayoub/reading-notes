# Read: Class 17 - AWS: S3 and Lambda

## Review, Research, and Discussion

(note: since a lot of these are repeated questions, i'm answering them from my previous days' readings.)

1. What’s the difference between a FIFO and a standard queue? a standard queue works first in first out (FIFO) so they are one and the same. However if you're asking about the AWS FIFO Queues - those are for items that are processed only once. [src](https://aws.amazon.com/about-aws/whats-new/2016/11/amazon-sqs-introduces-fifo-queues-with-exactly-once-processing-and-lower-prices-for-standard-queues/#:~:text=FIFO%20queues%20have%20essentially%20the,being%20received%20by%20message%20consumers.)
2. How can the server be assured a message was properly received?  When the client emits a received event for that particular message.
3. What classic design pattern is best represented by event driven programming? I think it's Singleton, but not sure.
4. How do you test an event driven system? In Automation: by testing all the functions, Manually: by emitting the events

## Vocabulary Terms

* Server Instances: a collection of sql server databases run by a solitary sql server service / instance [src](https://www.techopedia.com/definition/32149/server-instance#:~:text=A%20server%20instance%20is%20a,based%20or%20command%2Dline%20based.)
* Containers: a form of OS virtualization. A single container can be used to run a small process or a whole app. [src](https://www.netapp.com/devops-solutions/what-are-containers/#:~:text=Containers%20are%20a%20form%20of,%2C%20libraries%2C%20and%20configuration%20files.)
* Cloud Services: all of the services offered by cloud providers such as AWS and Azure. Can be computing, storage, ...etc. [src](https://www.citrix.com/glossary/what-is-a-cloud-service.html)
* Cloud Architecture: how individual technologies are integrated to create clouds. [src](https://www.redhat.com/en/topics/cloud-computing/what-is-cloud-architecture)
* AWS: Amazon Web Services
* EC2/Beanstalk vs Heroku: They're both ways to deploy your website and both use AWS, but Elastic Beanstalk has a lot more functionality.

## Preview

* Which 3 things had you heard about previously and now have better clarity on? how to deploy on azure
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo? i look forward to actually understanding what i'm doing :) at this point i'm still very shaky on the deployment capabilities.
* What are you most excited about trying to implement or see how it works? Azure!

## Preparation Materials

[AWS S3](https://aws.amazon.com/s3/)
[AWS Lambda Basics](https://www.serverless.com/aws-lambda)
[AWS Lambda Functions](https://aws.amazon.com/lambda/)
[CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)