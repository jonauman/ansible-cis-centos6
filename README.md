# CIS Security check for CentOS 6 with Ansible

## About

This ansible script is used to check security compliance with CIS CentOS Linux 6 Benchmark v1.0.0 found here:

http://benchmarks.cisecurity.org/downloads/show-single/?file=centos6.100

This script has been tested against CentOS 6.4 minimal install with a custom kickstart to enforce compliance.

## Preqrequisites
- ansible
- root access

Ansible can be installed with:

````
 wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
 sudo rpm -Uvh epel-release-6-8.noarch.rpm
 sudo yum update
 sudo yum install ansible
````

## Usage

Checkout this git repo and then cd to that directory.
Run:

`ansible-playbook security.yml`

If all goes well, you will get to the end of the tests. If any test fails, the test will stop there. You can fix the issue and then run it again. All chapters in the Benchmark document are tagged, so if you want to run just one chapter, you can do something like:

`ansible-playbook security.yml -t 1.1` 
