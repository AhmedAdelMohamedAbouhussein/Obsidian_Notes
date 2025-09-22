serverless setup
![[Pasted image 20250922201055.png]]
## Receive traffic

An Amazon API Gateway receives and validates HTTP requests.

## Trigger Lambda function

The API Gateway triggers a Lambda function that sends requests to Amazon DynamoDB.

## Monitor traffic

X-Ray traces requests through API Gateway, Lambda, DynamoDB and back to the client. This helps developers troubleshoot any problems.



![[Pasted image 20250922201217.png]]
## Accept customer input

Customers submit questions using a contact form housed on a static Amazon S3 website.

## Receive request

An API Gateway receives and validates the contact form request.

## Send email

The API Gateway then invokes a Lambda function that sends an email to the business owner using Amazon SES.

![[Pasted image 20250922202048.png]]
## Initiate contact

A customer calls or texts a customer support center. Calls are placed into the Amazon Connect interactive voice response (IVR) system. Text messages are routed to Amazon Connect from CloudFront.

## Connect to agent

Amazon Connect tries to connect the customer with a live agent.

## Provide options

For calls with long wait lines, customers can choose to receive an agent callback or they can switch to text through a Lambda function.