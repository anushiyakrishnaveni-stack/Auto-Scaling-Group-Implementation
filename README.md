**AWS Auto Scaling Group (ASG) Implementation**


**📌 Project Overview**
This project demonstrates the setup of a highly available and scalable architecture on AWS. By leveraging Auto Scaling Groups and an Application Load Balancer, the infrastructure automatically scales in or out based on real-time demand, ensuring application performance and cost efficiency.

**🏗 Architecture**
The setup follows AWS best practices for high availability:

**VPC: **Custom VPC with Public and Private subnets across two Availability Zones.

**Application Load Balancer (ALB):** Routes incoming traffic to the EC2 instances.

**Auto Scaling Group:** Manages the lifecycle of EC2 instances.

**CloudWatch:** Monitors metrics to trigger scaling events.

**🚀 Features**
**Self-Healing:** Automatically detects and replaces failed instances.

**Elasticity:** Scales capacity up during peak hours and down during low traffic.

**Load Balancing:** Evenly distributes traffic to prevent bottlenecks.

**Security:** Instances are placed in private subnets with restricted Security Groups.

**🛠 Prerequisites**
An active AWS Account.

Basic knowledge of EC2 and VPC.

(Optional) AWS CLI configured for scripted deployment.

**📖 Step-by-Step Setup**
**Create a Launch Template:** Define the AMI (Amazon Linux 2), Instance Type (t2.micro), and User Data scripts.

**Configure Target Group:** Set up a target group for the ALB to route traffic to.

**Deploy Application Load Balancer:** Create an internet-facing ALB.

**Create Auto Scaling Group:**  Select the Launch Template.

Set Desired, Minimum, and Maximum capacity.

Attach to the ALB Target Group.

**Define Scaling Policies:** Use Target Tracking (e.g., maintain 50% average CPU utilization).

**🧪 Testing**
**Stress Test:** Run a load test on the instances to observe the ASG triggering a "Scale Out" event.

**Termination Test:** Manually terminate an instance to verify the ASG automatically launches a replacement.
