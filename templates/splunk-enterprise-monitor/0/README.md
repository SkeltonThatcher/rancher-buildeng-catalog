# STCL-Tech Splunk Enterprise Monitor

### Info:

 This custom catalog item presents an STCL-Tech modified installation of Splunk Enterprise Monitor for Docker using the [official Splunk image](https://hub.docker.com/r/splunk/splunk/). It utilises EBS volumes via a Busybox sidekick for /opt/splunk/etc and /opt/splunk/var data.

 The image comes with some data inputs activated (e.g., file monitor of docker host JSON logs, HTTP Event Collector, Syslog, etc.). It also includes the Docker app which has dashboards to help you analyze collected logs and docker information such as stats, events, tops, and inspect from your running images.

### Usage:

  Install the Rancher EBS plugin stack first.

  Using the Rancher storage option, pre-create x2 volumes named splunk_etc and splunk_var

  Set the volume size and type pairs, e.g:

  ```
  volumeType = gp2
  size = 10
  ```

  Add the Splunk Enterprise Monitor stack.

  Once launched, the Splunk Enterprise Monitor UI will be available at http://<HOST_IP_OR_DNS_NAME>:8000

  *NOTE*
  
  The Splunk UI and services ingress are dependent on Rancher host security group rules.
