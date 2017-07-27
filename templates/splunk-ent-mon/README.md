# STCL-Tech Splunk Enterprise Monitor

### Info:

 This custom catalog item presents an STCL-Tech modified installation of Splunk Enterprise Monitor for Docker using the [official Splunk image](https://hub.docker.com/r/splunk/splunk/)

 The stack utilises an AWS EBS volume for /opt/splunk.

### Usage:

 First install the Rancher EBS stack plugin.

 Using the Rancher storage option, create an EBS volume named splunkebs.

 Set the volume size (in GB) and type pairs, e.g:

 ```
 volumeType = gp2
 size = 10
 ```
 Launch the Splunk Enterprise Monitor stack.

 The Splunk Enterprise Monitor UI will be available at http://<HOST_IP>:8000

 *NOTE* UI access is dependent on related EC2 security group rules for the Rancher hosts
