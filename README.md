# Raspberry Pi 4 Fedora IoT Playbook

Raspberry Pi 4 Fedra IoT setup and configuration via Ansible.

## Quick Start

```bash
ansible-galaxy collection install ansible.posix community.general
ansible-playbook -i inventory.yaml playbook.yaml
```

## Ad-hoc Examples

Run a command on all nodes:

```bash
ansible all -i inventory.yaml -a "rpm-ostree status"
```

Reboot all nodes using the reboot module:

```bash
ansible all -i inventory.yaml -m ansible.builtin.reboot -a "reboot_timeout=300"
```
