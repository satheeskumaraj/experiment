Create a script which outputs basic metrics of the machines.

In this repo, I have created some script to monitor our instance. Please navigate the folder experiment/exercise1/metrics/

1. If you want the metrics from local machine & ansible not there on that machine. Then please run the Ansible_installation.sh.
2. Once Ansible installed on that server, We need some softwere to get the basic system monitoring like CPU usage, Disk Uasge and Network Usage. So please execute the below command. ansible-playbook Monitoring_Package.yml
3. After install required packages, Please execute below command to get the metrics date. 
    ansible-playbook Monitoring_Metrics.yml

    
Note: if you are trying to get the metrics from differnt server the you need to create one inventory file and that inventory you need to mentioned all the ip's look like below example

File : Azure_VM/vm_metrics/inventory

Content of the file will be

[metricsip] 
10.0.1.5 
10.0.1.4

How to execute the metrics ansible script?

1. If you're going to connect remote hosts by using username & password then please use the below command. ansible-playbook Monitoring_Metrics.yml -i inventory -e "ansible_user=########" -e "ansible_password=#########"
2. If it's password less authentication the use simple below one. ansible-playbook Monitoring_Metrics.yml -i inventory1