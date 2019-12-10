# ODF Workshop 1

This repository contains the Jupyter Notebooks for the use cases: 

1. Underwater object detection (Koster)
2. Invasive Species GIS Analysis (D. Villosus)

## Getting the data

### Git Clone
For those with a Github account or git installed simply clone this repository using ```git clone https://github.com/ocean-data-factory-sweden/odf-workshop-1.git``` and ```cd``` into this directory.

### No Github account

- Option 1: Github installation
  - Windows: Download and install [here](https://gitforwindows.org/)
  - Mac (Homebrew): ```brew install git```
  - Linux (Debian & Ubuntu): ```sudo apt-get install git```

- Option 2: Manual download
  - Find "Clone or Download" button on repository website and click "Download zip"
  - NOTE: The package "PyImpute" also relies on an installation from a git repository, so if you choose to go this route, you will first need to manually download that repository as well from [here](https://github.com/jannesgg/pyimpute.git#egg=pyimpute). 
  
## Prerequisites

What things you need to install the software and how to install them. We recommend that you create a new virtual environment before installing the packages. Popular options include [Anaconda](https://www.anaconda.com/distribution/) and [PyEnv](https://github.com/pyenv/pyenv).

#### Linux & Mac OS:

```
pip install -r requirements.txt
```

#### Windows

Based on the experiences of many during the workshop, here are some of the possible issues you may run into when installing from the requirements.txt file on Windows and the proposed solutions.

To prevent most of the experienced errors, we advise that you follow the following instructions instead of installing from ```requirements.txt``` from the very start.

1. Install Visual Studio C++:
    - Install using any ONE of these choices:
Microsoft [Build Tools for Visual Studio](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16).
Alternative link to Microsoft [Build Tools for Visual Studio](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2019).
Offline installer: [vs_buildtools.exe](https://aka.ms/vs/16/release/vs_buildtools.exe)
Select: Workloads → C++ build tools.
Install options: select only the “Windows 10 SDK” (assuming the computer is Windows 10). To use MSVC cl.exe C / C++ compiler from the command line, additionally select the C++ build tools.

2. Install Numpy, Affine and others: ```pip install numpy affine cligj click enum34```


3. Install GDAL
    - Download the appropriate binary from [here](http://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal) then run the prompt ```pip install GDAL-1.11.2-cp27-none-win32.whl``` with the name changed to the binary version you have downloaded.
    - Conda users: ```conda install -c conda-forge gdal```

4. Install Rasterio
    - Download the appropriate binary from [here](http://www.lfd.uci.edu/~gohlke/pythonlibs/#rasterio) then run the prompt ```pip install rasterio-0.24.0-cp27-none-win32.whl``` with the name changed to the binary version you have downloaded.
    - Conda users: ```conda install -c conda-forge rasterio```

5. Install Kepler GL
    - ```pip install keplergl``` 
    - ```jupyter nbextension install --py --sys-prefix keplergl```
    - ```jupyter nbextension enable --py --sys-prefix keplergl```
    - ```jupyter labextension install @jupyter-widgets/jupyterlab-manager keplergl-jupyter```

6. Install Geopandas
    - Pip installation ```pip install pandas fiona shapely pyproj rtree``` 
    ```pip install geopandas```
    
    - Conda users: ```conda install pandas fiona shapely pyproj rtree```
    ```conda install --channel conda-forge geopandas```
    
7. Run ```pip install -r requirements.txt``` to fill any missing requirements.



## Additional installation issues

Should you experience any issues not highlighted above, please do not hesitate to contact us at jurie.germishuys[at]combine.se.

 
## Authors

* **Jurie Germishuys** - *Initial work* - [Github](https://github.com/jannesgg)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

