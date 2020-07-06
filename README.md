# Predicting Urban Development
This project uses the Google Earth Engine (GEE) Python API to identify trends in development surrounding Denver International Airport (DIA) from time-series Landsat imagery. The package geemap is used to visualize map layers. This repository was initially created as Richard Udell’s final project for the Earth Data Analytics Professional Certificate from the Earth Lab at University of Colorado - Boulder.

### How to run this workflow
There are two Jupyter Notebooks in the Notebooks folder.  
The first notebook, LinearFit_Workflow_Only.ipynb, contains the analysis that identifies urban trend surrounding DIA using GEE’s built-in ee.Reducer.linearFit().
The second notebook, GEE_Python_API_Tutorial.ipynb, includes a tutorial for the first notebook!  This is a great place to start if you are new to Python and the GEE Python API.  

### Environment and setup
To [set up the development environment](https://www.earthdatascience.org/courses/intro-to-earth-data-science/python-code-fundamentals/use-python-packages/use-conda-environments-and-install-packages/), create a new environment from the environment-ee.yml file.

    >conda env create -f environment-ee.yml

A [Google Earth Engine account](https://signup.earthengine.google.com) is necessary to use the Google Earth Engine API (a university email address may be accepted more quickly).

An excellent resource for Google Earth Engine Python API is Dr. Quisheng Wu's GitHub package [geemap](https://github.com/giswqs/geemap).

### Data needed
The notebooks will create their own data by exporting it from GEE - this means the data that is needed to import into the workflow is created and exported earlier in the workflow.  The data will export as a .TIF to your Downloads/ folder on your home directory.  Landsat 5 satellite imagery is the initial source data for both notebooks.  The entire Landsat 5 collection is loaded from the [GEE Data Catalog](https://developers.google.com/earth-engine/datasets/catalog/landsat-5/) with the GEE Python API, preventing it to never have to exist locally on your computer.
The data folder contains the exports that will be created if you run the workflow with the preset circular ROI.  You will only need to reference this data if the export does not work.  In this case you will have to change the input directory for importing the .TIF file.


### Note on relevance of this repository
It is clear to any observer that a large amount of development has occurred around the Denver International Airport since its completion of construction in 1995. Since the Denver International Airport was the last major airport constructed in the United States (no major airport has been constructed since 1995), understanding the impact DIA had on the development of the surrounding region is of interest to policy makers, business owners, and citizens in the Denver Metro Area. The goal of this project is to develop a model that can predict future development.

Google Earth Engine is a powerful tool, however, fewer workflows involve the the python API than the built-in JavaScript API. Additionally, the geemap package was first released in March 2020. With proper installation of these packages, the workflow can be run in a Jupyter Notebook (.ipynb) - workflow is contained in one script.
