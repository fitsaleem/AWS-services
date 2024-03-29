# class 4

# AWS Auto Scaling:

Auto Scaling is a feature of Amazon Web Services (AWS) that allows you to automatically adjust the number of EC2 instances in response to changing demand. It ensures that you have the correct number of Amazon EC2 instances available to handle the load for your application.

Here are some key points about Auto Scaling in AWS:

1. **Scalability**: Auto Scaling enables you to scale your Amazon EC2 capacity up or down automatically according to conditions you define. To use Auto Scaling, you create collections of EC2 instances, called Auto Scaling groups.

2. **Flexibility**: With Auto Scaling, you can ensure that you have the right amount of compute power to meet the demands of your application. You can configure scaling policies to increase or decrease the number of instances during specific times or in response to certain conditions.

3. **Cost Efficiency**: By automatically adjusting the number of instances, Auto Scaling helps you save money. When demand is low, you can reduce the number of instances to minimize costs. When demand increases, Auto Scaling can quickly launch additional instances to handle the increased load.

4. **High Availability**: Auto Scaling helps ensure high availability for your applications. If an instance becomes unhealthy, Auto Scaling can terminate the instance and launch a new one.

5. **Integration with other AWS services**: Auto Scaling works seamlessly with other AWS services such as Elastic Load Balancing, Amazon CloudWatch, and Amazon SNS.

6. **Ease of Management**: With Auto Scaling, you can manage your EC2 instances without worrying about capacity planning. You can easily add or remove instances as needed.

Remember, while Auto Scaling can help you maintain steady, predictable performance at the lowest possible cost, it's not a silver bullet. You still need to design your application to be stateless and to store session data in a centralized datastore.

# AWS thresholds and CloudWatch:

In AWS, thresholds are used in conjunction with Amazon CloudWatch to monitor and respond to changes in your AWS resources. They are part of the scaling policies that determine when to scale out (increase capacity) or scale in (decrease capacity).

CloudWatch is a monitoring service for AWS resources and the applications you run on AWS. You can use CloudWatch to collect and track metrics, collect and monitor log files, set alarms, and automatically react to changes in your AWS resources.

Here's how thresholds and CloudWatch work together:

1. **Define Metrics**: First, you define what metrics you want to monitor. These could be CPU utilization, network traffic, disk usage, etc.

2. **Set Thresholds**: Next, you set thresholds for these metrics. For example, you might set a threshold for CPU utilization above 70%.

3. **Create Alarms**: Then, you create alarms in CloudWatch based on these thresholds. An alarm watches a single metric over a specified time period, and performs one or more actions based on the value of the metric relative to a threshold you define.

4. **Configure Auto Scaling Policies**: Finally, you configure your Auto Scaling group to respond to these alarms. For example, you might set a policy to add instances when the CPU utilization exceeds 70%, and another policy to remove instances when the CPU utilization drops below 30%.

This way, CloudWatch and Auto Scaling work together to ensure that your application scales appropriately based on real-time demand.

# digram of auto scaling:

![aws-auto-scaling-elb](https://jayendrapatil.com/wp-content/uploads/2016/06/Screen-Shot-2016-06-07-at-4.13.10-PM.png)

# Amazon Elastic Block Store (EBS) 

Amazon Elastic Block Store (EBS) provides raw block-level storage that can be attached to Amazon EC2 instances and is used as primary storage for instances. Each EBS volume is automatically replicated within its Availability Zone to protect you from component failure.

Here are some key features of Amazon EBS:

1. **Durability and Performance**: Amazon EBS volumes are designed to provide consistent and low-latency performance. They are built on solid-state drives (SSD) and hard disk drives (HDD) to deliver millions of IOPS and throughput.

2. **Data Persistence**: Data on EBS volumes persists independently from the life of the instance. This means that even if you stop or terminate an instance, the data on the EBS volume remains intact.

3. **Volume Types**: Amazon EBS offers several types of volumes optimized to different use cases including General Purpose SSD (gp2), Provisioned IOPS SSD (io1), Throughput Optimized HDD (st1), Cold HDD (sc1), and Magnetic (standard).

4. **Snapshotting**: You can create snapshots of your EBS volumes, which are point-in-time copies of your data. Snapshots are stored in Amazon S3 and can be used to create new volumes or to restore your data to a previous state.

5. **Encryption**: Amazon EBS supports encryption of data at rest. You can encrypt your EBS volumes using keys managed by AWS Key Management Service (KMS).

6. **Backups**: Amazon EBS does not automatically backup your data. You should regularly back up your data to Amazon S3 or another storage service.

Remember, while EBS volumes are highly durable, they are not designed to be used as a primary database storage solution. For databases, consider using Amazon RDS or DynamoDB.