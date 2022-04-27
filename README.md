# EDA-Intermediate-Summarizing-Data-and-Deducing-Probabilities
### some statisitcs 
<br> infer-stat -> does our sample represent population and do some hypothesis and machine learning to test some hypothesis or even make ml model
<br> IQR -> says that 50% of data (Q3 (greater than 75% of data) -Q1(gtreater than 25% of data)) distributed in x values  
<br> ex. q1 = 20 & q3 = 60 --> so IQR is 40 means that 50% of data differentiate in just 40 value from 20 to 60. so thet are 21.22.24.30.35 and so on.
<br> variance is covariance between column with itself. but its always positive as we take power of 2 of the difference. 
<br> why? as its not imp to have neg or pos relation we just wanna know the jump BUT in covariance we wanna know if its pos * neg or neg * neg or pos * pos
<br> so pos * pos => pos relationship and so on.
### Performing Exploratory Data Analysis in Spreadsheets
### univar 
<br>  correlation measures the degree of a relationship between two variables (x and y), whereas regression is how one variable affects another
<br> first -> tool menu -> add analyses option
<br> tool -> data analyses -> descrptive stat to get all analyses you may need.
<br> neg **skewness** => skewed to the left
<br> neg **kurtosis** => has lighter tail 
<br> so some vis => select data -> insert -> chart 
<br> **grouping** using pivot table => insert -> pivot table -> select data -> sum so we add height to row so total sum for each hieght then change it to count 
<br> **to get frequency** then add height to agg again but as percent of total. 
<br> **binning**/bucketing => select first value in row tables -> group selection menu -> group by 12 as binning. so from 140 - 151 and so on.
<br> select pivot data on bucketing  -> insert -> pivot chart (default : historgram) 
<br> r-click on chart of historag -> change chart type to pie chart. -> r-click add data label -> r-click on element of chart and inc font size.
<br> click on pie chart -> fields of pivot table -> values -> change it to grant of total % 
### bi-var
<br> scatter plot for correlation 
<br> corr fun 
<br> or just tool-> data analyses->regression
<br> R square and adj R square -> how much variance in data  is captured by regression(straight line. of regression)
<br> regression tries to fit a strait line so formule is y=mx + c
<br> intercept is c in the prev formula.
<br> m is slope
<br> head size is value of m.
<br> the significance of result -> if pvalue is less than .05 and tstat is positive.
### multi-var 
<br> correlation -> tool -> data analyses -> correlation -> select whole data.
<br> better to use correlation as it has magintute bet 1 and -1 so normalized than co variance. 
<br> some vis -> insert -> pivot chart 
<br> check excel to find regression summary and total R square means .8 so data is correlated overall. 
### Summarizing Data and Deducing Probabilities Using Python
<br> Jupyter : Descriptive stat using numpy pandas and stats model 
<br> percentile:interpolation is lower so of q1 or q3 lies between 2 values will get lower of them.
<br> linear regression is same as correlation but regression allows us to predict new data. also correlation is relationship but regression measure how one var 
<br> affect the other one. (nearly the same.)
<br> default plot on two col is the scatter plot.
<br> Correlation is used to get association between two variables while (linear) regression is used to estimate the best straight line to summarise the association
<br> we can use both to find rel between 2 var.
<br> reg-> for predictions too.
<br> jupyter: regression with multi var data
<br> we do regression with 2 options 1- **ols** -> using stats model like we did in excel. 2-using ml model 
<br> ml linear reg: normalize = true means to make all values between 0 and 1.
<br> R square -> measure how far is pred data from straint line (original y-train.<we call it the output itself>)
### bayes rule  
<br> probability of **scenario based on other scenarios**.
<br> assume that all features are independant.
<br> prior probability is always based on original data means basiclly abd before anything there are probability to have runner on streat highter than police man
<br> also on titanic we take label on train set to get frequencey of survival for our prior probabilities of survival or death.
<br> so the prior probability is based on frequencey of the label we wanna predict itself.
<br> ==== in notenook it get frequencey of survived women as rule based and it give us probability of 72 % while bayes give us 79 % which is better 
<br> note that naive bayes model in python gives us conditional probability not prior so we took label in train set to calc prior probability then we dropped it 
<br> for our ml model to calc conditional probaility. 
<br> so note that depending on prior probability in our case without knowing gender would be very bad. as gender give us accuracy of 79 %
<br> conditional is got by multipling all conditional features in out case just gender.... then to get final * by prior. and other option of not survival * by prior. 
<br> https://www.geeksforgeeks.org/naive-bayes-classifiers/
### seaborn data visualizations  
### KDE plot
<br> notes from jupyter :
<br> seaborn is build on the top of matplot lib
<br> kde is just historgram and line over it (very simple.)
<br> make it false to just get histogram in seaborn.
<br> rug = true means to add actual data point values on the histogram. 
<br> define specific height to only show data points exists on data and ignore frequency bar.
<br> **bw** is the **bandwidth** of data representation. so when its smaller --> show more details.
<br> we can add many bandwidths as .1 and 1 as we did on jupyter.
#### bi variant analyses
<br> playing arround scatter plot 
<br> **hexbin** => so its is like scatter plot but point with high frequency is darker. 
<br> **join plot** -> scatter plot + frequencey plot.  <we can make scatter plot as hex plot too. in parameter : kind = hex .>
#### regresion plots
<br> **LM plot** shows **regresion** 
<br> using hue with LM make 2 lines for each elemnt of the hue 
<br> hue -> in english means color.
<br> size is categorical data (1,2,3,4,5,6)
<br> col option to filter and make 2 graphs. of regression
<br> hue and col on same col will make multiple graphs and each with different color.
<br> **Reg plot** is same as  LM plot  but has more flexibility it can accept  pandas series  and array as well.  
<br> **LM plot** just aceept pandas series. 
<br> **logistic** in reg plot = true means to make logistic regression : used for classification so will see aline which called **classification separator**. 
#### pairwise relationships 
<br> **pair plot** and pair grid => used to make visualization on multiple vars. 
<br> **pair grid** has more flexibility and options over pair plot
<br> **map_diag** => what chart on diagonal
<br> **map_off_diag** =>  what chart on NOT diagonal line.
#### visualize categorical data
<br> **strip plot** to work with categorical data 
<br> jitter = false : all data will be showed as single line 
<br> **swarm plot** => same as strip but without any overaloing of the points so you can see how many values clearly than overlaping in strip plot
<br> in swarm plot => palette : 'set1' and dodge = True if you wanna separate data based on the hue eg. if the hue is sex so male and female data will be separated.
<br> dpdge = false means to not separate and overlap.so charts will not be side by side but over each others.
<br> and not above each other and only color change . no all will be with diff color but in sep line.
#### box plot
<br> you can make multiple box plots on column based on filteration or values of other column eg sex so males and females will be 2 box plot for their grades foreg. 
<br> puting another column in the hue will make 2 box plot for each color too the same way as sex did in prev. so we have grades of males who are accepted 
<br> and plot of males who are rejected and same for females.
<br> **Violinplot** -> show the same as boxplot but it shows the distributtion of data based on KDE distribution.
<br> we can **mix swarm plot + box plot** th **show distribution** of data and **all data points too** using swarm plot.
#### catigorical plots 
<br> bar plot -> position of  line in the midle of it is the average.
<br> vertical line (line itself not the position of it ) is the error estimate which means uncertinity arround this estimates (avg)
<br> count plot => show frequency for cat data 
<br> ci = sd to make vertical line in bar plot be the standard deviation rather than error estimate.
<br> **cat plot ** the mean chart keyward and we say kind = .... may be box, line, point plot and others.
##### END 
