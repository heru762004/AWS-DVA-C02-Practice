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

