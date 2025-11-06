# Must-Gater and SOS report

## Must-Gather (example for perfomrance issues)

1) ### We want to see all nodes ready
omc get nodes

2) ### search for Conditions Tab (Pressure)
omc describe node | less 

3) ### Check events for namespace, search for context dedline exceeded,  Readinness probe failed, Liveness probe failed,

omc get events -n <namesspace> 
### pods retarts
omc get po

4) ### pod logs
omc log pod/<pod name> -n <namespace> -c <container>

### SOS Report

xsos sos-report -py  
xsos sos-report -my  
xsos sos-report -dy  


2) ### SOS COmmands
sos_commands/openshift/  
sos_commands/crio/  
sos_commands/logs/  

3) ### kubelet.service - no pager boot
in folder opneshift - kubelet

4) ### cat
cat sos_commands/networkmanager/nmcli_con  
grep -i "oom-kill\|out of memory" sos_commands/kernel/dmesg_-T

