# STCL GoCD server

### Info:

 This template creates and configures a GoCD server instance with data HA.

 It utilises an AWS EC2 EBS volume for /godata.

### Usage:

 Install the Rancher EBS plugin.

 Using the Rancher EBS plugin, create an EBS volume named ebs.

 Launch the GoCD server stack.

 The GoCD server will be available at http://<HOST_IP>:8153

### Optional:

 To provide DNS HA in the event of a host or service failure.

 Install the Rancher AWS Route 53 plugin.

 Create a Route 53 CNAME entry to the dynamic A record for the GoCD server service.
