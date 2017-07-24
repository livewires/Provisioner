# LiveWires provisioning

Using [Ansible](https://docs.ansible.com/) set up a bunch of computers for use at LiveWires.

## Setup

1. Install Ansible on the host computer (On MacOS: `brew install ansible`)
2. Ensure SSH servers are on each remote machine and you have access
3. Copy the host public key to the remote servers
4. List the IP addresses in the `hosts` file
5. Check everything is working with `ansible all -i hosts -m ping`

With the `hosts` file computers are groups by the section:

- web
- mob-dev
- video (coming soon)
- programming (coming soon)

## Provision

```
ansible-playbook playbook.yml -i hosts
```
