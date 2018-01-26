For this tutorial I will use a dataset of Stack Overflow posts from September 2017 compiled from the [Stack Exchange Data Explorer](https://data.stackexchange.com/stackoverflow/query/new). I want to use this dataset because, in addition to being interesting to developers, it contains numerical, text, time series and geographic data. My plan is to show a wide collection of Python's visualization libraries, rather than diving too deeply into any one of them.

We will start by looking at how complete the data is using [missingno](https://github.com/ResidentMario/missingno). Next we will make histograms of a few columns such as the time a post was created and the number of posts there are of each type using [Pandas](http://pandas.pydata.org) and Bokeh. 

Once we have an idea of the distribution of a few fields, we will start using scatter plots to show the correlations between numerical fields using [Seaborn](http://seaborn.pydata.org/). At this point we will start exploring methods of restructuring the data such as building a clustering over the tags based on how often they co-occur.

After exploring the numerical data, we will look at how we can plot the geographic data using [Geoplot](https://residentmario.github.io/geoplot/index.html). We will look at where questions and answers are coming from, and which hours are the most popular for posting at different longitudes.

Next we will look at the text of the posts themselves. We will start out by looking at the most common words in question titles and how to visualize them as a [word cloud](https://github.com/amueller/word_cloud). I want to then show how we can represent words with more context using a [word tree](https://www.jasondavies.com/wordtree/), but I haven't decided on which python library to use for that yet.

To finish up we will build some interactive visualizations in [Gleam](https://github.com/dgrtwo/gleam).