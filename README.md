# Terraform

Terrform repo for my excersice with ned course on plurights

## Using the files

In the course, you are given a Terraform configuration for a basic web application from someone else on the Globomantics team. We are going to make a copy of this configuration and modify it over the length of the course. The `base_web_app` directory has the basic web app configuration, which we will copy over to the `globo_web_app` and start making alterations.

As we progress through the modules, you will be challenged to make updates to the files in `globo_web_app` to meet the evolving needs and requirements of the web application infrastructure. The completed solution for each module is in the `mX_solution` directories. I recommend trying to first write the solution yourself, and then checking your answer against what you see in the solution file.

At the beginning of module three, we will hardcode our AWS keys into the configuration. **You would not do this in any kind of scenario!** I am trying to illustrate a point in the course. *Please do not commit your AWS keys to source control*. Some of us (**me**) have done this in the past and felt very silly. We will move these keys into environment variables in module four, and they shall never again be hardcoded **anywhere**.

The suggested commands for each module are in the `commands` directory. You can run these commands to get through the exercises, but I also encourage you to experiment and try things out for yourself.

## AWS Environment

You will need access to an AWS environment with permissions to create resources in EC2, S3, and IAM. I recommend creating a throwaway account just for this course. The exercises have been tested with AWS region `us-east-1`. The input variable `aws_region` has `us-east-1` set as the default, but you can supply a different region if you prefer. Generally, the exercises should work in any region that has at least three availability zones and an Amazon Linux 2 AMI.

You will need to generate an AWS access key to run through the exercises. You can do this through the IAM console in a browser (*hint*: it's under security credentials for your user) by following the [official AWS docs](https://aws.amazon.com/premiumsupport/knowledge-center/create-access-key/). I'd recommend assigning the `AdministratorAccess` policy to your user to give you permissions to do everything in the account. Also, enable 2FA for the user account!