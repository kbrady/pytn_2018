# Visualizing Everything in Python

A workshop from [PyTennessee 2018](https://www.pytennessee.org)

You can go through the tutorial online by **clicking** the following button:

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/kbrady/pytn_2018/master)

## Description

This tutorial covers methods of performing several visualization techniques in Python with a particular focus on exploratory research and data cleaning. It uses a dataset of Stack Overflow posts from the first two weeks of September 2017 compiled from the [Stack Exchange Data Explorer](https://data.stackexchange.com/stackoverflow/query/new).

[...](description.md)

### Topics Covered
1. Data Completeness
1. Text Visualization
1. Visualize Time
1. Visualize Network Connections
1. Mapping Location

### Libraries Used
- [numpy](http://www.numpy.org)
- [pandas](https://pandas.pydata.org)
- [seaborn](https://seaborn.pydata.org)
- [bokeh](https://bokeh.pydata.org/en/latest/)
- [missingno](https://github.com/ResidentMario/missingno)
- [pydotplus](https://pydotplus.readthedocs.io)
- [shapely](https://shapely.readthedocs.io/en/latest/)
- [descartes](https://bitbucket.org/sgillies/descartes/)

## Installing Environment & Dependencies

To use the scripts in this repository, you must have _Anaconda_ installed on the systems that will be running the scripts. This will simplify the process of installing all the dependencies.

If you are unsure if you have Anaconda on your machine run `conda -h` in your terminal. This should bring up a help message. If you get a command not found error, follow the installation instructions [here](https://docs.anaconda.com/anaconda/install/).  After installation, you may still need to add Anaconda to your path variable. If `conda -h` still doesn't work, see instructions on adding Anaconda to your path in the Anaconda installation instructions.

For reference on Anaconda environments, see: [https://conda.io/docs/user-guide/tasks/manage-environments.html](https://conda.io/docs/user-guide/tasks/manage-environments.html)

The package counts with a __Makefile__ with useful functions. You must use this Makefile to ensure that you have all the necessary _dependencies_, as well as the correct _conda environment_. 

* Show all available functions in the _Makefile_

```
$:  make show-help
    
    Available rules:
    
    clean               Delete all compiled Python files
    environment         Set up python interpreter environment - Using environment.yml
    remove_environment  Delete python interpreter environment
    test_environment    Test python environment is setup correctly
    update_environment  Update python interpreter environment
```

* __Create__ the environment from the `environment.yml` file:

```
    make environment
```

* __Activate__ the new environment __pytn_viz_2018__.

```
    source activate pytn_viz_2018
```

* To __update__ the `environment.yml` file (when the required packages have changed):

```
  make update_environment
```

* __Deactivate__ the new environment:

```
    source deactivate
```

### Troubleshooting

If you are trying to install the environment on a mac and get an XCode error, you may need to run
```
xcode-select install
```

## Acknowledgments

Thank you to:
+ [Victor Calderon](https://github.com/vcalderon2009) - for helping me set up the environment
+ [Gayathri Narasimham](https://github.com/gnvandy) - for inspiring me to do this talk and getting me interested in forum data
+ Rachael Brady - for teaching me the power of visualization and being a guinea pig for this talk
