# aus_precip_benchmarking: Jupyter Notebooks (Python) Analysis Files for the CORDEX-Australasia Precipitation Benchmarking

Version 1.1 release of the software used for the Regional Climate Model (RCM) Precipitation Benchmarking Framework. 

This code has been updated from v1.0 to address deprecated functionality with Pandas DataFrames and new automation to create a heat map for the Seasonal Cycle Minimum Standard Metric (Figure 4 in the corresponding manuscript).

[![DOI](https://zenodo.org/badge/392496602.svg)](https://zenodo.org/badge/latestdoi/392496602)

The Jupyter Notebooks here were used to complete the main analysis and create the figures for the manuscript:
Isphording, R.N., L.V. Alexander, M. Bador, D. Green, J. P. Evans, and S. Wales (2023). A Standardized Benchmarking Framework to Assess Downscaled Precipitation Simulations. J Clim. 37, 1089-1110, https://doi.org/10.1175/JCLI-D-23-0317.1. 

The notebooks are named according to the corresponding figures from the manuscript. 
Custom functions used within each of the Fig*.ipynb notebooks is defined in the master_functions_bmf.ipynb notebook.

Functions included are:

  File Input functions:
  
    - Get data model names from a user-defined dictionary
    - Get a subset of models from a user-defined dictionary
    - Get model data paths
    - Get data from paths
    
  Plotting Functions:
  
    - Truncating a predefined colormap
    - Define vertical bands to shade along a time series
    
  Spatially Averaged Functions:
  
    - Weighted Spatial Average from Pre-processed Data (such as a climatology)
    - Spatial Pattern Correlation (Homogenous Variable Names)
    - Mean Absolute Percentage Error (Homogenous Variable Names)
    - Monthly Averages over time/space to gauge seasonality (Homogenous Variable Names)
    - Annual Averages
    - Normalized Root Mean Square Error for pre-processed data (i.e. maps of climatologies or other calculated values)
    - Paired Bootstrapping function to calculate the Circular Correlation Coefficient on a random subset of two sets of data
    - Get Weighted Spatial Average at Default Time Step
    
  Metrics for Maps (Temporally Averaged):
  
    - Get Bias
    - Get Climatology
    - Get the Amplitude of the Annual Cycle at Each Grid Point
    - Get the Phase of the Annual Cycle at Each Grid Point

The notebooks require a general understanding of Python programming but were developed to encourage reuse from the broader climate and Earth science communities and include options not explicitly used within the manuscript (such as seasonal subsetting).

Unless a user is analyzing the same 24 simulations for the CORDEX-Australasia ensemble used in the manuscript, users will need to revise the gcm_ and rcm_names lists in the master_functions notebook to match their ensemble. Users will also need to edit the Spatiotemporal Boundaries, Data Keywords, and the master path(s) within each Fig* notebook to match their database structure and spatiotemporal specifications. Users will also likely need to change the figure settings based on the size of their ensemble, the range of their values, the region, etc. It's also encouraged to review how masks are applied within the relevant functions in the master_functions notebook if users are incorporating masking over their domain.
 
Additional explanations for the metrics used can be found within the corresponding manuscript and Jupyter notebooks. I encourage users to adapt these scripts to their needs.
