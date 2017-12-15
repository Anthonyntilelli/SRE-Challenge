# ansible_linux_server_challenge

- remove root login for ssh
- set up ansible user account

- Install web server on a Debian, Ubuntu, or CentOS host

- Configure host-based firewall for ports 22, 80 and 443 #possible issue with firewall

- Configure https (a self-signed certificate is acceptable for this challenge)
- Configure http redirect to https

- Configure the http/https homepage to display "SRE CHALLENGE"

- Create an automated test to verify the web server is listening on port 443.

Command to run
ansible-playbook webserver.yml
