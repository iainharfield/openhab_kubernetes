# openhab_kubernetes
Get openhab working on microk8s - basic config

Note:
Using Ubuntu 22.04 and in  .bash_aliases I have set:
- alias kubectl='microk8s kubectl'


To get OpenHab running in a Pod, execute the following commands below.  It won't for anyone else as-is as I've hard coded the openhab volume mappings to my nodes home folder.  You'll need to edit openhab-pod.yml "volumes" to point to right folder.  Something for another day - still early learning days for me.

1. kubectl create -f create-namespace.yml
2. kubectl create -f openhab-pod.yml 
3. kubectl create -f openhab-nodeport.yml

With this basic config,  you should be able to access the volumes and openhab UI on:  _yournodeip:30008_
