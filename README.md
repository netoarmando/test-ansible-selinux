# test-ansible-selinux

```bash
==> default: Running provisioner: ansible...
Vagrant has automatically selected the compatibility mode '2.0'
according to the Ansible version installed (2.7.10).

Alternatively, the compatibility mode can be specified in your Vagrantfile:
https://www.vagrantup.com/docs/provisioning/ansible_common.html#compatibility_mode

    default: Running ansible-playbook...

PLAY [all] *********************************************************************

TASK [Gathering Facts] *********************************************************
ok: [default]

TASK [create test config file] *************************************************
fatal: [default]: FAILED! => {"changed": false, "checksum": "cbddbad2c491aab236e1025ad5b9ace129ea5667", "cur_context": ["system_u", "object_r", "nfs_t", "s0"], "gid": 0, "group": "root", "input_was": ["system_u", "object_r", "default_t", "s0"], "mode": "0744", "msg": "invalid selinux context: [Errno 95] Operation not supported", "new_context": ["system_u", "object_r", "default_t", "s0"], "owner": "root", "path": "/vagrant/.ansible_tmpenzaqj_htest-file.yaml", "secontext": "system_u:object_r:nfs_t:s0", "size": 8, "state": "file", "uid": 0}
	to retry, use: --limit @/root/test-ansible-selinux/provision.retry

PLAY RECAP *********************************************************************
default                    : ok=1    changed=0    unreachable=0    failed=1   

Ansible failed to complete successfully. Any error output should be
visible above. Please fix these errors and try again.

```
