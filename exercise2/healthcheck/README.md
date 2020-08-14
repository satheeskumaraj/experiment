Exercise 2: Basic Linux service setup


Requirements: 

1. ElasticSearch running in a docker container
2. Check the health of ElasticSearch from the command line

Basic package requirement:
1. Ansible
2. Docker

ElasticSearch container health status:
1. Clone the github repository (https://github.com/satheeskumaraj/experiment.git)
2. Please navigate the folder experiment/exercise2/healthcheck
* ansible-playbook docker_elasticsearch.yml -t elk_health_check


Note: *** if you need to mentioned particular remote machine the please use that host file while executing the ansible script, look like following command “ansible-playbook docker_elasticsearch.yml -t <tag_name> -i hosts --limits “hostip/group_name” ”
         *** if you run ansible by using password authentication of remote machine then please pass the extra parameter like follow “ -e "ansible_user=#######" -e "ansible_password=########" ”