# Serverless Framework WildRydes Webapp

[![Made with Serverless](https://img.shields.io/badge/serverless-⚡-yellow.svg?style=flat-square)](https://serverless.io)
## 🦄 Unicorns made even better with Serverless! 
Start with the [AWS Labs WildRydes Webapp example](https://github.com/awslabs/aws-serverless-workshops/tree/master/WebApplication)

I used [Serverless-Stack](https://serverless-stack.com/) as a heavy reference guide on how to integrate the Serverless Framework into the AWS Labs example. 

## Things to do in the AWS Web Console
* Follow Module 1 to Create the S3 Bucket, Upload Content, Add a Bucket Policy, and Enable web hosting
* In Module 2 create the Cognito User Pool
* In Module 3 create the DynamoDB Table

## Things that Serverless Framework handle 
* Writing and uploading the Lambda Function
* Attaching an Execution Role between DynamoDB and the Lambda
* Create a mock request to test the function locally
```
sls invoke local --function request --path mocks/request-event.json
```
* Create and configure the API Gateway endpoint

The client side file, `config.js` still has to be updated and uploaded to S3. I used `env.json` to hold the ARN for the Cognito Pool as an authorizer property in the `serverless.yaml` file. 