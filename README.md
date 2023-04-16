# ansible
My Ansible-stack for deploying and configuring servers and clients

# Machine Provisioning
Berofe running this playbook, the host's ssh-keys has to be present on the target node. For example by running:
`ssh-copy-id -i ~/.ssh/id_ed25519 <username>@<node>`

Another sideffect is that the hardening creates new ssh-keys for sshd. Thus, the user will be asked to confirm the
fingerprint of the target node's ssh-key the first time using SSH (or Ansible) to access the node.

## Hardening
For the custom settings for sshd I have mostly been inspired by https://www.sshaudit.com/hardening_guides.htm.

Furthermore, I have found the following tool quite useful for checking the ssh-configuration: https://github.com/jtesta/ssh-audit
