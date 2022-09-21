# Association-Rule-Mining
This is a type of unsupervised learning involving Market Basket Analysis on groceries to determine which items are likely to be bought together.
This activity involves association rule mining using Apriori algorithm on the Groceries
dataset downloaded from Kaggle. The first step after loading the data, is data exploration
and some visualization to understand the dataset in terms of its shape, if there are missing
values, the columns of the dataset etc. It turned out that this particular dataset does not
need much of preprocessing because it does not have noise and is smaller in size.
The second step is to rescale the dataset by transforming it to one-hot encoded user-item
matrix. This eases the process of Market Basket Analysis because transactions are in a
better format. There are three attributes in this dataset, that is,Member_number, Date and
itemDescription. An assumption is that when a single user purchased different items on a
single date, then those items are considered to be one transaction.
The last step is to call the Apriori algorithm by defining the threshold values for the
support, confidence and lift. The Apriori algorithm finds the frequent itemsets, those that
have support equal to or greater than the minimum support value. It then finds the
association rules among the frequent itemsets and filters strong rules, those rules that
have confidence and lift values that are greater than or equal to the defined thresholds.
The final rules are printed together with their confidence and lift.
To establish the accuracy of Apriori algorithm, Predictive Accuracy could be used to
measure it. Predictive Accuracy can be defined as: Let D be a data file with n number of
records. If [x y] is an Association Rule which is generated by a static process P then the
predictive accuracy of [x y] is c([x y])=P[n] satisfies y|n [satisfies x]where distribution of
r is governed by the static process P and the Predictive Accuracy is the conditional
probability of xn and yn.
Given a dataset, Predictive Accuracy can provide the accuracy of the Apriori algorithm
on the dataset in terms of the percentage.
## Challenges
1. The challenge of this model is that Apriori algorithm is less efficient as it consumes
more space and is somewhat slower as compared to ECLAT and F-P Growth algorithms.
This is because it makes many iterations on the dataset to produce the frequent itemsets
and the strong association rules, and it takes much time to hold candidate sets with many
frequent itemsets.
2. Another challenge is that it is not easy to establish the threshold values for the Apriori
algorithm and it is difficult to establish the accuracy of unsupervised learning as
compared to supervised learning
