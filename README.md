# Creating-a-Manual-AMI-Backup-and-Launching-a-New-EC2-Instance-from-the-Backup-Image-in-AWS
In this task, I created a Manual Amazon Machine Image (AMI) backup of an existing EC2 instance and then launched a new EC2 instance using that AMI.
This process demonstrates how to safely back up an instance, preserve its configuration, and quickly restore or duplicate it when needed.

The purpose of this task was to understand instance recovery, cloning, and backup management in AWS.

##🪜 Steps Performed
🔹 1. Created Manual AMI Backup
![Alt text](https://github.com/Naveen15github/Creating-a-Manual-AMI-Backup-and-Launching-a-New-EC2-Instance-from-the-Backup-Image-in-AWS/blob/5730b4dc51cb73b400db4236b5b3a64d168407c4/Screenshot%20(103).png)

Opened the AWS Management Console and navigated to EC2 → Instances.

Selected the existing instance that I wanted to back up.

Went to Actions → Image and templates → Create image.

Gave a name and description for the AMI (e.g., manual-backup-2025-11-04).

Left “Reboot” option enabled to ensure a consistent image (can be unchecked for no downtime).

Clicked Create image to start the AMI creation process.

Verified the AMI creation under AMIs tab — its state changed from pending to available.

✅ Result: A manual AMI was successfully created, containing the OS, configurations, and root volume snapshot of my EC2 instance.

🔹 2. Launched a New EC2 Instance from AMI
![Alt text](https://github.com/Naveen15github/Creating-a-Manual-AMI-Backup-and-Launching-a-New-EC2-Instance-from-the-Backup-Image-in-AWS/blob/5730b4dc51cb73b400db4236b5b3a64d168407c4/Screenshot%20(103).png)

Navigated to EC2 → AMIs in the AWS Console.

Selected the newly created AMI.

Clicked Launch instance from image.

Chose:

Instance type (e.g., t2.micro)

Existing key pair for SSH access

Default VPC and Subnet

Security Group with SSH/RDP access

Reviewed the configuration and clicked Launch instance.

Once launched, connected to the new instance using:

SSH (for Linux)

RDP (for Windows)

Verified that all configurations and data from the original instance were present.

✅ Result: A new EC2 instance was successfully created and launched from the AMI backup.
![Alt text](https://github.com/Naveen15github/Creating-a-Manual-AMI-Backup-and-Launching-a-New-EC2-Instance-from-the-Backup-Image-in-AWS/blob/5730b4dc51cb73b400db4236b5b3a64d168407c4/Screenshot%20(105).png)
![Alt text](https://github.com/Naveen15github/Creating-a-Manual-AMI-Backup-and-Launching-a-New-EC2-Instance-from-the-Backup-Image-in-AWS/blob/5730b4dc51cb73b400db4236b5b3a64d168407c4/Screenshot%20(106).png)

🧩 Purpose of the Task

To learn how to take a full system backup using AMI.

To understand restoring or cloning instances easily.

To practice disaster recovery and instance replication in AWS.

💡 Key Benefits

Easy recovery if the original instance fails.

Launch identical environments for testing or scaling.

Quick cloning without manual setup.

Reliable backup for production environments.

⚙️ Technologies Used

Amazon Web Services (AWS)

EC2 (Elastic Compute Cloud)

AMI (Amazon Machine Image)

EBS (Elastic Block Store)

🏁 Outcome

This activity helped me understand the backup and restore mechanism in AWS EC2.
By creating an AMI and launching a new instance from it, I learned how to ensure data safety, configuration consistency, and faster recovery for any environment.
