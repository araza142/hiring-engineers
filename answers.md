# Solved exercise for the role 'Solutions Engineer' at [Datadog](http://datadog.com)

## Candidate Information
Ali Raza  
alirazaonsite@gmail.com

### Level 0 (optional) - Setup an Ubuntu VM
* New Ubuntu VM has been setup on AWS cloud:  
![Ubuntu_VM_AWS](images/Level0_1.png)

### Level 1 - Collecting your Data
* Sign up and install local agent
Signed up for DataDog:  
![DataDog_SignedUp](images/Level1_1a.png)

Locate remote agent:
![DataDog_RemoteAgent_Setup](images/Level1_1b.png)

Install remote agent:
To install agent run following commands:
```bash
DD_API_KEY=xxx-xxx bash -c "$(curl -L https://raw.githubusercontent.com/DataDog/dd-agent/master/packaging/datadog-agent/source/install_agent.sh)"
```
Where DD_API_KEY is the unique key we retrieved from DataDog portal.

Ensure it is running:
![DataDog_RemoteAgent_Status](images/Level1_1c.png)
Alternatively, you can start, stop and check the status of datadog agent by running:
```bash
service datadog-agent start | stop | status
```

* What is the Agent?
In this context, agent is a piece of software which collects data generated from alerts, triggers, events, etc and send to remote server which in this case is DataDog server (endpoint). Agent runs in background and can also be setup as a service and set to start automatically so that upon reboot of machine, agent starts itself.
