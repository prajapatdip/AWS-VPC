# AWS VPC for Demonstrating App in Private Subnet

## Overview

This project provides a set of AWS CloudFormation templates to deploy a Virtual Private Cloud (VPC) on Amazon Web Services (AWS) that demonstrates the setup for hosting an application in a private subnet. The goal is to showcase a secure architecture where the application is not directly accessible from the internet but can communicate with other resources in the VPC.

The following diagram provides an overview of the resources included in this example. The VPC has public subnets and private subnets in two Availability Zones. Each public subnet contains a NAT gateway and a load balancer node. The servers run in the private subnets, are launched and terminated by using an Auto Scaling group, and receive traffic from the load balancer. The servers can connect to the internet by using the NAT gateway. The servers can connect to Amazon S3 by using a gateway VPC endpoint.



## Features

- **VPC Configuration:** Defines a custom VPC with public and private subnets.
- **Security Groups and NACLs:** Configures network security to control inbound and outbound traffic.
- **Private Subnet App Deployment:** Demonstrates how to deploy an application in a private subnet for enhanced security.

## Prerequisites

Before you begin, ensure you have the following:

- An AWS account.
- Basic understanding of AWS VPC concepts.
- Access to the AWS Management Console.

## Getting Started

```
    1. Open the [AWS Management Console](https://aws.amazon.com/console/).

    2. Navigate to the AWS CloudFormation service.

    3. Create a new stack using the `vpc-template.yml` template provided in this repository.

    4. Follow the on-screen instructions, providing necessary parameters.

    5. Monitor the stack creation progress in the AWS CloudFormation console.
```
## Architecture

The architecture of the VPC setup is as follows:

- **Public Subnet:** Contains resources that need to be publicly accessible, such as a load balancer.
- **Private Subnet:** Hosts application servers that should not be directly exposed to the internet.

[Include a simple diagram of your VPC architecture here]

## Usage

Describe how to access the application, any additional configuration steps, or troubleshooting tips.

## Cleanup

To avoid incurring charges, delete the CloudFormation stack when you are done testing:

```
    1. Navigate to the AWS CloudFormation console.

    2. Select the stack (e.g., MyAppVPCStack).

    3. Click on "Actions" and choose "Delete stack."

    4. Follow the on-screen instructions to delete the stack.
```