---
layout: exam
---

# Practice Exam 1

1. A developer is instructed to configure a worker daemon to queue messages based on a specific schedule using a worker environment hosted in Elastic Beanstalk. Periodic tasks should be defined to automatically add jobs to your worker environment’s queue at regular intervals. Which configuration file should the developer add to the source bundle to meet the above requirement?
    
   - A. env.yaml
   - B. cron.yaml
   - C. appspec.yml
   - D. Dockerrun.aws.json	

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B
    </details>


2. A mobile game has a serverless backend consisting of an API Gateway backed by Lambda functions and a DynamoDB table in provisioned capacity mode, where player data is stored. While the game has maintained a consistent level of traffic, recent growth in the player base has caused response times to slow down. To improve performance, the developer wants to reduce the number of database queries for data that rarely change. What approach can the developer take to achieve this goal cost-effectively and with less development overhead?

    - A. Create an Amazon MemoryDB for Redis database in front of the DynamoDB table to cache data.
    - B. Use DynamoDB Session Handler to handle the saving and retrieval of player data.
    - C. Switch the DynamoDB table’s capacity mode to On-demand.
    - D. Set up an Amazon DynamoDB Accelerator (DAX) caching layer in front of the DynamoDB table.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>


3. A developer is managing a distributed system that consists of an Application Load Balancer, an SQS queue, and an Auto Scaling group of EC2 instances. The system has been integrated with CloudFront to better serve clients worldwide. To enhance the security of the in-flight data, the developer was instructed to establish an end-to-end SSL connection between the origin and the end-users. Which TWO options will allow the developer to meet this requirement using CloudFront? (Select TWO.)

    - A. Configure your ALB to only allow traffic on port 443 using an SSL certificate from AWS Config.
    - B. Configure the Origin Protocol Policy to use HTTPS only
    - C. Configure the Viewer Protocol Policy to use HTTPS only
    - D. Set up an Origin Access Control (OAC) setting
    - E. Associate a Web ACL using AWS Web Application Firewall (WAF) with your CloudFront Distribution.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B, C. 
    </details>

4. A serverless application composed of Lambda, API Gateway, and DynamoDB has been running without issues for quite some time. As part of the IT compliance of the company, a developer was instructed to ensure that all of the new changes made to the items in DynamoDB are recorded and stored in another DynamoDB table in another region. In this scenario, which of the following is the MOST ideal way to comply with the requirements?

    - A. Enable DynamoDB Streams and configure a Lambda function to process and save new changes to the other table.
    - B. Enable DynamoDB Point-in-Time Recovery to automatically sync the two tables.
    - C. Set up DynamoDB Accelerator
    - D. Create an Amazon EventBridge (Amazon CloudWatch Events) rule that tracks table-level events in DynamoDB. Set a Lambda function as a rule target to process and save new changes to the other table.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

5. A recently deployed Lambda function has an intermittent issue in processing customer data. You enabled the active tracing option in order to detect, analyze, and optimize performance issues of your function using the X-Ray service. Which of the following environment variables are used by AWS Lambda to facilitate communication with X-Ray? (Select TWO.)

    - A. AWS_XRAY_DEBUG_MODE	
    - B. AWS_XRAY_TRACING_NAME	
    - C. _X_AMZN_TRACE_ID	
    - D. AWS_XRAY_CONTEXT_MISSING	
    - E. AUTO_INSTRUMENT	

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C, D. 
    </details>

6. Your serverless AWS Lambda functions are integrated with Amazon API gateway using Lambda proxy integration. The API caching feature is enabled in the API Gateway with a TTL value of 300 seconds. A client would like to fetch the latest data from your endpoints every time a request is sent and invalidate the existing cache. What should the client do in order to get the latest data?

    - A. Modify cache TTL value to a shorter period.
    - B. Have the client send a request with the Cache-Control: max-age=0 header.	
    - C. Have the client send a request with the Cached: false header.	
    - D. Override API caching by allowing the client to send requests to the endpoint directly.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

7. A developer is planning to deploy a high-performance online trading application which requires a database that can scale globally and can handle frequent schema changes. The database should also support flexible schemas that enable faster and more iterative development. Which is the MOST suitable database service that you should use to achieve this requirement?

    - A. Amazon RDS
    - B. Amazon Aurora
    - C. Amazon DynamoDB
    - D. Amazon Redshift

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>



