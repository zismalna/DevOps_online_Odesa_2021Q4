# AWS

Provisioning and instance with Amazon Lightsail and logging into it:

![Lightsail](./images/lightsail.png "Lightsail instance")

Launching EC2 instance without Amazon Lightsail and taking a snapshot:

![EC2 instance](./images/ec2.png "EC2")
![Snapshot](./images/snap.png "Snapshot")

Created an EBS volume and atached in to the instance. Mounted on the filesystem and created some files:

![Disk_D](./images/ebs1.png "Disk_D")

Spun up another instance from the snapshot taken earlier:

![Restored from snapshot](./images/third.png "Third instance")

Attached the volume detached from the last instance and made sure the files are there:

![Files](./images/still_there.png "Still there")

Created an S3 bucket and uploaded my files there.
Hosted a static website available at zismalna.com (redirect).
