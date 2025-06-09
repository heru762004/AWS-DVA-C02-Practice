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
    </picture><BR>
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

23. A financial services company is developing a real-time fraud detection system for its payment processing application. Payment transaction events are sent via an API, and the system must analyze each transaction in real-time to identify and flag potentially fraudulent activities. The solution should support concurrent processing by multiple fraud detection models and monitoring systems while ensuring scalability, low-latency performance, and cost optimization. Which AWS service is best suited to meet these requirements?

    - A. Amazon Data Firehose
    - B. Amazon Managed Streaming for Apache Kafka (Amazon MSK)
    - C. Amazon Kinesis Data Streams
    - D. Amazon Kinesis Agent

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

24. A recruitment agency has a large collection of resumes stored in an Amazon S3 bucket. The agency wants to perform an analysis on these files, but for privacy compliance reasons, they need to ensure that certain personally identifiable information (PII) is redacted before being processed by their internal service. Which solution can meet the requirements in the most cost-effective way?

    - A. Use Amazon S3 Object Lambda to redact PII before it is returned to the application.
    - B. Implement a solution with AWS Glue to transform the data and redact PII before storing it in an S3 bucket.
    - C. Configure an Amazon S3 Access Point and set up an Amazon CloudFront distribution with a Lambda@Edge function to redact the PII as data is fetched from the S3 bucket.
    - D. Use a Lambda function to create a redacted copy of each file in a separate S3 bucket. Then, set up an Amazon S3 Access Point to serve these files.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

25. A DynamoDB table has several top-level attributes such as id, course_id, course_title, price, rating and many others. The database queries of your application returns all of the item attributes by default but you only want to fetch specific attributes such as the course_id and price per request. As the developer, how can you refactor your application to accomplish this requirement?

    - A. Use filter expressions
    - B. Use expression attribute names
    - C. Use projection expression
    - D. Use condition expressions

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

26. Your application is processing one Kinesis data stream which has four shards, and each instance has one KCL worker. To scale up processing in your application, you reshard your stream to increase the number of open shards to six. What is the MAXIMUM number of EC2 instances that you should launch to achieve optimum performance?

    - A. 6
    - B. 3
    - C. 5
    - D. 12

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

27. An application hosted in a multicontainer Docker platform in Elastic Beanstalk uses DynamoDB to handle the session data of its users. These data are only used in a particular timeframe and the stale data can be deleted after the user logged out of the system. Which of the following is the most suitable way to delete the session data?

    - A. Use conditional writes to add the session data to the DynamoDB table and then automatically delete it based on the condition you specify.
    - B. Delete the stale data by regularly performing a scan on the table.
    - C. Enable TTL for the session data in the DynamoDB table.
    - D. Use atomic counters to track the validity of the session data and delete once it becomes stale.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

28. A developer uses AWS SAM templates to deploy a serverless application. He needs to embed the application from the AWS Serverless Application Repository or from an S3 bucket as a nested application. Which of the following resource type is the most SUITABLE one that the developer should use?

    - A. WS::Serverless::Application
    - B. AWS::Serverless::Function
    - C. AWS::Serverless::LayerVersion
    - D. AWS::Serverless::Api	

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

29. A programmer is developing a Node.js application that will be run on a Linux server in their on-premises data center. The application will access various AWS services such as S3, DynamoDB, and ElastiCache using the AWS SDK. Which of the following is the MOST suitable way to provide access for the developer to accomplish the specified task?

    - A. Create an IAM role with the appropriate permissions to access the required AWS services and assign the role to the on-premises Linux server. Whenever the application needs to access any AWS services, request for temporary security credentials from STS using the AssumeRole API.	
    - B. Go to the AWS Console and create a new IAM user with programmatic access. In the application server, create the credentials file at ~/.aws/credentials with the access keys of the IAM user.	
    - C. Go to the AWS Console and create a new IAM User with the appropriate permissions. In the application server, create the credentials file at ~/.aws/credentials with the username and the hashed password of the IAM User.	
    - D. Create an IAM role with the appropriate permissions to access the required AWS services. Assign the role to the on-premises Linux server.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

