<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** irahimsindhu@gmail.com  
**Email:** irahimsindhu@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/affectionate_olive_majestic_marjoram/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

'm doing this project to learn the basics of setting up a VPC network and get the insights on it to improve my knowledge of this technology.

### What is Amazon VPC?

Amazon VPC is service in amazon which lets you create private,isolated networks on the clound where you can run your EC2 instances. It is useful because it gives you control over IP ranges, subnets, and security so that you can securely manage your cloud infrastructure.

In today's project, I used Amazon VPC to create subnets and attach it to my VPC. Also, I learnt on how to connect my VPC to internet using Internet Gateway.

### Personal reflection

This project took me around 35 minutes to complete including the secret mission.

One thing I didn't expect in this project was how everything was explained in a very easy and clear manner.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will learn on how to create a custom VPC, learing about IPv4 addresses and CIDR.

### How VPCs work

VPCs are a resource that makes sure that everything on the cloud is private to every user. Without VPCs, every file uploaded to the cloud would be available to everyone without any privacy.

### Why there is a default VPC in AWS accounts

The availablity of a default VPC when you create a new AWS account is to allow the user to utilize the other services like AWS Lambda, S3 bucket etc from day 1 without any hassle. If the default VPC was not available, the user would have to learn on how to create a VPC and that would take them some time provided if they didn't have prior knowledge of it.

![Image](http://learn.nextwork.org/affectionate_olive_majestic_marjoram/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a collection/network of IPv4 addresses. IPv4 CIDR have a collection of unique IP addresses belongs to a network and is used for routing and organization.

---

## Subnets

### What I did in this step

In this step, I will be learning on how to create subnets in my custom VPC

### Creating and configuring subnets

Subnets are smaller ranges of IP addresses within a VPC. They help organize resources and control network access. A subnet can be public or private depending on its routing configuration. Each subnet must use a unique, non-overlapping CIDR block within the VPC.

### Public vs private subnets

The difference between public and private subnets are that or a subnet to be considered public, it has to be directly accessible from the internet. A private subnet can only be accessed within the organization or the EC2 instance in which it is created. A public subnet can directly communicate with the internet using an internet gateway while a private subnet does not have direct access to the internet and is typically used for internal access outside of the internet's reach

![Image](http://learn.nextwork.org/affectionate_olive_majestic_marjoram/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

The need to enable this setting is that by default, the subnet is set to private meaning that it can not be accessed from the internet. To allow the access to the subnet via the internet, we have to enable the "auto-assign public IPv4 addresses" that would make the privacy setting of the subnet from private to public.

---

## Internet gateways

### What I did in this step

In this step, I will learn on how to connect my VPC to the internet via a internet gateway to fully implement the theoratical knowledge that I learnt from this project.

### Setting up internet gateways

Internet gateways are the bridge that connects the user's VPC to the mainstream internet.

Attaching an Internet Gateway to a VPC enables resources in the VPC to communicate with the internet, provided they are configured with appropriate routing, public IP addresses, and security rules. Without an Internet Gateway, the VPC cannot directly send or receive traffic from the public internet, effectively isolating it from internet access.

![Image](http://learn.nextwork.org/affectionate_olive_majestic_marjoram/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will launch my VPC in seconds with AWS cloudshell

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which an online shell service sitting directly in AWS from where we can run shell commands to achieve our goals. Wherease, AWS CLI is a command line interface that enables us to directly create,manage or delete our AWS services with the help of specific commands.

### Debugging my setup

I ran into errors because I was not specifying the CIDR correctly.

### Comparing CloudShell vs AWS Console

| Feature | CloudShell | AWS Console |
|----------|------------|-------------|
| Purpose | Provides a browser-based command-line environment for managing AWS resources. | Provides a web-based graphical user interface (GUI) for managing AWS services and resources. |
| Interface | Command Line Interface (CLI). | Graphical User Interface (GUI). |
| Access Method | Accessible directly from the AWS Management Console through a terminal window. | Accessible through a web browser after signing in to AWS. |
| Tools Available | Preinstalled with AWS CLI, SDKs, and common development tools. | Offers dashboards, forms, wizards, and visual monitoring tools. |
| Automation | Well-suited for scripting, automation, and infrastructure management. | Better suited for manual configuration and visual administration. |
| Learning Curve | Requires familiarity with command-line operations and AWS CLI commands. | Easier for beginners due to its visual interface. |
| Resource Management | Enables fast execution of commands across multiple AWS services. | Allows resource management through menus and service-specific pages. |
| File Storage | Includes persistent home directory storage for user files and scripts. | Does not provide a shell environment or persistent command-line workspace. |
| Best Use Cases | Automation, troubleshooting, scripting, and DevOps workflows. | Resource monitoring, configuration, reporting, and general administration. |

#### Summary

- **CloudShell** is ideal for users who prefer command-line operations, automation, and scripting without installing local tools.
- **AWS Console** is ideal for users who prefer a graphical interface for managing, monitoring, and configuring AWS resources.
- Many AWS users leverage **both tools together**: the AWS Console for visualization and management, and CloudShell for advanced operations and automation.

---
