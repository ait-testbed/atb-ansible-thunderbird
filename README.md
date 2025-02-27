# Ansible role for Thunderbird

This role installs Thunderbird and optionally generates dummy emails in the users thunderbird profile.

# Requirements
- Ubuntu



# Usage

Simply put this role to the "roles"-folder and use the following playbook.yml:
```
- hosts: localhost
  become: true
  roles:
    - atb-ansible-thunderbird
```


# Role Variables
```
thunderbird_user: Joe
```

thunderbird profile will be created in this users home directory

```
populate_emails: true
```
if true, generates an mbox file with dummy emails in /home/{{ thunderbird_user }}/.thunderbird/user.default-release/Mail/Local Folders/Inbox
