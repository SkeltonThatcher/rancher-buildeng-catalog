# STCL GoCD Agent

### Info:

 This template creates and configure GoCD agent(s).

### Usage:

  Obtain the auto-registration key from config XML in the GoCD server.

  Add the key to the AGENT_AUTO_REGISTER_KEY variable.

  Launch the GoCD agent stack, specifying the gocdio-server service + number of agents required.

### Optional:

   To force agents to run on a different host to the server, specify a service scheduling rule for 'Must not' against the GoCD server 'Container label' value.
