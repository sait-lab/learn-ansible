# Learn Ansible

Welcome to the **learn-ansible** repo! This is a practical, beginner-friendly collection of notes, examples, and playbooks to help you get comfortable with Ansible.

## What's Inside

- **[Ansible Demo.md](Ansible%20Demo.md)**: A complete walkthrough covering Ansible installation (via `pipx`), SSH connectivity, inventory management, variables, loops, common modules (`copy`, `fetch`, `lineinfile`), and privilege escalation (`become`).
- **[ansible-demo-code/](ansible-demo-code/)**: Hands-on demo files and playbooks (`playbook1.yaml` through `playbook15.yaml`), along with sample inventories and `ansible.cfg` to test things out.

## Quick Start

### 1. Prerequisites
- Python 3 installed
- SSH key-based authentication configured between your control node and target hosts

### 2. Install Ansible
We recommend using `pipx` for a clean install:

```bash
# Install pipx (Ubuntu/Debian)
sudo apt update && sudo apt install -y pipx
pipx ensurepath

# Install Ansible
pipx install --include-deps ansible
```

### 3. Run a Playbook
Jump into the demo directory and try running a playbook:

```bash
cd ansible-demo-code/playbook

# Test playbook execution in check mode (dry run)
ansible-playbook -i inventory.ini playbook1.yaml --check

# Run the playbook
ansible-playbook -i inventory.ini playbook1.yaml
```

## Tips
- Check out `Ansible Demo.md` for in-depth explanations and command breakdowns.
- Make sure to update the inventory IP addresses in `ansible-demo-code/` to match your own lab VMs or containers before running the playbooks.
