# SRE Challenge - Ansible script to create a https webserver

## Table of Contents
1. [Challenge](#Challenge)
2. [Files](#Files)
3. [Roles](#Roles)
4. [Requirements](#Requirements)
5. [Author](#Author)

## Challenge:               <a name="Challenge"></a>

  - Install and configure a web server on a Ubuntu  (tested oin Ubuntu 16.4)
  - Configure https using self signed certificate
  - Configure http redirect to https
  - Configure the http/https homepage to display "SRE CHALLENGE"
  - Configure host-based firewall for ports 22, 80 and 443
  - Create an automated test to verify the web server is listening on port 443.

## Files:                 <a name="Files"></a>
  - provision.yml  - playbook attempts to set up requirements, for machine that is unable to run ansible
  - webservers.yml - playbook attempts to set up http server

## Roles                  <a name="Roles"></a>
  - webserver-packages - install needed webserver packages
  - webserver-firewall - sets firewall
  - webserver-https - converts webserver to https and sets webpage
  - check_https - automated test to verify the web server is listening on port 443

## Requirements:          <a name="Requirements"></a>

  - Python for ansible to run (python-apt need for --check)
  - User "ansible" with sudo rights
  - ssh key pair for ssh

#### provision.yml
  - webserver_rsa.pub is required name of ssh key for ansible user
  - To meet industry best practice, it will also prevent root ssh log in
  - -> Recommend reboot after complete <-

## Author:                <a name="Author"></a>
 - Anthony Tilelli
