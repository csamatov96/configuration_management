mv aws-vpc role to /etc/ansible/roles directory
mv test.yml file to /etc/ansible directory
Execute the following commands to set up your AWS credentials as an environment variables. The playbook will need these at runtime, or u can provide them in /etc/ansible/roles/aws-vpc/tasks/mail.yml
export AWS_ACCESS_KEY_ID=<replace your key>
export AWS_SECRET_ACCESS_KEY=<replace your secret>
Execute the following command to run the ansible playbook from the directory that contains the playbook: ansible-playbook first_task.yml 

