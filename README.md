# Moneybags's playground

### Welcome to my playground

This repo contains playbooks that I use for my home infrastructure. Feel free to use them, just make sure you have a folder for your inventory file.

### Important

Please note that if your using my `linux_initialsetup` playbook you'll need to make sure that you have added the public ssh keys of your hosts to your known_hosts file. You can do this by running the following commands (I add the IP address of the host as well just in case my internal DNS server stops working):

Please ensure that you have sshpass installed as some of my playbooks require this.

```bash
ssh-keyscan -H hostname >> ~/.ssh/known_hosts
ssh-keyscan -H ipaddress >> ~/.ssh/known_hosts
```

`linux_ubuntu_setup_base.yml` - Used for configuring a fresh Ubuntu install. If you're using Zabbix then you can uncomment the lines relating to Zabbix.
`linux_general_check.yml` - Used for configuring existing VMs.

To execute a playbook run

```
ansible-playbook -i ~/playgound/inventory -u <yourusername> -k -K ~/playgound/<file>.yml
```

Feel free to comment or log a pull request if you want to make improvements.
