Lambda is a serverless compute service that runs code in response to events without the need to provision or manage servers. It automatically manages the underlying infrastructure, scaling resources based on the volume of requests. You are charged only for the compute time consumed, down to the millisecond. Lambda handles execution, scaling, and resource allocation. Each Lambda function has a **maximum execution time of 15 minutes per invocation**, meaning if the code runs longer than that, it will be terminated. You can also optimize performance by configuring the appropriate memory size for your function.

Lambda is perfect for this event-driven use case. It can run code in response to uploads and scale automatically based on the number of events.
### **How Lambda Works**

1. **Upload code to Lambda**  
    First, you upload your code to AWS Lambda, which is stored as a **Lambda function**.
    
2. **Set code to trigger from an event source**  
    Next, you configure your function to be triggered by events, such as AWS services (e.g., S3 file upload, DynamoDB update), API Gateway (HTTP requests), or even mobile and web applications.
    
3. **Run code when triggered**  
    Your code runs only when an event occurs. Lambda automatically handles the **server management, scaling, and infrastructure**, so you don’t have to. The Lambda runtime executes your function using the event data passed to it. Each execution can last for a maximum of **15 minutes per invocation**, after which it is terminated if still running.
    
4. **Pay only for the compute time used**  
    You are charged only for the compute time your function consumes, measured **down to the millisecond**. The cost depends on the **memory size** allocated to your function.
    

---

✅ This way, Lambda ensures your code runs **reliably, securely, and efficiently**, without you managing servers or infrastructure.

![[Pasted image 20250915141414.png]]

- **Architecture**
    - An SQS queue is used to store incoming messages.
    - AWS Lambda is triggered automatically whenever a new message is added to the queue.
        
- **Function creation**
    - A Lambda function is created using a blueprint for SQS integration.
    - Runtime (e.g., Node.js, Python, Java, or custom) can be chosen when creating the function.
        
- **Permissions**
    - An **execution role** with the proper IAM policy (e.g., SQS poller policy) is assigned to allow the Lambda function to read messages from the queue.
        
- **Trigger setup**
    - The SQS queue is configured as the event source for the Lambda function.
    - Messages placed in the queue automatically invoke the Lambda function.
        
- **Processing**
    - Lambda retrieves messages, logs details (e.g., ID, text), and marks them as processed.
    - Messages are removed from the queue after processing.
        
- **Monitoring**
    - Function logs and metrics are available in **Amazon CloudWatch** for verification and debugging.
        
- **Result**
    - A simple, serverless, event-driven workflow where messages are reliably processed with minimal infrastructure management.
