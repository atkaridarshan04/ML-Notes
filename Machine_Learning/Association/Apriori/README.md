# **Apriori Algorithm**

## **Introduction**
- The Apriori algorithm is a popular data mining technique used for association rule learning.
- It is used to identify frequent itemsets and derive association rules from them.
- It follows the "Apriori principle," which states that if an itemset is frequent, then all its subsets must also be frequent.

## **Working of Apriori Algorithm**
1. **Step 1: Set a Minimum Support Threshold**
   - Define the minimum support value to filter frequent itemsets.
   
2. **Step 2: Generate Frequent Itemsets**
   - Count the occurrence of individual items in transactions.
   - Remove items that do not meet the minimum support threshold.
   - Combine frequent items to form larger itemsets (pairs, triplets, etc.).
   
3. **Step 3: Pruning Using Apriori Principle**
   - Eliminate itemsets that have infrequent subsets.
   - Continue forming larger itemsets until no more frequent itemsets can be found.
   
4. **Step 4: Generate Association Rules**
   - Use confidence and lift metrics to extract strong association rules.
   - Rules are of the form: "If {Item A}, then {Item B}."
   
## **Key Metrics Used**
- **Support**: Frequency of itemset occurrence.
- **Confidence**: Strength of association between items.
- **Lift**: Relationship strength between itemsets.

---