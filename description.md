For this tutorial I will use a dataset of Stack Overflow posts from the first two weeks of September 2017 compiled from the [Stack Exchange Data Explorer](https://data.stackexchange.com/stackoverflow/query/new). I want to use this dataset because, in addition to being interesting to developers, it contains numerical, text, time series and geographic data. My plan is to focus on how visualization can assist exploratory research and data cleaning.

After loading the libraries and data, we will examine how complete the data is using [missingno](https://github.com/ResidentMario/missingno). In this section, we will look at how the data can be partitioned and track down some anomalies on Stack Overflow's website. As part of this section, the bar charting capabilities of [Pandas](http://pandas.pydata.org) and [Bokeh](https://bokeh.pydata.org/en/latest/).

Next we will concentrate on visualizing text from the question titles. This section will begin by using the bag of words model to make a bar chart and heatmap. We will then discuss the shortcomings of this model and go over [word trees](http://hint.fm/papers/wordtree_final2.pdf) using [Pydotplus](https://pydotplus.readthedocs.io).

The fourth section looks at what our data tells us about the time of each post. First, we will make a histogram of the hour of the day each post was created. Next we will look at how many minutes passed between when a question was posted and when it was answered. We will look briefly at the anomalies this shows us, and at how box plots allow us to compare latency distributions using [Seaborn](http://seaborn.pydata.org/).

The fifth section looks at the network of users answering each other's questions. We model this network by drawing an edge from each user who answered a question to the person they answered. Using [Pydotplus](https://pydotplus.readthedocs.io) we visualize how connected this graph is and the different roles taken on by different users.

The final section deals with the self reported location data from Stack Overflow. This section will go through a few example visualizations with this data, and talk about why geo-spatial data is hard to work with. We will use [Bokeh](https://bokeh.pydata.org/en/latest/) to make the example visualizations.

I will finish this presentation with a short conclusion. There are many libraries for visualization in Python that this talk does not touch on. Hopefully the examples here will give participants the vocabulary to find other libraries and experiment on their own. The main points I'm hoping participants come away with are:

1. Visualize early - Making visualizations early on can help a lot with data cleaning
1. Visualize for yourself first - Visualization is a powerful tool for showing you what is going on in your data and if you can't understand your own visualizations, no one else will
1. Barcharts are awesome, but not everything should be a barchart - Wordtrees, network diagrams and heatmaps are also nice
1. You can do it - You know python and therefore can make almost any chart you want. If a library doesn't already exist to do what you want, I'd appreciate if you'd make one.