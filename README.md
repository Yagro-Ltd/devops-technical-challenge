# DevOps Tech Challenge

## **Challenge Details**

The DevOps team at YAGRO serve as the infrastructure engineers for the company. Strong competency with both AWS (or other cloud environments) and creating CI/CD pipelines are required for this position.

This challenge is not about creating an all-singing and all-dancing product, it is about seeing how you implement a solution and the ways you go about it. Don’t go and give up a whole week working on this, that wouldn’t be fair on you 😃

What we are looking for is **Terraform code written to deploy an Auto Scaling Group (ASG) of web servers that deliver a website on AWS from a load balancer**. This should include the following:

1. VPC Configuration with subnets in multiple Availability Zones
2. EC2 Configuration
3. ELB to manage traffic
4. A running copy of a basic web page (Hello world will suffice) 

We love answering questions. Please send us your questions at the email address we sent you the challenge from. We're happy to help!

## **Requirements**

1. Runs on AWS Infrastructure.
2. The website is publicly accessible via the ELB.
3. The website should **not** be publicly accessible unless going through the ELB.
4. Code is documented in some way or another.

**Bonus Points** (not required at all) for *any* of the following:

- Include some form of CI/CD pipeline code. GitHub Actions, Jenkins, or any other tool is fine.
- Have the group of ASG's deliver said application via an ECS Cluster.
- Consider how the configuration can be reused in multiple builds
- Create a method to add linting or verifying that the code meets [Terraform style conventions](https://www.terraform.io/docs/language/syntax/style.html).

## **Submission**

Please upload your code to GitHub (or alike) and submit via email to the YAGRO team member you have been speaking too.
