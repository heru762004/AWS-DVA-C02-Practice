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

8. An application, which already uses X-Ray, generates thousands of trace data every hour. The developer wants to use a filter expression that will limit the results based on custom attributes or keys that he specifies. How should the developer refactor the application in order to filter the results in the X-Ray console?

    - A. Create a new sampling rule based on the custom attributes.
    - B. Add the custom attributes as annotations in your segment document.
    - C. Add the custom attributes as metadata in your segment document.
    - D. Include the custom attributes as new segment fields in the segment document.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

9. You are building a distributed system using KMS where you need to encrypt data at a later time. An API must be called that returns only the encrypted copy of the data key which you will use for encryption. After an hour, you will decrypt the data key by calling the Decrypt API then using the returned plaintext data key to finally encrypt the data. Which is the MOST suitable KMS API that the system should use to securely implement the requirements described above?

    - A. GenerateRandom	
    - B. GenerateDataKeyWithoutPlaintext	
    - C. GenerateDataKey	
    - D. Encrypt	

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

10. A reporting application is hosted in AWS Elastic Beanstalk and uses Amazon DynamoDB as its database. If a user requests data, the application scans the entire table and returns the requested data. The table is expected to grow due to the surge of new users and the increase in requests for reports in the coming weeks. Which of the following should be done as a preparation to improve the application’s performance with minimal cost? (Select TWO.)

    - A. Set the ScanIndexForward parameter to control the order of query results.
    - B. Increase the Write Compute Unit (WCU) of the table
    - C. Use Query operations instead
    - D. Use DynamoDB Accelerator (DAX)
    - E. Reduce page size

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C, E. 
    </details>

11. An application performs various workflows and processes long-running tasks that take a long time to complete. Users are complaining that the application is unresponsive since the workflow substantially increases the time it takes to complete a user request. The development team is looking for a managed solution that can handle background tasks efficiently, scale automatically, and integrate seamlessly with the existing application deployed on Elastic Beanstalk. Which of the following is the BEST way to improve the performance of the application?

    - A. Spawn a worker process locally in the EC2 instances and process the tasks asynchronously.
    - B. Use a multicontainer docker environment in Elastic Beanstalk to process the long-running tasks asynchronously.
    - C. Use an Amazon ECS Cluster with a Fargate launch type to process the tasks asynchronously.
    - D. Use an Elastic Beanstalk worker environment to process the tasks asynchronously.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

12. A website is hosted in an Auto Scaling group of EC2 instances behind an Application Load Balancer. It also uses CloudFront with a default domain name to distribute its static assets and dynamic contents. However, the website has a poor search ranking as it doesn’t use a secure HTTPS/SSL on its site. Which are the possible solutions that the developer can implement in order to set up HTTPS communication between the viewers and CloudFront? (Select TWO.)

    - A. Set the Viewer Protocol Policy to use Redirect HTTP to HTTPS.
    - B. Use a self-signed certificate in the ALB.
    - C. Set the Viewer Protocol Policy to use HTTPS Only.
    - D. Use a self-signed SSL/TLS certificate in the ALB which is stored in a private S3 bucket.
    - E. Configure the ALB to use its default SSL/TLS certificate.

   <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A, C. 
    </details>

13. An application hosted in an Amazon ECS Cluster processes a large data stream and stores the result in a DynamoDB table. There is an urgent requirement to detect new entries in the table and automatically trigger a Lambda function to run some verification tests on the processed data. Which of the following options can satisfy the requirement with minimal configuration?

    - A. Run the Lambda function using SNS each time the ECS Cluster successfully processes financial data.
    - B. Set up an Amazon EventBridge (Amazon CloudWatch Events) rule to automatically trigger the Lambda function whenever a new entry is created in the DynamoDB table.
    - C. Detect the new entries in the DynamoDB table using AWS Copilot, then automatically invoke the Lambda function for processing.
    - D. Enable DynamoDB Streams to detect the new entries and automatically trigger the Lambda function.
   
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

14. A developer configured an Amazon API Gateway proxy integration named MyAPI to work with a Lambda function. However, when the API is being called, the developer receives a 502 Bad Gateway error. She tried invoking the underlying function, but it properly returned the result in XML format. What is the MOST likely root cause of this issue?

    - A. The endpoint request timed-out.
    - B. There has been an occasional out-of-order invocation due to heavy loads.
    - C. There is an incompatible output returned from a Lambda proxy integration backend.
    - D. The API name of the Amazon API Gateway proxy is invalid.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

15. A developer has recently completed a new version of a serverless application that is ready to be deployed using AWS SAM. There is a requirement that the traffic should shift from the previous Lambda function to the new version in the shortest time possible, but you still don’t want to shift traffic all-at-once immediately. Which deployment configuration is the MOST suitable one to use in this scenario?

    - A. CodeDeployDefault.LambdaLinear10PercentEvery1Minute
    - B. CodeDeployDefault.HalfAtATime
    - C. CodeDeployDefault.LambdaLinear10PercentEvery2Minutes
    - D. CodeDeployDefault.LambdaCanary10Percent5Minutes

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

