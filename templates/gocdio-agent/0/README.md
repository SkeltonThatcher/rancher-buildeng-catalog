# STCL-TECH GoCD Agent

### Info:

 This template creates and configures GoCD agent(s).

### Usage:

  Obtain the auto-registration key from config XML in the GoCD server.

  Launch the GoCD agent stack, specifying the gocdio-server service, the number of agents required, and inputting the registration key.

### Optional:

   To force agents to run on a different host to the server, specify a service scheduling rule for 'Must not' against the GoCD server 'Service with name' value.