30. An application hosted in an Auto Scaling group of On-Demand EC2 instances is used to process data polled from an SQS queue, and the generated output is stored in an S3 bucket. To enhance security, you were tasked to ensure that all objects in the S3 bucket are encrypted at rest using server-side encryption with AWS KMS keys. Which of the following is required to properly implement this requirement?

    - A. Add a bucket policy which denies any s3:PutObject action unless the request includes the x-amz-server-side-encryption header.
    - B. Add a bucket policy which denies any s3:PutObject action unless the request includes the x-amz-server-side-encryption-aws-kms-key-id header.	
    - C. Add a bucket policy which denies any s3:PostObject action unless the request includes the x-amz-server-side-encryption header.	
    - D. Add a bucket policy which denies any s3:PostObject action unless the request includes the x-amz-server-side-encryption-aws-kms-key-id header.
   
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

31. A serverless application consisting of Lambda functions integrated with API Gateway, and DynamoDB processes ad hoc requests that its users send. Due to the recent spike in incoming traffic, some of your customers are complaining that they are getting HTTP 504 errors from time to time. Which of the following is the MOST likely cause of this issue?

    - A. Since the incoming requests are increasing, the API Gateway automatically enabled throttling which caused the HTTP 504 errors.
    - B. The usage plan quota has been exceeded for the Lambda function.
    - C. An authorization failure occurred between API Gateway and the Lambda function.
    - D. API Gateway request has timed out because the underlying Lambda function has been running for more than 29 seconds.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

32. A company has a microservices application that must be integrated with API Gateway. The developer must configure custom data mapping between the API Gateway and the microservices. In addition, the developer must specify how the incoming request data is mapped to the integration request and how the resulting integration response data is mapped to the method response. Which of the following integration types is the MOST suitable one to use in API Gateway to meet this requirement?

    - A. AWS	
    - B. HTTP	
    - C. AWS_PROXY	
    - D. HTTP_PROXY

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

33. To improve their information security management system (ISMS), a company recently released a new policy which requires all database credentials to be encrypted and be automatically rotated to avoid unauthorized access. Which of the following is the MOST appropriate solution to secure the credentials?

    - A. Create an IAM Role which has full access to the database. Attach the role to the services which require access.
    - B. Create a parameter to the Systems Manager Parameter Store using the PutParameter API with a type of SecureString.	
    - C. Enable IAM DB authentication which rotates the credentials by default.
    - D. Create a secret in AWS Secrets Manager and enable automatic rotation of the database credentials.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

34. A developer is moving a legacy web application from their on-premises data center to AWS. The application is used simultaneously by thousands of users, and their session states are stored in memory. The on-premises server usually reaches 100% CPU Utilization every time there is a surge in the number of people accessing the application. Which of the following is the best way to re-factor the performance and availability of the application’s session management once it is migrated to AWS?

    - A. Use an ElastiCache for Redis cluster to store the user session state of the application.
    - B. Store the user session state of the application using CloudFront.
    - C. Use Sticky Sessions with Local Session Caching.
    - D. Use an ElastiCache for Memcached cluster to store the user session state of the application.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

35. A serverless application is composed of several Lambda functions which reads data from RDS. These functions must share the same connection string that should be encrypted to improve data security. Which of the following is the MOST secure way to meet the above requirement?

    - A. Create a Secure String Parameter using the AWS Systems Manager Parameter Store.
    - B. Use AWS Lambda environment variables encrypted with KMS which will be shared by the Lambda functions.
    - C. Create an IAM Execution Role that has access to RDS and attach it to the Lambda functions.
    - D. Use AWS Lambda environment variables encrypted with CloudHSM.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

36. A Lambda function downloads the same 250 MB file between invocations and stores it in memory for processing. This leads to frequent timeouts and negatively impacts the performance of the serverless application. Which change should be made to resolve the issue most effectively?

    - A. Increase the timeout of the function.
    - B. Store the file in the /tmp directory of the execution context and reuse it on succeeding invocations.	
    - C. Increase the memory allocation of the function.
    - D. Increase the ephemeral storage size of the function

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

37. A Lambda function has been integrated with DynamoDB Streams as its event source. There has been a new version of the function that needs to be deployed using CodeDeploy where the traffic must be shifted in two increments. It should shift 10 percent of the incoming traffic to the new version in the first increment and then the remaining 90 percent should be deployed five minutes later. Which of the following deployment configurations is the MOST suitable to satisfy this requirement?

    - A. Linear
    - B. Canary
    - C. Rolling with additional batch
    - D. All-at-once

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

