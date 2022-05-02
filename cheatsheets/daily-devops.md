
# EC2 

- A Linux-based/Windows-based/Mac-based virtual server that you can provision.

- You are limited to running On-Demand Instances per your vCPU-based On-Demand Instance limit, purchasing 20 Reserved Instances, and requesting Spot Instances per your dynamic Spot limit per region.

- The AWS Nitro System is the underlying platform of the next generation of EC2 instances. Traditionally, hypervisors protect the physical hardware and bios, virtualize the CPU, storage, networking, and provide a rich set of management capabilities. With the Nitro System, these functions are offloaded to dedicated hardware and software, thereby reducing costs of your instances in the process. Hence, the Nitro Hypervisor delivers performance that is indistinguishable from bare metal and performs better than its predecessor: the Xen Hypervisor.

- Server environments called instances.

- Package OS and additional installations in a reusable template called Amazon Machine Images.

- Various configurations of CPU, memory, storage, and networking capacity for your instances, known as instance types
t-type and m-type for general purpose
c-type for compute optimized
r-type, x-type and z-type for memory optimized
d-type, h-type and i-type for storage optimized
f-type, g-type and p-type for accelerated computing

- Secure login information for your instances using key pairs
 
- Storage volumes for temporary data that are deleted when you STOP or TERMINATE your instance, known as instance store volumes. Take note that you can stop an EBS-backed instance but not an Instance Store-backed instance. You can only either start or terminate an Instance Store-backed instance.

- Persistent storage volumes for your data using Elastic Block Store volumes (see aws storage services).

- Multiple physical locations for deploying your resources, such as instances and EBS volumes, known as regions and Availability Zones (see AWS overview).

- A firewall that enables you to specify the protocols, ports, and source IP ranges that can reach your instances using security groups (see aws networking and content delivery).

- Static IPv4 addresses for dynamic cloud computing, known as Elastic IP addresses (see aws networking and content delivery).

- Metadata, known as tags, that you can create and assign to your EC2 resources

- Virtual networks you can create that are logically isolated from the rest of the AWS cloud, and that you can optionally connect to your own network, known as virtual private clouds or VPCs (see aws networking and content delivery).

- Add a script that will be run on instance boot called user-data.

- Host Recovery for Amazon EC2 automatically restarts your instances on a new host in the event of an unexpected hardware failure on a Dedicated Host.

- EC2 Hibernation is available for On-Demand and Reserved Instances running on freshly launched M3, M4, M5, C3, C4, C5, R3, R4, and R5 instances running Amazon Linux and Ubuntu 18.04 LTS. You can enable hibernation for your EBS-backed instances at launch. You can then hibernate and resume your instances through the AWS Management Console, or though the AWS SDK and CLI using the existing stop-instances and start-instances commands. Hibernation requires an EC2 instance to be an encrypted EBS-backed instance.

## Instance states

- Start – run your instance normally. You are continuously billed while your instance is running.

- Stop – is just a normal instance shutdown. You may restart it again anytime. All EBS volumes remain attached, but data in instance store volumes are deleted. You won’t be charged for usage while instance is stopped. You can attach or detach EBS volumes. You can also create an AMI from the instance, and change the kernel, RAM disk, and instance type while in this state.

- Hibernate – When an instance is hibernated, it writes the in-memory state to a file in the root EBS volume and then shuts itself down. The AMI used to launch the instance must be encrypted, and also the root EBS volume of the instance. The encryption ensures proper protection for sensitive data when it is copied from memory to the EBS volume. While the instance is in hibernation, you pay only for the EBS volumes and Elastic IP Addresses attached to it; there are no hourly charges.

- Terminate – instance performs a normal shutdown and gets deleted. You won’t be able to restart an instance once you terminate it. The root device volume is deleted by default, but any attached EBS volumes are preserved by default. Data in instance store volumes are deleted.

- To prevent accidental termination, enable termination protection.

## Root Device Volumes

- The root device volume contains the image used to boot the instance.

- Instance Store-backed Instances
Any data on the instance store volumes is deleted when the instance is terminated (instance store-backed instances do not support the Stop action) or if it fails (such as if an underlying drive has issues).
You should also back up critical data from your instance store volumes to persistent storage on a regular basis.

- Amazon EBS-backed Instances
An Amazon EBS-backed instance can be stopped and later restarted without affecting data stored in the attached volumes.
When in a stopped state, you can modify the properties of the instance, change its size, or update the kernel it is using, or you can attach your root volume to a different running instance for debugging or any other purpose.
By default, the root device volume for an AMI backed by Amazon EBS is deleted when the instance terminates.
Previously, to launch an encrypted EBS-backed EC2 instance from an unencrypted AMI, you would first need to create an encrypted copy of the AMI and use that to launch the EC2 instance. Now, you can launch encrypted EBS-backed EC2 instances from unencrypted AMIs directly.

