# **Association Rule Learning**

- Association rule learning is a machine learning technique used to discover interesting relationships or patterns in large datasets.
- It is often applied to transactional data, where items are bought or used together.

## **How Does Association Rule Learning Work?**

- Association rule learning works on the concept of an If-Then statement.
  - The "If" element is called the _antecedent_.
  - The "Then" statement is called the _consequent_.

## **Key Metrics in Association Rule Learning**

1. **Support**

   - The first step is to find frequently bought items.
   - It is a straightforward calculation based on frequency.
   - Formula:

     `Support(A) = Transactions(A) / Total Transactions`

2. **Confidence**

   - Measures how often item Y is purchased when item X is purchased.
   - Formula:

     `Confidence(X => Y) = P(Y | X) = Support(X n Y) / Support(X)`

     - (Number of transactions containing X and Y) / (Number of transactions containing X)

3. **Lift**

   - Given that different items are bought at different frequencies, lift helps determine the strength of the association.
   - Formula:

     `lift(X Y) = supp(X n Y) / supp(X) x supp(Y)`

   - **Interpretation:**
     - _Lift > 1:_ The two items are more likely to be bought together.
     - _Lift < 1:_ The two items are more likely to be bought separately.
     - _Lift = 1:_ No association between the two items.

## **Types of Association Rule Learning**

1. **Apriori Algorithm**
2. **Eclat Algorithm**
3. **F-P Growth Algorithm**

## **Applications of Association Rule Learning**

- **Market Basket Analysis**: Understanding which products are often bought together.
- **Medical Diagnosis**: Identifying relationships between symptoms and diseases.
- **Protein Sequence Analysis**: Detecting patterns in biological data.

---
