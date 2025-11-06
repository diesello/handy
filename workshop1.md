1) Install Homebrew - ref: brew.sh

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

 
2) Install xsos - ref: https://github.com/ryran/xsos

sudo curl -Lo /usr/local/bin/xsos https://raw.githubusercontent.com/ryran/xsos/master/xsos
sudo chmod +x /usr/local/bin/xsos

3) Install gollowing apps
brew install bash coreutils gawk 

4) add to you .bashrc


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

## SOS Report
1) ### xsos commands
xsos sos-report -py  
xsos sos-report -my  
xsos sos-report -dy  


2) ### SOS Commands
sos_commands/openshift/  
sos_commands/crio/  
sos_commands/logs/  

3) ### kubelet.service - no pager boot
in folder opneshift - kubelet

4) ### cat
cat sos_commands/networkmanager/nmcli_con  
grep -i "oom-kill\|out of memory" sos_commands/kernel/dmesg_-T

