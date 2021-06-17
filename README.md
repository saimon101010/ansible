# ansible

Before execute you shoud specify vars:

-- inventory/server.yml - host ip

--- files/id_edsa - private-key for clone repo with pages , after you add key specify it's name in roles/sites/vars/
--- roles/sites/vars/ - git repo url and name pages for nginx config (can be NULL if name page index.html )

---- roles/system/vars -  2 ssh-keys

May be used like this:

ansible-playbook main.yml -i "inventory/server.yml" -e "ansible_ssh_pass=" --tags=site

ansible-vault pass - qwerty