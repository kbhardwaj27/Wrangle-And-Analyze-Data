# Wrangle and Analyze Data - WeRateDogs

Real-world data rarely comes clean. Using Python and its libraries, I gathered data from a variety
of sources and in a variety of formats, assessed its quality and tidiness, then cleaned it. 
I have documented my wrangling efforts in a Jupyter Notebook and showcased them through analyses 
and visualizations using Python (and its libraries).

#### After completing the project, I covered the steps involved to Wrangle and Analyze Data
1. Gathering Data
   1. The WeRateDogs Twitter archive.
   2. The tweet image predictions
   3. Twitter API
2. Asessing Data
   1. At least 8 Quality Issues
   2. At least 2 Tidiness Issues
3. Cleaning Data
4. Storing Data
5. Analyzing Data
6. Visualizing Data

Gathering, assessing, cleaning, storing, analyzing and visualzing efforts are documented in [Wrangle Act](https://github.com/kbhardwaj27/Wrangle-And-Analyze-Data/blob/master/wrangle_act.ipynb)

[Wrangle Report](https://github.com/kbhardwaj27/Wrangle-And-Analyze-Data/blob/master/wrangle_report.ipynb) describes my wrangling efforts briefly.

[Act Report](https://github.com/kbhardwaj27/Wrangle-And-Analyze-Data/blob/master/act_report.pdf) communicates the insights and displays the visualizations produced from the wrangled data.

#### Project Motivation
This project was part of the [Data Analyst Nanodegree](https://d20vrrgs8k4bvw.cloudfront.net/documents/en-US/nd002-syllabus_2018-June_v9.pdf?utm_campaign=acq_100_auto_ndxxx_syllabus_global&utm_source=blueshift&utm_medium=email&utm_content=acq_100_auto_ndxxx_auto-syllabus_global&bsft_clkid=e35bb41c-6de3-4fd8-a8be-98fde6853f64&bsft_uid=c298ccd0-50bd-484b-9481-d45b3ac669f8&bsft_mid=13f86b25-7b59-4122-8af9-19e22212dcab&bsft_eid=063b0846-68f4-0fd6-1512-dae12f602902&bsft_txnid=a274ee4a-7f22-412e-80ef-a9b8bbddd46a)

Your goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses 
and visualizations. The Twitter archive is great, but it only contains very basic tweet 
information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy 
analyses and visualizations.

#### The Data
##### Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not 
everything. One column the archive does contain though: each tweet's text, which I used to extract 
rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter 
archive "enhanced." Of the 5000+ tweets, I have filtered for tweets with ratings only (there are 2356).

I extracted this data programmatically, but I didn't do a very good job. The ratings probably 
aren't all correct. Same goes for the dog names and probably dog stages (see below for more 
information on these) too. You'll need to assess and clean these columns if you want to use 
them for analysis and visualization.

The Dogtionary explains the various stages of dog: doggo, pupper, puppo, and floof(er)

##### Additional Data via the Twitter API
Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable 
column omissions. Fortunately, this additional data can be gathered by anyone from Twitter's API. 
Well, "anyone" who has access to data for the 3000 most recent tweets, at least. But you, because 
you have the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this 
data for all 5000+. And guess what? You're going to query Twitter's API to gather this valuable data.

##### Image Predictions File

One more cool thing: I ran every image in the WeRateDogs Twitter archive through a neural network 
that can classify breeds of dogs*. The results: a table full of image predictions (the top three only) 
alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction 
(numbered 1 to 4 since tweets can have up to four images).

So that's all fun and good. But all of this additional data will need to be gathered, assessed, 
and cleaned. This is where you come in.
