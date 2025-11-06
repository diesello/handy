# Must-Gater and SOS report

## Must-Gather (example for perfomrance issues)

###We want to see all nodes ready
omc get nodes

### search for Conditions Tab (Pressure)
omc describe node | less 

### Check events for namespace, search for context dedline exceeded,  Readinness probe failed, Liveness probe failed,

omc get events -n <namesspace> 
### pods retarts
omc get po

###pod logs
omc log pod/<pod name> -n <namespace> -c <container>

### SOS Report

xsos sos-report -py
xsos sos-report -my
xsos sos-report -gy 


###
sos_commands/crio/
sos_commands/logs/

### kubelet.service - no pager boot
in folder opneshift - kubelet