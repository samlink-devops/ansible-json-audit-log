# ansible-json-audit-log
This project provides a json formatted audit log for ansible

## Known limitations
A magic variable named environment_name must be defined in inventory. Use group_vars/all to set defaults.

## Configuration
1. Copy json_audit.py callback plugin to plugins directory (default: /usr/share/ansible/plugins/callback/)
2. Ensure that your inventory has environment_name variable set
3. Ensure that /var/log/ansible is writeable by user running ansible
4. Whitelist json_audit callback plugin:

    [defaults]
    bin_ansible_callbacks = True
    callback_whitelist = json_audit
