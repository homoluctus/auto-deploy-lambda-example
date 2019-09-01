# Demo Auto Deploy Lambda
This repository is demo app to automatically deploy to AWS Lambda using GitHub Actions

# Usage
## 1. Set GitHub secrets
Set the following parameters in GitHub secrets:

- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- SLACK_WEBHOOK

## 2. Uncomment YAML file
Please uncomment `.github/workflows/deploy.yml` and `.github/workflows/remove.yml`.<br>

## 3. Push to master branch
Start deploy to AWS Lambda when you push to master branch.<br>
So, you commit and push after uncommenting the above two files.

## 4. Deploy using GitHub Actions
Start GitHub Actions and automatically deploy to AWS Lambda after pushed to master branch.<br>
So, You just wait.<br>
After tens seconds or minutes, you receive a slack notification like below.<br>

- Invoke Lambda function

<img src="./images/lambda.png" alt="invoke_lambda">

- GitHub Actions Success

<img src="./images/slack_deploy.png" alt="deploy_lambda_notification">

## 5. Remove Lambda
You push to branch called 'remove'.<br>
GitHub Actions deletes Lambda instead of you.
After a moment, you receive a notification like below.<br>

<img src="./images/slack_remove.png" alt="remove_lambda_notification">


# GitHub Actions screen
## Deploy Lambda

<img src="./images/auto_deploy.png">

## Remove Lambda

<img src="./images/remove_lambda.png">