# stampede2Setup
Files necessary for setting up a nice environment on stampede2

Intended to help people new to cluster computing get set up as fact as possible.

# Random
### Copying ssh key to host when ssh-copy-id doesnt work: 
In the following, replace {...} with username@host for appropriate platform/cluster:  
Run in a local terminal `$env:USERPROFILE\.ssh\id_rsa.pub | ssh {...} "cat >> .ssh/authorized_keys"`

### Manually running jupyter notebooks (general cluster instructions)
Instructions courtesy of [Chelsea](https://hangchelseasu.github.io/). Assume your cluster has an interactive compute node session utility, accessed by the command "idev" (interactive development, changes for each cluster). The following steps allow you to use its compute resources for a jupyter notebook which is accessed locally in your personal machine's browser.  

**On cluster:**  
- Go to the directory you want to work in
- Start an interactive session `idev -t 2:00:00` (or similar command, you can also change how much time you request)
- Activate your python environment `conda activate env` (or equivalent)
- Set jupyter password `jupyter notebook password` and set a simple password (you may need to do this every time).
- Start notebook `jupyter notebook --no-browser --ip=*`

Then note the output in that terminal, as it will give you a URL which looks like `http://hostname:YYYY` where `YYYY` is the default port on that system (can be changed if desired). You can always check what `hostname` is for your specific compute node by typing `hostname` in a terminal connected to that particular compute node.

**On your local machine:**  
- Run `ssh -fvNL XXXX:hostname:YYYY user@cluster` with the following replacements:
    - `XXXX` -> the port you wish to use on your local machine, often people use 8888, but it may be in use so try 8889 or similar
    - `hostname:YYYY` -> from the above steps
    - `user@cluster` -> the usual info you would use to ssh into that cluster. If you have an ssh config file set up you can just type the ssh HostName here[^2]
- Go to a local browser and type `localhost:XXXX` in the URL field
- Enter your password, and you will see the notebooks.

[^2]: I.e. if you usually type `ssh clusterThatIWorkOn` then you can replace `user@cluster` above with `clusterThatIWorkOn`
