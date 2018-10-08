# 2.1.1 Exploratory Data Analysis - Pete Alonzi October 8, 2018

## 2.1.1.1 Types of Data
### 2.1.1.1.1 Categorical - Qualitative - limited number of possibilities
* 2.1.1.1.1.1 Nominal - "collectively grouped on the basis of a particular characteristic"
  * grouped by characteristics: eg - [NFPA 291](https://www.google.com/search?q=nfpa+291&safe=off&rlz=1C5CHFA_enUS690US690&source=lnms&tbm=isch&sa=X&ved=0ahUKEwiAjoKJtu3dAhXEMd8KHQlwAosQ_AUIDygC&biw=1440&bih=636&dpr=2#imgrc=pB0PvN24Ei9lNM:)
* 2.1.1.1.1.2 Ordinal - "natural, ordered categories"
  * eg: [Likert scale](https://en.wikipedia.org/wiki/Likert_scale): 1=Like,2=Neutral,3=Dislike
  * nb: I chose this example because it uses numbers to correspond to categories but it is not numeric
### 2.1.1.1.2 Numerical - Quantitative - takes on a numerical value that is in direct proportion
* 2.1.1.1.2.1 Counts - integer
  * represents the number of times something occurs: eg - number of fire hydrants in Fry's Spring Neighborhood
  * requires a strict definition: Is half of a sandwich a sandwich?
* 2.1.1.1.2.2 Measures - float
  * represents a quantifiable value
* Error/uncertainty - BONUS ITEM NOT ON THE FORMAL AGENDA
  * every reported value is only as good as its reported error estimate
  * two kinds of error
    * statistical - eg: we sampled 1,000 people and if we sampled a different 1,000 people we would get a different answer
    * systematic - eg: we sampled 1,000 people but they interpreted the questions differently
  * Note about election polling data
    * when it says +/- 3% that means they polled about 1,000 people, they are quoting the statistical error
    * they do not include the size of the systematic error
  
## 2.1.1.2 Exploring Data

Exploratory Data Analysis, EDA. Nabokov put it best, 
* "In reading, one should notice and [play with] details. ... We should always remember that the work of art is invariably the creation of a new world, so that the first thing we should do is to study that new world as closely as possible, approaching it as something brand new, having no obvious connection with the worlds we already know."

The hard part is to put aside your bias and explore with an open mind. Everything else is easy.

### 2.1.1.2.1 Plots: Bar, Histogram, and Box (slight reordering from before)
#### 2.1.1.2.1.1 Histograms and Bar Graphs
* Histograms and Bar Graphs have lots of similarities. Here is the core difference:
  * Histograms express numerical data
    * Hardest part in excel is finding the fiddly bit for them
    * For me: Tools -> Excel Add-ins -> Analysis ToolPak ; then Data -> Data Analysis -> Histogram
    * Don't forget to click, 'chart output'
  * Bar Graphs express categorical data
  
* [Histogram Example](https://github.com/alonzi/DataWranglingForOpenData/blob/master/histo.png)
* [Bar Graph Example](https://github.com/alonzi/DataWranglingForOpenData/blob/master/bargraph.jpg)
    
#### 2.1.1.2.1.2 Box Plots
* There are a few versions, make sure you know what you're looking at. Here we describe the most common.
* Features:
  * Central Band: denotes the median
  * Box limits: denotes the median of the upper and lower halves of the dataset
  * Whiskers: varies greatly, often an extended quartile multiple or percentile, always check this one
  * Outliers: Often represented as individual points
* [Box Plot Example](https://github.com/alonzi/DataWranglingForOpenData/blob/master/mm.png)
* In excel this is [gnarly](https://support.office.com/en-us/article/create-a-box-plot-10204530-8cdf-40fe-a711-2eb9785e510f)
  
### 2.1.1.2.3 Measures
#### 2.1.1.2.3.1 Centrality (aka averages)
* [Wiki is a great resource](https://en.wikipedia.org/wiki/Mean)
* 2.1.1.2.3.1.1 Mean
  * What people normally think of as the average
  * Add everything up and divide by the total number of entries: eg (5,10,15) --> (5+10+15) / 3 = 10
* 2.1.1.2.3.1.2 Median
  * The point where as many are above as below: eg (5,10,15) --> 10
* 2.1.1.2.3.1.3 Mode
  * The most common value: eg (5,10,15) --> 5,10,15
* Here is a visual: https://github.com/alonzi/DataWranglingForOpenData/blob/master/mmm.png
* There are lots of scenarios, these are just a few.

#### 2.1.1.2.3.2 Spread
* 2.1.1.2.3.2.1 Standard Deviation
  * Again [Wiki is a great resource](https://en.wikipedia.org/wiki/Standard_deviation)
  * Gnarly Formula - the square root of the mean of the distance squared
  * [Visual Expression](https://github.com/alonzi/DataWranglingForOpenData/blob/master/sd.png)
  * Basically the standard deviation is how spread out your data is (but beware of the two towers example)
  
* 2.1.1.2.3.2.2 Quartiles/Interquartile Range
  * A quartile is a type of quantile, it is one fourth of the data
  * Defined by three points: Q1,Q2,Q3
  * [Visual Example](https://github.com/alonzi/DataWranglingForOpenData/blob/master/quartiles.png)

### 2.1.1.2.4 Summary Tables
* A summary table is typically laid out with rows representing objects and columns representing observables of those objects
  * example rows: the city of charlottesville, albemarle county
  * example columns: population, population density, mean number of misdemeanor arrests per day, etc.

### 2.1.1.2.5 Exceptions
#### 2.1.1.2.5.1 No Data/Nulls
* Sometimes data is missing: we call that No Data
  * depending on your analysis this may skew the results or even invalidate them
  * you can do several things: exclude and impute are two common solutions
* Sometimes data is encoded as Null
  * this means zero but often does not mean zero, be careful
  * look to the data dictionary to understand what is going on

#### 2.1.1.2.5.2 Outliers
* Outliers are tricky
  * if they arise from a statistical effect they cannot be ignored, but without proper treatement will skew results, proper error estimation is critical
  * if they arise from a systematic effect they can be excluded as long as provisions are clearly explained to the audience
    * in this case subsetting is often very useful


## 2.1.1.3 Exercise Explore a Data Set
While you are working these exercises take note of the problems that crop up. We will be addressing them in future sessions.

* Categorical or numerical? Explain why.
  * gender
  * wage
  * date of birth
  
* Pick a variable and make a histogram or a bar graph. Explain why you chose that type of plot.

* Compute the mean, median, mode, and standard deviation of the wage feature.

* Pick a feature and make a summary table.

* Identify an outlier and explain how to treat it.

