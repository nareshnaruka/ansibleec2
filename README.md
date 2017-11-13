#Q2.
#Write an ansible playbook to create and instance that can store items in S3.

Assumptions: 
     A. Roles, which has S3 Access has been created.
     B. Private Key has been already created
     C. Security Group has been created allowing access to port 22.

Steps
1. Update file variables.sh with details of AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY.
   The IAM User created should have EC2 Instance Creation access priviledges.
2. Update all the variables in file ansibleec2/group_vars/all file, the variable to be updated are security_group, key_name and IamProfile
3. Update file ansibleec2/roles/launch/tasks/main.yml with absolute location of file ec2.py. 
4. Source the env file variable.sh by executing command ". ./variable.sh"
5. Execute playbook by executing command "ansible-playbook site.yml
