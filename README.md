# Dynamic-Inventory-of-aws-for-Ansible

Requirment: python3 need tobe available in your system
------------------------------------------------------------------
Step 1: Download both given files "ec2.ini" and "ec2.py" and
        save them in a same folder.

------------------------------------------------------------------
Step 2: Give executable permission to "ec2.py" file.
```
[ ]# chmod +x ec2.py 
```

-----------------------------------------------------------------
Step 3: Install "ansible, boto, boto3" python library.
```
[ ]# pip3 install ansible
[ ]# pip3 install boto
[ ]# pip3 install boto3
```
-------------------------------------------------------------------------
Step 4: Go to ansible config file and update the inventory location
        in (step 1) we download files and saved them in folder
        get the location of folder and update in the ansible config. file
```
[ ]# vim /etc/ansible/ansible.cfg

[defaults]
inventory=/path_of_folder_where_we_saved_"ec2.ini"_"ec2.py"_files
```

--------------------------------------------------------------------------
Step 4: Create shell varibale
```
[ ]# export AWS_ACCESS_KEY_ID='paste_access_key_of_your_aws_iam_user'

[ ]# export AWS_SECRET_ACCESS_KEY='paste_secret_key_of_your_aws_iam_user'

[ ]# export AWS_REGION='ap-south-1'
```
Note: in place of "ap-south-1" you can give your required region

--------------------------------------------------------------------------
Step 5:

Now go and launch any instance on AWS 
and come to ansible system
run the below given command to check the ip-address of ec2 instance.
```
[ ]# ansible all --list-host
```