38. A developer is working on a Lambda function which has an event source mapping to process requests from API Gateway. The function will consistently have 10 requests per second and it will take a maximum of 50 seconds to complete each request. What should the developer do to prevent the function from throttling?

    - A. Submit a Service Limit Increase request to AWS to raise your concurrent executions limit.	
    - B. Implement traffic shifting in Lambda using Aliases.
    - C. Use Dead Letter Queues (DLQ) to reprocess failed requests.
    - D. Do nothing since Lambda will automatically scale to handle the load.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

39. A developer needs to encrypt all objects being uploaded by their application to the S3 bucket to comply with the company’s security policy. The bucket will use server-side encryption with Amazon S3-Managed encryption keys (SSE-S3) to encrypt the data using 256-bit Advanced Encryption Standard (AES-256) block cipher. Which of the following request headers should the developer use?

    - A. x-amz-server-side-encryption
    - B. x-amz-server-side-encryption-customer-key-MD5
    - C. x-amz-server-side-encryption-customer-key
    - D. x-amz-server-side-encryption-customer-algorithm

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

40. A developer is refactoring a Lambda function that currently processes data using a public GraphQL API. There’s a new requirement to store query results in a database hosted in a VPC. The function has been configured with additional VPC-specific information, and the database connection has been successfully established. However, the engineer has discovered that the function can no longer connect to the internet after testing. Which of the following should the developer do to fix this issue? (Select TWO.)

    - A. Add a NAT gateway to your VPC.
    - B. Submit a limit increase request to AWS to raise the concurrent executions limit of your Lambda function.
    - C. Ensure that the associated security group of the Lambda function allows outbound connections.
    - D. Configure your function to forward payloads that were not processed to a dead-letter queue (DLQ) using Amazon SQS.
    - E. Set up elastic network interfaces (ENIs) to enable your Lambda function to connect securely to other resources within your private VPC.
   
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A, C. 
    </details>

41. A developer is building a photo-sharing application that automatically enhances images uploaded by users to Amazon S3. When a user uploads an image, its S3 path is sent to an image-processing application hosted on AWS Lambda. The Lambda function applies the selected filter to the image and stores it back to S3. If the upload is successful, the application will return a prompt telling the user that the request has been accepted. The entire processing typically takes an average of 5 minutes to complete, which causes the application to become unresponsive. Which of the following is the MOST suitable and cost-effective option which will prevent the application from being unresponsive?

    - A. Use a combination of Lambda and Step Functions to orchestrate service components and asynchronously process the requests.
    - B. Configure the application to asynchronously process the requests and change the invocation type of the Lambda function to Event.	
    - C. Configure the application to asynchronously process the requests and use the default invocation type of the Lambda function.
    - D. Use AWS Serverless Application Model (AWS SAM) to allow asynchronous requests to your Lambda function.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

42. A developer has an application that uses a Lambda function to process data from an Aurora MySQL DB Instance in a Virtual Private Cloud (VPC). The database throws a MySQL: ERROR 1040: Too many connections error whenever there is a surge in incoming traffic. Which is the most suitable solution for resolving the issue?

    - A. Increase the concurrency limit of the Lambda function
    - B. Increase the allocated memory of your function.
    - C. Increase the value of the max_connections parameter of the Aurora MySQL DB Instance.	
    - D. Provision an RDS Proxy between the Lambda function and the RDS database instance

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

43. You want to update a Lambda function on your production environment and ensure that when you publish the updated version, you still have a quick way to roll back to the older version in case you encountered a problem. To prevent any sudden user interruptions, you want to gradually increase the traffic going to the new version. Which of the following implementation is the BEST option to use?

    - A. Use Traffic Shifting with Lambda Aliases.
    - B. Use ELB to route traffic to both Lambda functions.
    - C. Use Route 53 weighted routing to two Lambda functions.
    - D. Use stage variables in your Lambda function.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

44. A developer is creating a script using AWS CLI to retrieve a list of objects in an S3 bucket. However, the script is timing out if the bucket has tens of thousands of objects. Which solution would most likely rectify the issue?

    - A. Enable Amazon S3 Transfer Acceleration
    - B. Increase the AWS CLI timeout value
    - C. Apply the pagination parameters in the AWS CLI command
    - D. Enable CORS

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

