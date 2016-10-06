Assignment 1:

based on overview and observation, the procedure in which the null and alternative hypothesis is formulated and the data is evaluated is seems correct. 

Assignment 2:

Statistical Analyses	IV(s)	IV type(s)	DV(s)	DV type(s)	Control Var	Control Var type	Question to be answered	H0	alpha	link to paper 
Chi-square	celldivision	Cell
Divisionper intervals	Rate of mutation Family patternIndividual development	Family patternIndividual development	Fixed family size	Multiplefamily sizes	Estimate biological mutation rates	Mutation of of the family is same 	1%and3%
See table-4	http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0135398

T test	differentially expressed genes	complex human background at concentrations	Hybridzations of Spike in genes	differentially expressed genes	Group Replicates		Compute false positiva rate	 that the expected values of expression for a given gene are equal between two groups of interest	5%	http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0012336




Assignment 3:
#Null Hypothesis: The % of former prisoners employed after release
#is the same or lower for candidates who participated in the program
#as for the control group. significance level p=0.05
#Ho: Po-P1 >= 0 
#Ha: Po-P1 < 0

We set the population ratios,and find ratios. Then asses the significance using z-test. To do this test we calculate sample proportion p to calculate standard error. With that z test can tell how far away from the mean our data is. Also calculated is the p value which in this case tells us Null hypthesis is rejected.

In the case that the inmate was or was not conviected to a felony, z value is less or greater than -1.873 and the pvalue is less than alpha and the null hypothesis rejected. However, the chisq test finds that Null hypthesis holds since chi_value 436.223 is not smaller than the critical value 0.38 which is obtained using table.

In this homework probalem, with the chisq practice I used the def evalChisq(values) method based on the recommendation and the work from Matt Sloan.

#Assignment 4: Tests of correlation using the scipy package with citibike data.
#Pearson’s test
#Spearman’s test
#K-S test
#Use: age of bikers for 2 genders. State your result in 
#words in terms of the Null Hypothesis
#You must state the Null Hypothesis, according to what you know about the test 
#and the scipy.stats package documentation for three scipy.stats function, 
#corresponding to the three tests.
#You must put the caluclated statistics and the p-value in the context
#of null hypothesis rejection in each case.

#Solution includes data from February 2015 : We will assume there is no difference or it is same between population proportion
#This makes the null hypothesis a two tail test so as long as there is an extreme
#value on either side beyond 2sigma alpha=0.05 null hypo will not hold

#Ho: Distribution of ages same or lower for men riders than women

#H1: The citybike men riders are greater than women riders

#Ho - H1 >= 0
#Ho - H1 < 0

#Followed the instrutions and plotted histograms with pandas than pylab
#If we take this age split every 5 years, it seems most men riders are between 30-35 whereas
#with women most riders are 25 to 30
#Also, quick observation from the histrograms show that with in that using this two groups 
#Women riders are observed from the histrograms to be approximately 1/5 th of men riders

#Normalized Cumulative Distributions
#What we see in the plot is the age gap that widens between men and women beginning from
#25 until about 35 and the gap closes down. Age gap merges approximately at 55. Meaning same 
#number of men and women ride city bike at 55 and beyond
#What's also interesting is that men and women pick citybikes about the same ages in early 20s
#but the men ride citybikes more frequently until later ages than women


KS Correlation: Ks_2sampResult(statistic=0.08478881431969218, pvalue=4.5875015783108826e-172)

#This will compute stats of 2 samples from the same distribution
#It will return the KS statistics and the two tailed p-value
#In the case that the KS is small or the p-value is high null hypthesis can not be
#rejected. Source: http://docs.scipy.org/doc/scipy-0.15.1/reference/generated/scipy.stats.ks_2samp.html
#At  aplha  = 5% KS is higher and p-value is less then 0.05 so we can reject the null hypothesis in this case
#Double checking this with the critical value table given in the instructions: Ks= 0.0847 C(a)=1/0.0847=11.806
#Since 11.806 is not less than 1.36 c(a) than KS permits null rejection

Ks with a sample data 1 in every 200: Ks_2sampResult(statistic=0.008022192182034541, pvalue=0.058515246189746364)
#Redo the test with a subsample of the data
#Here the KS statistic for this two samples is small and the pvalue is high
#Null hypothesis can not be rejected since pvalue is high at 5.8%
#compared to 5% alpha
#Subset data we have choosen holds Null hypothesis true

#Pearson's test for correlation 
#The p-value roughly indicates the probability of an uncorrelated system 
#pearson test indicates an exact monotonic inversely proportional correlation
#Pvalue is greater than aplha 0.05 indicating the null hypothesis holds

#Spearman's test for correlation - assumes no normal distribution: 
SpearmanrResult(correlation=-0.0040072154028195665, pvalue=0.46622939814840048)
#these datasets-Source: docs.scipy scipy.stats.spearmanr
#spearsman test indicates an exact monotonic inversely proportional correlation
#Pvalue is greater than aplha 0.05 indicating the null hypothesis holds


