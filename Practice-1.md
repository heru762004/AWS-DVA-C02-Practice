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
    Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second. DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables without requiring developers to manage cache invalidation, data population, or cluster management.
This will enable you to focus on building great applications for your customers without worrying about performance at scale. You do not need to modify application logic since DAX is compatible with existing DynamoDB API calls. You can enable DAX with just a few clicks in the AWS Management Console or using the AWS SDK. Just as with DynamoDB, you only pay for the capacity you provision.
</details>



