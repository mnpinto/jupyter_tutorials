# Jupyter Notebooks Tutorial
## Install Anaconda
Go to https://www.anaconda.com/download/, download and install the most recent version of Anaconda with Python 3.6.
## Start a jupyter notebook
With Anaconda Jupyter is installed by default. Now you can open the terminal (or Anaconda prompt if you are on Windows) and type:
```bash
jupyter notebook
```
A jupyter notebook will be created and the browser will open by default. Notice the link should look link localhost:8888. This means the notebook is running in your local machine in port 8888.
**Start a notebook in specific directory:**
To set the home folder for the current notebook you can pass the argument the ´--notebook-dir=some_path´ argument to set the home folder to ´some_path´. To set for the current folder use a dot in the path.
´´´bash
jupyter notebook --notebook-dir=~/my_notebooks #set the notebook home folder to my_notebooks folder in home (if you are in linux)
jupyter notebook --notebook-dir=. #set the notebook home folder to the current directory.
´´´
## Notebook server on local network
