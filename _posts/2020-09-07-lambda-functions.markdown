# Lambdas

Within the context of Serverless, there are multiple ways to give Lambda functions permissions to access other AWS resources:

1. By default, Lambdas assume a role that has various CloudWatch permissions. You can add additional permissions to that role by adding IAM role statements to `serverless.yml`. Doing this will update the default role by merging those additional permissions with the pre-existing ones.

2. Another method is to forego the default role by defining a top-level role in the `serverless.yml` that all functions assume on execution. This wasn't documented in the Serverless AWS docs but I found that the role also needed to allow Lambda to assume it, which can be achieved by allowing the service principal `lambda.amazonaws.com` access to call `AssumeRole`:

```javascript
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "lambda.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

These methods apply to all functions within a service but it's also possible to configure permissions for individual Lambdas differently.