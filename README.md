# rsc-aws-lambda-simple-dynamodb-get
A simple Node lambda that retrieves a value from a DynamoDB and returns either 200 SUCCESS or 404 ERROR if the file is not found. 

## Installation


### Requirements

Node v17.3.0 (at least node.js 14 for AWS SDK to work)
npm 8.3.0

## Usage

### Successful invocation

### Error (file not found) invocation

## Testing

# AWS Deployment

## How to Deploy

Run these commands from the root directory to deploy the code to AWS. You will need your `~/.aws/credentials` file set up with the default account you want to update. 

Zip up the index.js file
```bash
zip function.zip index.js
```

To deploy this code to AWS run the following commands from the root directory
```bash
aws lambda update-function-code --function-name <function-name> --zip-file fileb://function.zip
```

## How to Test

Run the following command to test the lambda is working in the AWS account.

```bash
aws lambda invoke --function-name <function-name> response.json
```