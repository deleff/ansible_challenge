# Part 1:
## Create an AWS security group,an EC2 instance, and assign the security group to it
 
1. cd launch_ec2_with_security_group
2. Edit the variables file, and enter the relevant info (launch_ec2_with_security_group/roles/ec2_security/vars/main.yml)
3. Run the role (no need to worry about the hosts, since you will be creating a new instance, it uses "localhost"): 
     ansible-playbook launch_ec2_with_security_group.yml -i hosts

# Part 2:
## Provision an NGINX server

1. cd ansible_webserver
2. make sure the EC2 instance you created in part 1 has been added to your inventory
3. Run the role (no need to worry about variables):
     ansible-playbook ansible_webserver.yml -i hosts

Congratulations, you created and provisioned a thing.
Now go view the webpage you just created on the EC2 instance you made.
