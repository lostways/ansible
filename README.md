# ansible
ansible scripts

## Setup
Install packages
`pip install -r requirements.txt`


## Usage
```bash
ansible-playbook -i hosts site.yml -e "deploy_ssh_key='$(cat ~/.ssh/deploy_key.pub)'"
```

Or run individual roles:
```bash
ansible-playbook -i hosts site.yml --tags "initial-setup"
ansible-playbook -i hosts site.yml --tags "user-setup" -e "username=myuser"
ansible-playbook -i hosts site.yml --tags "deploy-setup" -e "deploy_ssh_key='$(cat
~/.ssh/deploy_key.pub)'"
```
