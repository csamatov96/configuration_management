IAM User with the required permission.
Boto installed. (Ansible uses the Boto Python library to handle AWS management)

first i created an AWS VPC Role by using the following command: ansible-galaxy init aws-vpc
we will be using the two files below from our aws-vpc role.
- tasks
   - main.yml
- vars
   -main.yml

We will place the variables in the vars/main.yml file. This allows the role to be easily reusable. Modify the variables depending on your requirement but replace your AWS Access and Secret key.

VPC will include the following components.

VPC
Subnet
Router
IGW (Internet Gateway)
Security Group
EC2 Instance
We will write all the code below in the tasks/main.yml file.




mv aws-vpc role to /etc/ansible/roles directory
mv test.yml file to /etc/ansible directory
Execute the following commands to set up your AWS credentials as an environment variables. The playbook will need these at runtime, or u can provide them in /etc/ansible/roles/aws-vpc/tasks/mail.yml
export AWS_ACCESS_KEY_ID=<replace your key>
export AWS_SECRET_ACCESS_KEY=<replace your secret>
Execute the following command to run the ansible playbook from the directory that contains the playbook: ansible-playbook first_task.yml 

