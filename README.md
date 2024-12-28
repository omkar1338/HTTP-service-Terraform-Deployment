# HTTP-service-Terraform-Deployment
HTTP service creation and it's Terraform Deployment

Assignment for Hiring Evaluation
Problem Statement
You are required to complete the following tasks as part of this assignment:

Part 1: HTTP Service
Develop an HTTP service in any programming language of your choice. The service should
expose the following endpoint:
Endpoint: GET http://IP:PORT/list-bucket-content/<path>
● Functionality:
○ This endpoint returns the content of an S3 bucket for the specified path.
○ If no path is specified, the top-level content of the bucket is returned.
○ The response should be in JSON format.

Example Scenarios:
Assume the S3 bucket contains the following structure:
Copy code
|_ dir1
|_ dir2
|_ file1
|_ file2

● GET http://IP:PORT/list-bucket-content
○ Response: {"content": ["dir1", "dir2", "file1", "file2"]}
● GET http://IP:PORT/list-bucket-content/dir1
○ Response: {"content": []}
● GET http://IP:PORT/list-bucket-content/dir2
○ Response: {"content": ["file1", "file2"]}

Part 2: Terraform Deployment
Write a Terraform layout to provision AWS infrastructure and deploy the HTTP service
created in Part 1.
● The Terraform code should:
1. Create and configure the necessary AWS resources.
2. Deploy the service to AWS (e.g., using EC2, ECS, Lambda, or any other
appropriate AWS service).

Evaluation Criteria
1. Code Quality:
○ Clarity, simplicity, adherence to language-specific coding standards, and
inclusion of test cases.
2. Infrastructure Quality:
○ Quality of Terraform layouts, deployment topology, and configuration
management (including secret management).

3. Error Handling:
○ Gracefully handle errors for invalid or non-existing paths, e.g.,
http://IP:PORT/list-bucket-content/non-existing.

4. Bonus Points:
○ Secure the service with HTTPS.
○ Provide a comprehensive README file explaining your design decisions,
assumptions, and any challenges faced.
○ Submit a short video demo of the working solution, along with screenshots of
the S3 bucket structure and API responses.