16. A website hosted in AWS has a custom CloudWatch metric to track all HTTP server errors in the site every minute, which occurs intermittently. An existing CloudWatch Alarm has already been configured for this metric but you would like to re-configure this to properly monitor the application. The alarm should only be triggered when all three data points in the most recent three consecutive periods are above the threshold. Which of the following options is the MOST appropriate way to monitor the website based on the given threshold?

    - A. Set both the Period and Datapoints to Alarm to 3.
    - B. Set both the Evaluation Period and Datapoints to Alarm to 3.
    - C. Use high-resolution metrics.
    - D. Use metric math in CloudWatch to properly compute the threshold.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

17. A developer is creating an analytics REST API service that is powered by API Gateway. Analysts from a separate AWS account must interact with the service through an IAM role. The IAM role already has a policy that grants permission to invoke the API. What else should the developer do to meet the requirement without too much overhead?

    - A. Create a Lambda function authorizer for the API. In the Lambda function, write a logic that verifies the requester’s identity by extracting the information from the context object.
    - B. Set AWS_IAM as the method authorization type for the API. Attach a resource policy to the API that grants permission to the specified IAM role to invoke the execute-api:Invoke action.
    - C. Create an API Key for the API. Attach a resource policy to the API that grants permission to the specified IAM role to invoke the GetAPIKeys action.
    - D. Create a Cognito User Pool authorizer. Add the IAM role to the user pool. Authenticate the requester’s identity using Cognito. Ask the analysts to pass the token returned by Cognito in their request headers.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

18. An API gateway with a Lambda proxy integration takes a long time to complete its processing. There were also occurrences where some requests timed out. You want to monitor the responsiveness of your API calls as well as the underlying Lambda function. Which of the following CloudWatch metrics should you use to troubleshoot this issue? (Select TWO.)

    - A. IntegrationLatency
    - B. Latency
    - C. Count
    - D. CacheMissCount
    - E. CacheHitCount

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A, B. 
    </details>

19. A company selling smart security cameras uses an S3 bucket behind a CloudFront web distribution to store its static content, which it shares with customers worldwide. The company has recently released a new firmware update intended only for its premium customers, and unauthorized access should be denied with a user authentication process that has minimal latency. How can a developer refactor the current setup to achieve this requirement with the MOST efficient solution?

    - A. Use Lambda@Edge and Amazon Cognito to authenticate and authorize premium customers to download the firmware update.
    - B. Use the AWS Serverless Application Model (AWS SAM) and Amazon Cognito to authenticate the premium customers.
    - C. Restrict access to the S3 bucket only to premium customers using an Origin Access Control (OAC).
    - D. Use Signed URLs and Signed Cookies in CloudFront to distribute the firmware update file

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

20. You are developing a Lambda function which processes event notifications from Amazon S3. It is expected that the function will have:
    - 50 requests per second
    - 100 seconds to complete each request
    
    What should you do to prevent any issues when the function has been deployed and becomes operational?

    - A. Implement exponential backoff in your application.
    - B. Increase the concurrency limit of the function.
    - C. Request for AWS to increase the limit of your concurrent executions.
    - D. No additional action needed since Lambda will automatically scale based on the incoming requests.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

21. A mobile game is using a DynamoDB table named GameScore that keeps track of users and scores. Each item in the table is identified by a partition key (UserId) and a sort key (GameTitle). The diagram below shows how the items in the table are organized:
    <picture>
    <img src="https://td-portal-cdn.tutorialsdojo.com/wp-content/uploads/2019/12/cda1-59.png"></img>
    </picture>
    A developer wants to write a leaderboard application to display the top scores for each game. How can the developer meet the requirement in the MOST efficient manner?

    - A. Create a global secondary index. Assign the GameTitle attribute as the partition key and the TopScore attribute as the sort key.
    - B. Create a local secondary index. Assign the TopScore attribute as the partition key and the GameTitle attribute as the sort key.
    - C. Create a local secondary index. Assign the GameTitle attribute as the partition key and the TopScore attribute as the sort key.
    - D. Use the Scan operation and filter the results based on a GameTitle value.
   
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

22. You have several API Gateway APIs with Lambda Integration for each release life cycle of your application. There is a requirement to consolidate multiple releases into a single API Gateway for the ALPHA, BETA, RC (Release Candidate), and PROD releases. For example, their clients can connect to their ALPHA release by using the alpha.tutorialsdojo.com endpoint and beta release through the beta.tutorialsdojo.com endpoint. As the AWS developer, how can you satisfy this requirement?

    - A. Use Layers to the underlying Lambda functions of the API Gateway.
    - B. Modify the Integration Response of the API Gateway to add different endpoints for each release.
    - C. Modify the Integration Request of the API Gateway to manage different endpoints for each release.
    - D. Set up Stage Variables for each release.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>



    













