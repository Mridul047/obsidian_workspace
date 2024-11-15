* Elastic Block Storage consist of collection of blocks.
* Each block has a unique identifier.
* These blocks can be stored in diff. physical devices.
* Blocks can be presented as volumes which can be used as file system or hard-drive which can be used to boot OS.
	* ![[Pasted image 20241007101325.png]]
* EBS are separate from EC2 instances. These can be attached to EC2 instances. Detach it and attach to another EC2 instance. The data will not be lost.
* ![[Pasted image 20241007101637.png]]
* EBS are present with in an  AZ.
	* ![[Pasted image 20241007101755.png]]
* EBS & EC2 instance should be in same AZ in order to work together.
	* ![[Pasted image 20241007102001.png]]
* Snapshots stored in S3 can be used to move data in EBS in AZ-1 to AZ-2.:
	* ![[Pasted image 20241007102200.png]]
* Copying data across regions:
	* ![[Pasted image 20241008095254.png]]
* EBS Volume Types:
	* ![[Pasted image 20241103183602.png]]
	* General purpose SSD:
		* ![[Pasted image 20241103183723.png]]
		* Use SSD in background.
		* Great for transactional workloads. eg: VM, DB, Dev/Test Env.
		* Recommended for most of the workloads.
		* GP3:
			* Latest gen. lowest cost volumes.
			* Enables scaling vol. performance independent of vol. size.
			* 20% lower cost as compared to gp2.
		* GP2:
			* Default vol. types for EC2 instance.
			* Performance scales with vol. size.
	* Provisioned IOPS SSD:
		* ![[Pasted image 20241103184359.png]]
		* These types of EBS are designed for IO intensive workloads. Eg. DB.
		* 
		* Types:![[Pasted image 20241103184446.png]]
	* HDD based volumes:
		* Uses hard drive in background.
		* Types:
			* ![[Pasted image 20241103185209.png]]
	* Magnetic Volumes:
		* ![[Pasted image 20241103185427.png]]
* EBS Pricing:
	* ![[Pasted image 20241103185552.png]]

## Summary:

* ![[Pasted image 20241103185642.png]]
* ![[Pasted image 20241103185701.png]]