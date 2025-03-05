# Dynamic Website Deployment on AWS

## Overview
This project demonstrates the deployment of a dynamic website on AWS using various AWS services. The infrastructure is designed with high availability, security, and scalability in mind. The GitHub repository contains deployment scripts and a reference architecture diagram.

## AWS Services Utilized

1. **Virtual Private Cloud (VPC)**: Configured with public and private subnets spanning two availability zones to enhance fault tolerance.
2. **Internet Gateway**: Enables internet connectivity for resources within the VPC.
3. **Security Groups**: Serve as a network firewall to control inbound and outbound traffic.
4. **Availability Zones**: Used two availability zones to improve system reliability.
5. **Public Subnets**:
   - Used for infrastructure components like the NAT Gateway and Application Load Balancer.
6. **EC2 Instance Connect Endpoint**: Securely connects to assets within public and private subnets.
7. **Private Subnets**:
   - Hosted web servers (EC2 instances) in private subnets for enhanced security.
   - Allowed instances in the private Application and Data subnets to access the internet via the NAT Gateway.
8. **EC2 Instances**:
   - Hosted the website on EC2 instances.
9. **Application Load Balancer (ALB)**:
   - Configured with a target group to distribute web traffic evenly to an Auto Scaling Group across multiple availability zones.
10. **Auto Scaling Group**:
    - Automatically manages EC2 instances to ensure availability, scalability, fault tolerance, and elasticity.
11. **AWS Certificate Manager**:
    - Secured application communications using SSL/TLS certificates.
12. **Amazon Simple Notification Service (SNS)**:
    - Configured to send alerts related to activities within the Auto Scaling Group.
13. **Route 53**:
    - Registered the domain and set up a DNS record.
14. **Amazon S3**:
    - Used to store application code.

## Repository Contents
- **Deployment Scripts**: Includes infrastructure as code (IaC) scripts for automated resource provisioning.
- **Reference Diagram**: Illustrates the architecture and resource relationships.

## Deployment Steps
1. Clone the GitHub repository.
2. Use Terraform or AWS CloudFormation to deploy the infrastructure.
3. Ensure proper security group configurations for restricted access.
4. Deploy the website on the provisioned EC2 instances.
5. Configure Route 53 DNS settings for domain name resolution.
6. Verify the Application Load Balancer distributes traffic correctly.
7. Set up monitoring and alerting using SNS.

## Security Considerations
- Web servers are placed in private subnets to minimize exposure.
- Security Groups enforce least privilege access.
- SSL/TLS encryption ensures secure communication.
- NAT Gateway allows internet access while maintaining security controls.

## Conclusion
This AWS-based deployment ensures a secure, scalable, and highly available dynamic website. The infrastructure is designed to handle varying loads while maintaining security best practices.

For more details, refer to the deployment scripts and reference diagram in the GitHub repository.

