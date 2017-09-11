# STCL-TECH GoCD server

### Info:

 Creates and configures a GoCD server instance with options for a /godata HA volume (NFS or AWS EBS/EFS)

### Usage:

 Example configuration using EBS

 *(NFS & EFS options follow a similar method)*

 Install the Rancher EBS plugin stack first.

 Using the Rancher storage option, create an EBS volume named godata.

 Set the volume size and type pairs, e.g:

 ```
 volumeType = gp2
 size = 10
 ```

 Launch the stack, choosing rancher-ebs as the volume driver.

 The GoCD server will be available at http://<HOST_IP>:8153

 *NOTES*

 - Access is dependent on Rancher host security group rules.

 - For EBS HA (vol re-attach) all Rancher hosts must be launched within the same AZ.

 - JVM options are fixed at default, e.g:

  ```
  Xms512m
  Xmx1024m
  ```

### Optional:

   Install the Rancher AWS Route 53 plugin to provide DNS HA in the event of a host or service failure.

   Once installed, create a Route 53 CNAME entry to the dynamic A record for the GoCD server service.
