# Creating conda environment for GIS in python
This was tested on ubuntu 18.04 LTS following https://automating-gis-processes.github.io/CSC18/course-info/Installing_Anacondas_GIS.html.

### Step 1 - Create the conda environment
I'm naming it as **geo**:
```bash
 conda create -n geo python
 ```
 
 ### Step 2 - Install packages
 We start by activating the **geo** environment:
 ```bash
  conda activate geo
 ```
Next, install packages:
```bash
  conda install numpy pandas scipy matplotlib scikit-learn networkx bokeh statsmodels pyspark geopandas cartopy geoplot osmnx folium dash pysal rasterio rasterstats
```
 ### Step 3 - Configure jupyter notebook kernel
```bash
conda install jupyter ipykernel
python -m ipykernel install --user --name geo --display-name "Python (geo)"
```
Then you can start a jupyter notebook and create a new notebook with the kernel "Python (geo)". 
You can change the kernel of an existing notebook in the menu *Kernel >> Change kernel*.
