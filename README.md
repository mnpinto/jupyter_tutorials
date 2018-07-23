# Jupyter Notebooks Tutorial
## Install Anaconda
Go to https://www.anaconda.com/download/, download and install the most recent version of Anaconda with Python 3.6.
## Start a jupyter notebook
With Anaconda Jupyter is installed by default. Now you can open the terminal (or Anaconda prompt if you are on Windows) and type:
```bash
jupyter notebook
```
A jupyter notebook will be created and the browser will open by default. Notice the link should look link `localhost:8888`. This means the notebook is running in your local machine in port 8888.

**Start a notebook in specific directory:**
To set the home folder for the current notebook you can pass the argument the `--notebook-dir=some_path` argument to set the home folder to ´some_path´. To set for the current folder use a dot in the path.
```bash
jupyter notebook --notebook-dir=~/my_notebooks #set the notebook home folder to my_notebooks folder in home (if you are in linux)
jupyter notebook --notebook-dir=. #set the notebook home folder to the current directory.
```
## Notebook server on remote host
**Find your public ip address**
```bash
curl ipinfo.io/ip
```
**Find your internal network address**
```bash
hostname -I
```
### Add new trusted machine (Linux)
Generate a pair of ssh keys in your local host with the following command:
```bash
ssh-keygen
```
This will generate to files inside `~/.ssh`, by defaut:
```bash
id_rsa
id_rsa.pub
```
The `id_rsa` is the private key and should never be shared. The `id_rsa.pub` has the public key. To gain acess to the remote host add the public key to the `~/.ssh/authorized_keys` file if it exists or create it otherwise. If you are on the local network you can access it using the local address. If you need to access with the public ip address you need to make a forward in the router for an ssh connection for your remote host.

### Add new trusted machine (Windows)
* Go to https://www.putty.org/ and install PuTTY. After the installation is complete type `windows key + R` and write `PuTTYgen`.
* Choose the option to generate and then save both public and private keys in a safe place. 
* Copy the public key as in the Linux case to your remote host.
* Open PuTTY and go to `Connection` > `SSH` > `Auth` and browse the private key location.
* Go back to `Session` in PuTTY and type the ip of the remote host. You should now be able to connect.

### Add new trusted machine (Android)
* Install JuiceSSH App
