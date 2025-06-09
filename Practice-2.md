---
layout: exam
---

# Practice Exam 2

1. A company wants to automate its order fulfillment and inventory tracking workflow. Starting from order creation to updating inventory to shipment, the entire process has to be tracked, managed and updated automatically. Which of the following would you recommend as the most optimal solution for this requirement?
   
   - A. Use AWS Step Functions to coordinate and manage the components of order management and inventory tracking workflow
   - B. Use Amazon SNS to develop event-driven applications that can share information
   - C. Configure Amazon EventBridge to track the flow of work from order management to inventory tracking systems
   - D. Use Amazon Simple Queue Service (Amazon SQS) queue to pass information from order management to inventory tracking workflow

     <details markdown=1><summary markdown='span'>Answer</summary>
       Correct answer: A
     </details>

2. You team maintains a public API Gateway that is accessed by clients from another domain. Usage has been consistent for the last few months but recently it has more than doubled. As a result, your costs have gone up and would like to prevent other unauthorized domains from accessing your API. Which of the following actions should you take?

   - A. Use Account-level throttling
   - B. Restrict access by using CORS
   - C. Use Mapping Templates
   - D. Assign a Security Group to your API Gateway

     <details markdown=1><summary markdown='span'>Answer</summary>
       Correct answer: B
     </details>

3. You work as a developer doing contract work for the government on AWS gov cloud. Your applications use Amazon Simple Queue Service (SQS) for its message queue service. Due to recent hacking attempts, security measures have become stricter and require you to store data in encrypted queues. Which of the following steps can you take to meet your requirements without making changes to the existing code?

   - A. Enable SQS KMS encryption
   - B. Use Secrets Manager
   - C. Use Client side encryption
   - D. Use the SSL endpoint
   
     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: A
     </details>

4. A company stores confidential data on an Amazon Simple Storage Service (S3) bucket. New regulatory guidelines require that files be stored with server-side encryption. The encryption used must be Advanced Encryption Standard (AES-256) and the company does not want to manage S3 encryption keys. Which of the following options should you use?

   - A. SSE-KMS
   - B. Client Side Encryption
   - C. SSE-S3
   - D. SSE-C

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: C
     </details>

5. Your company has embraced cloud-native microservices architectures. New applications must be dockerized and stored in a registry service offered by AWS. The architecture should support dynamic port mapping and support multiple tasks from a single service on the same container instance. All services should run on the same EC2 instance. Which of the following options offers the best-fit solution for the given use-case?
   
   - A. Application Load Balancer + ECS
   - B. Classic Load Balancer + Beanstalk
   - C. Application Load Balancer + Beanstalk
   - D. Classic Load Balancer + ECS

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: A
     </details>

6. A website serves static content from an Amazon Simple Storage Service (Amazon S3) bucket and dynamic content from an application load balancer. The user base is spread across the world and latency should be minimized for a better user experience. Which technology/service can help access the static and dynamic content while keeping the data latency low?

   - A. Configure CloudFront with multiple origins to serve both static and dynamic content at low latency to global users
   - B. Use CloudFront's Lambda@Edge feature to server data from S3 buckets and load balancer programmatically on-the-fly
   - C. Use CloudFront's Origin Groups to group both static and dynamic requests into one request for further processing
   - D. Use Global Accelerator to transparently switch between S3 bucket and load balancer for different data needs

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: A
     </details>

7. A firm runs its technology operations on a fleet of Amazon EC2 instances. The firm needs a certain software to be available on the instances to support their daily workflows. The developer team has been told to use the user data feature of EC2 instances. Which of the following are true about the user data EC2 configuration? ( Select two)

   - A. By default, user data runs only during the boot cycle when you first launch an instance
   - B. By default, scripts entered as user data are executed with root user privileges
   - C. When an instance is running, you can update user data by using root user credentials
   - D. By default, scripts entered as user data do not have root user privileges for executing
   - E. By default, user data is executed every time an EC2 instance is re-started

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: A, B
     </details>

8. A .NET developer team works with many ASP.NET web applications that use EC2 instances to host them on IIS. The deployment process needs to be configured so that multiple versions of the application can run in AWS Elastic Beanstalk. One version would be used for development, testing, and another version for load testing. Which of the following methods do you recommend?

   - A. Use only one Beanstalk environment and perform configuration changes using an Ansible script
   - B. Create an Application Load Balancer to route based on hostname so you can pass on parameters to the development Elastic Beanstalk environment. Create a file in .ebextensions/ to know how to handle the traffic coming from the ALB
   - C. You cannot have multiple development environments in Elastic Beanstalk, just one development and one production environment
   - D. Define a dev environment with a single instance and a 'load test' environment that has settings close to production environment

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: D
     </details>

9. A developer is defining the signers that can create signed URLs for their Amazon CloudFront distributions. Which of the following statements should the developer consider while defining the signers? (Select two)

   - A. You can also use AWS Identity and Access Management (IAM) permissions policies to restrict what the root user can do with CloudFront key pairs
   - B. CloudFront key pairs can be created with any account that has administrative permissions and full access to CloudFront resources
   - C. Both the signers (trusted key groups and CloudFront key pairs) can be managed using the CloudFront APIs
   - D. When you create a signer, the public key is with CloudFront and private key is used to sign a portion of URL
   - E. When you use the root user to manage CloudFront key pairs, you can only have up to two active CloudFront key pairs per AWS account

     <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: D, E
     </details>

10. You were assigned to a project that requires the use of the AWS CLI to build a project with AWS CodeBuild. Your project's root directory includes the buildspec.yml file to run build commands and would like your build artifacts to be automatically encrypted at the end. How should you configure CodeBuild to accomplish this?
    
    - A. Use an AWS Lambda Hook
    - B. Use In Flight encryption (SSL)
    - C. Specify a KMS key to use
    - D. Use the AWS Encryption SDK

      <details markdown=1><summary markdown='span'>Answer</summary>
        Correct answer: C
     </details>


