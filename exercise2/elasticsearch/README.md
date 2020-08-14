Exercise 2: Basic Linux service setup


Requirements: 

1. ElasticSearch running in a docker container
2. Check the health of ElasticSearch from the command line

Basic package requirement:
1. Ansible
2. Docker


ElasticSearch Container
Steps to install docker:
1. Clone the github repository (https://github.com/satheeskumaraj/experiment.git)
2. Please navigate the folder experiment/exercise2/elasticsearch
3. Run the Ansible_installation.sh script on that machine. (This is for installing ansible on that server)
	** If you are trying to run the remote machine from already installed ansible server then no need to install ansible.
4. Need to install docket by executing the ansible script by using the below command
* ansible-playbook docker_elasticsearch.yml -t docker_install

Steps to create container:
1. Need to create the elasticsearch docket container using ansible.
* ansible-playbook docker_elasticsearch.yml -t elk_container

Note: *** if you need to mentioned particular remote machine the please use that host file while executing the ansible script, look like following command “ansible-playbook docker_elasticsearch.yml -t <tag_name> -i hosts --limits “hostip/group_name” ”
         *** if you run ansible by using password authentication of remote machine then please pass the extra parameter like follow “ -e "ansible_user=#######" -e "ansible_password=########" ”