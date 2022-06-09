# stampede2Setup
Files necessary for setting up a nice environment on stampede2

Intended to help people new to cluster computing get set up as fact as possible.

Copying ssh key to host when ssh-copy-id doesnt work: replace {_} with username@host for appropriate platform
type $env:USERPROFILE\.ssh\id_rsa.pub | ssh {IP-ADDRESS-OR-FQDN} "cat >> .ssh/authorized_keys"
