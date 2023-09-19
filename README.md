# aus_precip_benchmarking: Jupyter Notebooks (Python) Analysis Files for the CORDEX-Australasia Precipitation Benchmarking

Initial release of the software used for the Regional Climate Model (RCM) Precipitation Benchmarking Framework. 

The Jupyter Notebooks here were used to complete the main analysis and create the figures for the manuscript:
Isphording, R.N., L.V. Alexander, M. Bador, D. Green, J. P. Evans, and S. Wales. A Standardized Benchmarking Framework to Assess Downscaled Precipitation Simulations. Accepted in Journal of Climate. in revision. 

The notebooks are named according to the corresponding figures from the manuscript. Custom functions used within each of the Fig*.ipynb notebooks is defined in the master_functions_bmf.ipynb notebook.
Functions included are:
  File Input functions:
    - Get data model names from a user-defined dictionary
    - Get a subset of models from da user-defined dictionary
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

The notebooks were developed to encourage reuse from the broader climate community and include options not explicitly used within the manuscript (such as seasonal subsetting). 
Additional explanations for the metrics used can be found within the corresponding manuscript and Jupyter notebooks.  
