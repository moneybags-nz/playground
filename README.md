# Moneybags's playground

### Welcome to my playground

This repo contains playbooks that I use for my home infrastructure. Feel free to use them, just make sure you have a folder for your inventory file.

### Important

Please note that if your using my `linux_initialsetup` playbook you'll need to make sure that you have added the public ssh keys of your hosts to your known_hosts file. You can do this by running the following commands (I add the IP address of the host as well just in case my internal DNS server stops working):

```bash
ssh-keyscan -H hostname >> ~/.ssh/known_hosts
ssh-keyscan -H ipaddress >> ~/.ssh/known_hosts
```

To execute a playbook run

```
ansible-playbook -i ~/playgound/inventory/<file> -u <yourusername> -k -K <file>.yml
```

Feel free to add comments.
