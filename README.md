# Market_Basket_Analysis

- Market Basket Analysis is a analysis technique which identifies the strength of association between pairs of products purchased together and identify patterns of co-occurrence.

- Market Basket Analysis creates If-Then scenario rules (association rules), for example, if item A is purchased then item B is likely to be purchased. The rules are probabilistic in nature or, in other words, they are derived from the frequencies of co-occurrence in the observations. Frequency is the proportion of baskets that contain the items of interest. The rules can be used in pricing strategies, product placement, and various types of cross-selling strategies.

- This analysis uses 'Online Retail' data from UCI data collection, and is aimed provide a background on Apriori algorithm, and a practical implementation of the same via Python.

## Apriori Algorithm
- Apriori algorithms is a data mining algorithm used for mining frequent itemsets and relevant association rules. It is devised to operate on a database that contain transactions -like, items bought by a customer in a store.

- An itemset can be considered frequent if it meets a user-specified support threshold. For example, if the support threshold is set to 0.5(50%), a frequent itemset is a set of items that are bought/purchased together in atleast 50% of all transactions.

## Association Rules
Association rules are a set of rules derived from a database, that can help determining relationship among variables in a large transactional database. It identifies frequent if-then associations, which themselves are the association rules.

An association rule has two parts: an antecedent (if) and a consequent (then). An antecedent is an item found within the data. A consequent is an item found in combination with the antecedent.

Since multiplie rules are possible even from a very small database, i-order to select the most relevant ones, we use constraints on various measures of interest. The most important measures are discussed below. They are:

### Support
The Support of an itemset X, supp(X) is the proportion of transaction in the database in which the item X appears. It signifies the popularity of an itemset.

    supp(X) = (Number of transactions in which X appears)/(Total number of transactions)
We can identify itemsets that have support values beyond this threshold as significant itemsets.

### Confidence
Confidence of a rule signifies the likelihood of item Y being purchased when item X is purchased.

Thus, 

    conf(X -> Y) = supp(X U Y) / supp( X )

If conf (X -> Y) is 75%, it implies that, for 75% of transactions containing X & Y, this rule is correct. It is more like a conditional probability, P(Y|X), that the probability of finding itemset Y in transactions fiven that the transaction already contains itemset X.

### Lift
Lift explains the the likelihood of the itemset Y being purchased when itemset X is already purchased, while taking into account the popularity of Y.

Thus, 

    lift (X -> Y) = supp (X U Y)/( supp(X) * supp (Y) )

If the value of lift is greater than 1, it means that the itemset Y is likely to be bought with itemset X, while a value less than 1 implies that the itemset Y is unlikely to be bought if the itemset X is bought.

### Conviction
The conviction of a rule can be defined as :

    conv (X->Y) = (1-supp(Y))/(1-conf(X-Y))
If the conviction means 1.4, it means that the rule X -> Y would be incorrect 40% more often if the association between X & Y was an accidental chance

## Conclusion
With this kind of analysis from the field of mareting you can now determine which products are most often bought in combination with each other. With this knowledge it is possible to arrange the products efficiently in the store. In the best case, products that are often bought together are positioned in the opposite direction in the store so that customers are forced to walk past as many other products as possible.

Furthermore, one can now consider targeted discount campaigns. If you discount a product that is often bought in combination with others, you increase the chance of buying these products in combination, whereby a small discount is granted on only one.
