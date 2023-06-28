# stampede2Setup
Files necessary for setting up a nice environment on stampede2

Intended to help people new to cluster computing get set up as fact as possible.

# Random
### Copying ssh key to host when ssh-copy-id doesnt work: 
The following only works when your cluster uses an authorized_keys file for ssh accesses.  

Run in a local terminal `$env:USERPROFILE\.ssh\id_rsa.pub | ssh {...} "cat >> .ssh/authorized_keys"` where you replace `{...}` with `username@host` for appropriate platform/cluster:

### Using Jupyter notebooks (general cluster instructions)
See [this github gist](https://gist.github.com/CianMRoche/ce176a089c06fd81d26f339f99f5af87)
