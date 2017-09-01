# STCL-Tech Ubuntu

### Info:

 This custom catalog item presents an STCL-Tech modified installation of Ubuntu for R&D purposes. It provides options for volume mounts to either local, NFS or AWS EBS/EFS.

 Port 22 is mapped for external SSH access.

### Usage:

  Example configuration using EBS

  *(NFS & EFS options follow a similar method)*

  Install the Rancher EBS plugin stack first.

  Using the Rancher storage option, pre-create x1 volume named ubuntu

  Set the volume size and type pairs, e.g:

  ```
  volumeType = gp2
  size = 10
  ```

  Add the Ubuntu stack, selecting rancher-ebs as the volume type.

  *NOTES*

  - SSH ingress is dependent on Rancher host security group rules.

  - For EBS HA (vol re-attach) all Rancher hosts must be launched within the same AZ.