45. A company operates an e-commerce website on Amazon Elastic Container Service (ECS) behind an Application Load Balancer (ALB). They’ve set their ALB as an origin for an Amazon CloudFront distribution. Users interact with the website via a custom domain linked to the CloudFront distribution, all maintained within a public hosted zone in Amazon Route 53. The company wants to display region-specific pricing tables to its users. For example, when a user from the UK visits the site, they should be redirected to https://tutorialsdojo.com/uk/, while users from the Philippines should view prices on https://tutorialsdojo.com/ph/
How can a developer incorporate this feature in the least amount of development overhead?

    - A. Forward the CloudFront-Viewer-Address header to the web server running on the ECS cluster. Implement a custom logic that matches the header’s value against a GeoIP database to determine user location. Based on the resolved location, redirect users to the appropriate region-specific URL.	
    - B. Configure the Route 53 record to use the geolocation routing policy.
    - C. Implement a CloudFront function that returns the appropriate URL based on the CloudFront-Viewer-Country. Configure the distribution to trigger the function on Viewer request events.	
    - D. Use AWS Web Application Firewall (WAF's) geo-matching rule to identify the user country and attach it to the ALB. Configure ALB listener rules with path conditions to route traffic based on the identified country.

      <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

46. A company offers a Generative Artificial Intelligence (AI) service exposed through a REST API managed by Amazon API Gateway. They recently rolled out a subscription tier where users receive API keys to access premium features. The company uses the CreateApiKey API for generating these keys. During testing, developers noticed that while existing users can access the service without issues, new premium subscribers get a 403 Forbidden error when using their API keys. What must be done to give new users access to the service?

    - A. Use the ImportApiKeys operation to import the premium users’ keys, then apply the UpdateUsagePlan operation to set the new tier access.	
    - B. Instruct users to send their API key in a custom header. In the integration request, adjust the mapping template to extract and evaluate this header to distinguish between free-tier and premium subscribers.
    - C. Use the UpdateAuthorizer operation to modify the authorization settings. Promote the changes to the production stage by calling the CreateDeployment operation.
    - D. Associate the API keys for the premium users with the intended usage plan using the CreateUsagePlanKey operation.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

47. A developer is managing a serverless application orchestrated by AWS Step Functions. One of the Lambda functions sends an API call to a third-party payment service, which takes some time to complete. The Step Functions workflow needs to pause while the service validates the payment. It should only resume after the service sends a notification to a webhook endpoint. Which combination of actions will fulfill the requirements in the most cost-effective manner? (Select Two)

    - A. Configure the webhook handler to call the SendTaskHeartbeat method after a successful notification.	
    - B. Configure the Lambda function task state to use the waitForTaskToken option. Retrieve the task token from the context object of the state machine and include it as part of the Lambda function’s payload body.	
    - C. Configure the webhook handler to call the SendTaskSuccess method after a successful notification.	
    - D. Use a Wait State to pause the execution of the workflow. Configure the webhook handler to invoke the Lambda function synchronously.
    - E. Set the invocation method of the Lambda function task state to asynchronous. Create an AWS SQS queue and configure the webhook handler to send the payment service’s response to the queue. Use a combination of Wait State and Choice State to poll the queue.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B, C. 
    </details>

48. A developer is building a web application which requires a multithreaded event-based key/value cache store that will cache result sets from database calls. You need to run large nodes with multiple cores for your cache layer and it should scale up or down as the demand on your system increases and decreases. Which of the following is the MOST suitable service that you should use?

    - A. AWS Greengrass
    - B. Amazon ElastiCache for Memcached
    - C. Amazon ElastiCache for Redis
    - D. Amazon CloudFront

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

49. A web application is running in an ECS Cluster and updates data in DynamoDB several times a day. The clients retrieve data directly from the DynamoDB through APIs exposed by Amazon API Gateway. Although API caching is enabled, there are specific clients that want to retrieve the latest data from DynamoDB for every API request sent. What should be done to only allow authorized clients to invalidate an API Gateway cache entry when submitting API requests? (Select TWO.)

    - A. Tick the Require Authorization checkbox in the Cache Settings of your API via the console.	
    - B. The client must send a request which contains the Cache-Control: max-age=1 header.	
    - C. The client must send a request which contains the Cache-Control: max-age=0 header.	
    - D. Modify the cache settings to retrieve the latest data from DynamoDB if the request header's authorization signature matches your API's trusted clients list.
    - E. Provide your clients an authorization token from STS to query data directly from DynamoDB.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A, C. 
    </details>

50. A new IT policy requires you to trace all calls that your Node.js application sends to external HTTP web APIs as well as SQL database queries. You have to instrument your application, which is hosted in Elastic Beanstalk, in order to properly trace the calls via the X-Ray console. What should you do to comply with the given requirement?

    - A. Enable active tracing in the Elastic Beanstalk by including the healthcheckurl.config configuration file in the .ebextensions directory of your source code.	
    - B. Use a user data script to run the daemon automatically.
    - C. Create a Docker image that runs the X-Ray daemon.
    - D. Enable the X-Ray daemon by including the xray-daemon.config configuration file in the .ebextensions directory of your source code.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

51. A developer is building an e-commerce application which will be hosted in an ECS Cluster. To minimize the number of instances in use, she must select a strategy which will place tasks based on the least available amount of CPU or memory. Which of the following task placement strategy should the developer implement?

    - A. distinctInstance
    - B. spread
    - C. binpack
    - D. random
      
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

52. The users of a social media website must be authenticated using social identity providers such as Twitter, Facebook, and Google. Users can login to the site which will allow them to upload their selfies, memes, and other media files in an S3 bucket. As an additional feature, you should also enable guest user access to certain sections of the website. Which of the following should you do to accomplish this task?

    - A. Create a User Pool in Amazon Cognito and enable access to unauthenticated identities.
    - B. Create a custom identity broker which integrates with the AWS Security Token Service and supports unauthenticated access.
    - C. Create an Identity Pool in Amazon Cognito and enable access to unauthenticated identities.
    - D. Integrate AWS IAM Identity Center with your website.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

53. A developer is instructed to set up a new serverless architecture composed of AWS Lambda, API Gateway, and DynamoDB in a single stack. The new architecture should allow the developer to locally build, test, and debug serverless applications. Which of the following should the developer use to satisfy the above requirement?

    - A. AWS Elastic Beanstalk
    - B. AWS CloudFormation
    - C. AWS Serverless Application Model (AWS SAM)
    - D. AWS Systems Manager

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

54. You are deploying a serverless application composed of Lambda, API Gateway, CloudFront, and DynamoDB using CloudFormation. The AWS SAM syntax should be used to declare resources in your template which requires you to specify the version of the AWS Serverless Application Model (AWS SAM). Which of the following sections is required, aside from the Resources section, that should be in your CloudFormation template?

    - A. Parameters
    - B. Format Version
    - C. Mappings
    - D. Transform

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

55. A developer is building a Docker application using Amazon ECS. The application requires containers to maintain long-lived connections and access specific ports on the host container instance to send or receive traffic using port mapping. Which component of ECS should the developer configure to properly implement this task?

    - A. Container instance
    - B. Service scheduler
    - C. Container Agent
    - D. Task definition
   
    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

56. An online stock trading platform is hosted in an Auto Scaling group of EC2 instances with an Application Load Balancer in front to distribute the incoming traffic evenly. The developer must capture information about the IP traffic going to and from network interfaces in your VPC to comply with financial regulatory requirements. Which of the following options should the developer do to meet the requirement?

    - A. Use AWS Inspector to capture information about the IP traffic going to and from the network interfaces of your EC2 instances.
    - B. Use CloudTrail logs to track all API calls and capture information about the IP traffic going to and from your VPC.
    - C. Install and run the AWS X-Ray daemon to your EC2 instances using an instance metadata script.
    - D. Create a flow log in your VPC.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>

57. A web application is uploading large files, which are over 4 GB in size, in an S3 bucket called data.tutorialsdojo.com every 30 minutes. You want to minimize the time required to upload each file. Which of the following should you do to minimize upload time?

    - A. Use the Putltem API.
    - B. Use the Multipart upload API.
    - C. Enable Transfer Acceleration in the bucket.
    - D. Use the BatchWriteItem API.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

58.  developer is working on an application which stores data to an Amazon DynamoDB table with the DynamoDB Streams feature enabled. He set up an event source mapping with DynamoDB Streams and AWS Lambda function to monitor any table changes then store the original data of the overwritten item in S3. When an item is updated, it should only send a copy of the item’s previous value to an S3 bucket and maintain the new value in the DynamoDB table. Which StreamViewType is the MOST suitable one to use in the DynamoDB configuration to fulfill this scenario?

    - A. NEW_IMAGE	
    - B. KEYS_ONLY	
    - C. NEW_AND_OLD_IMAGES	
    - D. OLD_IMAGE	

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>



59. You developed a shell script which uses AWS CLI to create a new Lambda function. However, you received an InvalidParameterValueException after running the script. What is the MOST likely cause of this issue?

    - A. You have exceeded your maximum total code size per account.
    - B. The resource already exists.
    - C. You provided an IAM role in the CreateFunction API which AWS Lambda is unable to assume.	
    - D. The AWS Lambda service encountered an internal error.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

60. A Software Engineer is developing an application that will be hosted on an Amazon EC2 instance and read messages from a standard Amazon SQS queue. The average time that it takes for the producers to send a new message to the queue is 10 seconds. Which of the following is the MOST efficient way for the application to query the new messages from the queue?

    - A. Configure the SQS queue to use Long Polling.
    - B. Configure each message in the SQS queue to have a custom visibility timeout of 10 seconds.
    - C. Configure an SQS Delay Queue with a value of 10 seconds.
    - D. Configure the SQS queue to use Short Polling.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A. 
    </details>

61. A developer is working with an AWS Serverless Application Model (AWS SAM) application composed of several AWS Lambda functions. The developer runs the application locally on his laptop using sam local commands. While testing, one of the functions returns Access denied errors. Upon investigation, the developer discovered that the Lambda function is using the AWS SDK to make API calls within a sandbox AWS account. Which combination of steps must the developer do to resolve the issue? (Select TWO)

    - A. Use the aws configure command with the --profile parameter to add a named profile with the sandbox AWS account’s credentials.	
    - B. Create an AWS SAM CLI configuration file at the root of the SAM project folder. Add the AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY environment variables to it.
    - C. Run the function using sam local invoke with the --parameter-overrides parameter.
    - D. Add the AWS credentials of the sandbox AWS account to the Globals section of the template.yml file and reference them in the AWS::Serverless::Function properties section of the Lambda function.
    - E. Run the function using sam local invoke with the --profile parameter.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: A, E. 
    </details>

62. A developer has deployed a Lambda function that runs in DEV, UAT, and PROD environments. The function uses different parameters that varies based on the environment it is running in. The parameters are currently hardcoded in the function. Which action should the developer do to reference the appropriate parameters without modifying the code every time the environment changes?

    - A. Create individual Lambda Layers for each environment
    - B. Use environment variables to set the parameters per environment.
    - C. Create a stage variable called ENV and invoke the Lambda function by its alias name.	
    - D. Publish three versions of the Lambda function. Assign the aliases DEV, UAT, and PROD to each version.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

63. A development team has started using AWS CloudFormation for deploying Lambda functions. Their project structure places the source code for the Lambda function locally within a directory named “tutorialsdojo”. The lambda handler for the function is in a file called “app.js”. Below is a snippet of their template.
    <picture>
    <img src="https://td-portal-cdn.tutorialsdojo.com/wp-content/uploads/2019/12/aws-cda-practice-exam-cf-code-snippet-for-serverless-function.jpg"></img>
    </picture><BR>
    What is the next step in order for the template to be deployed using the aws cloudformation deploy CLI?

    - A. Use the Fn::Base64 intrinsic function inline with the CodeUri property to encode the content of the app.js file.	
    - B. Use the aws cloudformation package command to upload the local artifacts of the Lambda function to an S3 bucket and produce a version of the template with references to the S3 URI of the file.
    - C. Upload the app.js file to an S3 bucket. Update the CodeUri property in the template to point to the S3 URI of the file.	
    - D. Package the Lambda function in a ZIP file. Specify the local path of the packaged file in the CodeUri property.

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: B. 
    </details>

64. A company follows collaborative development practices. The engineering manager wants to isolate the development effort by setting up simulations of API components owned by various development teams. Which API integration type is best suited for this requirement?

    - A. HTTP
    - B. HTTP_PROXY
    - C. MOCK
    - D. AWS_PROXY

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: C. 
    </details>

65. A junior developer working on ECS instances terminated a container instance in Amazon Elastic Container Service (Amazon ECS) as per instructions from the team lead. But the container instance continues to appear as a resource in the ECS cluster. As a Developer Associate, which of the following solutions would you recommend to fix this behavior?

    - A. The container instance has been terminated with AWS CLI, whereas, for ECS instances, Amazon ECS CLI should be used to avoid any synchronization issues
    - B. A custom software on the container instance could have failed and resulted in the container hanging in an unhealthy state till restarted again
    - C. You terminated the container instance while it was in RUNNING state, that lead to this synchronization issues
    - D. You terminated the container instance while it was in STOPPED state, that lead to this synchronization issues

    <details markdown=1><summary markdown='span'>Answer</summary>
          Correct answer: D. 
    </details>












    













    
















    



















    









    







    





    













