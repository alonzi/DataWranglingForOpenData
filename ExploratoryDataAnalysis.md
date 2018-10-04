# 2.1.1 Exploratory Data Analysis - Pete Alonzi October 8, 2018

## 2.1.1.1 Types of Data
### 2.1.1.1.1 Categorical - Qualitative - limited number of possibilities
* 2.1.1.1.1.1 Nominal
  * grouped by characteristic: eg - [NFPA 291](https://www.google.com/search?q=nfpa+291&safe=off&rlz=1C5CHFA_enUS690US690&source=lnms&tbm=isch&sa=X&ved=0ahUKEwiAjoKJtu3dAhXEMd8KHQlwAosQ_AUIDygC&biw=1440&bih=636&dpr=2#imgrc=pB0PvN24Ei9lNM:)
* 2.1.1.1.1.2 Ordinal
  * grouped by eg - [Likert scale](https://en.wikipedia.org/wiki/Likert_scale): 1=Like,2=Neutral,3=Dislike
  * nb: I chose this example because it uses numbers to correspond to categories but it is not numeric
### 2.1.1.1.2 Numeric - Quantitative - takes on a numerical value that is in direct proportion
* 2.1.1.1.2.1 Counts
  * represents the number of times something occurs: eg - number of fire hydrants in Fry's Spring Neighborhood
  * requires a strict definition: Is half of a sandwich a sandwich?
* 2.1.1.1.2.2 Measures
  * represents a quantifiable
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
#### 2.1.1.2.1.1 Histograms
#### 2.1.1.2.1.2 Bar Plots
#### 2.1.1.2.1.3 Box Plots

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

### 2.1.1.2.1.1 Summary Tables

### 2.1.1.2.6 No Data/Nulls
### 2.1.1.2.7 Outliers


## 2.1.1.3 Ex. Explore a Data Set
