# All at once

- The EC2 instances in the environment are all updated simultaneously.
- Requires downtime.

# Immutable

- The existing EC2 instances are not modified.
- The release is deployed to a newly created batch of EC2 instances, doubling the number momentarily.
- Once the deployment is successful, the old EC2 instances are destroyed.

# Rolling

- The release is deployed to a subset of EC2 instances, leaving the rest up. Once the release has finished deploying to those, the release is deployed to a new subset of instances. Repeat until all instances have the update.
- During deployment, the number of available EC2 instances will be less than there are normally, which would be a problem if handling load is a concern.

# Rolling with additional batch

- Like Rolling, but allows you to retain full capacity by creating a new batch of EC2 instances.

# Blue-green

- Like Immutable, except a new Elastic Beanstalk environment is created. Once the updates are made to the new environment, the CNAME record points to that instead of the old environment.
- The old environment gets destroyed; this would probably be an issue if that environment also contained an RDS instance attached.