# STCL-Tech Artifactory Pro

### Info:

 This custom catalog item presents an STCL-Tech modified installation of Artifactory Pro for Docker using the [official Artifactory Pro image](https://bintray.com/jfrog/artifactory-pro). It offers volume options via a Busybox sidekick for /var/opt/jfrog/artifactory to either local, NFS or AWS EBS/EFS mounts.

### Usage:

  Example configuration using EBS

  *(NFS & EFS options follow a similar method)*

  Install the Rancher EBS plugin stack first.

  Using the Rancher storage option, pre-create a volume named artifactory

  Set the volume size and type keypairs:

  ```
  volumeType = gp2
  size = 10
  ```

  Add the Artifactory Pro stack, selecting rancher-ebs as the volume type.

  Once launched, the Artifactory Pro UI will be available at http://<HOST_IP_OR_DNS_NAME>:8081

  *NOTES*

  - UI access is dependent on host security group rules.

  - For EBS HA (vol re-attach) all Rancher hosts must be launched within the same AZ.
