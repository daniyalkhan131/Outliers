# Outliers

outliers is sharma ji ka bete
it is that point that behave very differently from other data
outliers easily can do wrong to our ML model, like mean will shift to high value when 
only one student have package in crores
in LR model our line get shift towards the point that is very far from other linear data

not always ouliers are dangerous, sometimes it is part of data that represent and sometimes
it is dangerous

when oultiers dangerous?
when like age is 300 so that is outlier
but in anamoly detetction like credit card fraud outliers are important because they are the
things we needed to detect
remove outliers or not need a lot of thinking, what is problem statement, or type of outliers
sometimes we handle outliers by adding another dimensionality and that make them to
be normal points

outliers affect these algo very much-
linear reg.
logistic reg.
adaboost
deep learning
in these algos weights are calculated, so can think that whether algo. is weight based, if
yes then outliers will affect

tree based algo. dont have impact of outliers
decision tree, random forest, gradient boosting, xgboost because they cut the space 

how to treat outliers?
1-trimming
	simple removing the outliers
	in this data get less or thin if more outliers
	it is fast
2- capping
	outliers can be having min. values or max. values but not in between like present in
tail of normal dist rather than in between, so replace min. ones with (your choice) min.
value like 1 or something and max. ones with max value like 90 or something

less used ones-
3- treat them as missing values and apply those techniques for handling missing values
4- use discretization


how to detect outliers?

1- if col. is normally distributed then 99.7% data comes in mean+-3*std so data other
that can be discarded

2- id col. is skewed dist. then use IQR to detect outliers

3- other distribution then can do like take 2.5 percentile as min point and 97.7 percentile
as max point.

4- winsurization


Z score outlier detection-
	col. should be nearly normal dist.
	tranform all x by appling (x-mean)/std
	then mean+-3std ke bahar walo ko trim or capping

using IQR-
	(IQR proximity rule)
	when data is skewed
		
percentile method-
	max value is 100percentile
	min value is 0percentile
	median is 50percentile
	now we can define any percentile for lower and upper value and detect oultiers
	capping in this method is called winsurization
