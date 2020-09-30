## port_scan

### Description
Playbook scans provided hosts for open ports in range 0..65535 using nmap. On success scan, xml report will be generated and could be viewed in browser

### Usage
1. Install Ansible
2. Create `ip_list.txt` file if you want to scan your own set of IPs (see ip_list.txt.example). Otherwise, make sure you are logged in the AWS:
```
$ aws iam get-login-profile --user-name YOUR_IAM_USER
```
3. Run playbook
```
$ ansible-playbook main.yml
```
or
```
$ ansible-playbook main.yml -e 'public_ip_addresses=127.0.0.1,127.0.0.2,127.0.0.3'
```