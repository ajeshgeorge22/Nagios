***********************************************************************************************
# This ansible  roles will help you to configure a nagios server and nagios client

# Step to setup nagios server
# Requirement
# OS: Ubuntu 14 or 16
1. Please provide the host ip address and ssh user and password. Also for root permission give sudo  user and password.
2. Please update nagios admin email id in nagios-server-install/defaults/main.yml 
3. run ansible-playbook -i hosts nagios-server.yml
4. The nagios server will be configured in the specifed server and the  console will be available at http://ip/nagios

# Step to setup nagios client
# Two roles are used for configuring client and setup the client data in nagios server
1. Add the client ip address and ssh user and password. Also for root permission give sudo  user and password.
2. Add the nagios server IP in nagios-client-install/defaults/main.yml
3. run the ansible-playbook -i hosts nagios-client-install.yml
# To add the client host check detail in server
1. check the nagios server ip nad user is specified in hosts
2. run ansible-playbook -i hosts nagios-host-setup.yml

