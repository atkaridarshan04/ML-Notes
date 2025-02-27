# Logistic Regression

**For Logistic Regression to be applied the data must be Linearly Seperable**

- Logistic regression is one of the most popular Machine Learning algorithms, which comes under the Supervised Learning technique.
- It is used for predicting the categorical dependent variable using a given set of independent variables.
- Therefore, the outcome must be a categorical or discrete value. It can be either Yes or No, O or 1, true or  alse, etc. but instead of giving the exact value as O and 1, it gives the probabilistic values which lie between O and 1.

## Types of Logistic Regression

On the basis of the categories, Logistic Regression can be classified into three types:
- **Binomial:** In binomial Logistic regression, there can be only two possible types of the
dependent variables, such as O or I, Pass or Fail, etc.
- **Multinomial:** In multinomial Logistic regression, there can be 3 or more possible unordere
types of the dependent variable, such as "cat", "dogs", or "sheep".
- **Ordinal:** In ordinal Logistic regression, there can be 3 or more possible ordered types of
dependent variables, such as "Iow , Medium", or "High"

## Sigmoid Function
Logistic Regression works on Sigmoid Function

Sigmoid follows **Binary Class Classification**

    y = 1 / (1 + e^-x)
where:
- y = independent
- x = dependent
- e (Euler's Constant) = -2.71828

![image.png](sigmoid.png)


## **OVR (One-Versus-Rest) Method**  
The **One-Versus-Rest (OVR)** method is a classification strategy used in multi-class classification problems. Instead of treating all classes simultaneously, it breaks down the multi-class problem into multiple binary classification problems.

#### **How It Works:**  
1. Suppose you have \(N\) classes.  
2. For each class \(i\), a separate binary classifier is trained to distinguish between:
   - **Class \(i\)** (as positive)
   - **All other classes** (as negative)  
3. At inference, each classifier outputs a probability or score, and the class with the highest score is chosen.

#### **Example:**
If we have three classes (A, B, and C), we create three binary classifiers:
- Classifier 1: A vs. (B and C)
- Classifier 2: B vs. (A and C)
- Classifier 3: C vs. (A and B)  
At prediction time, we take the classifier that outputs the highest probability.


## **Softmax Function**  
The **Softmax function** is commonly used in multi-class classification problems where the goal is to output probabilities over multiple classes.

---

### **OVR vs. Softmax**
| Feature | OVR | Softmax |
|---------|----|--------|
| **Approach** | Multiple binary classifiers | Single multi-class classifier |
| **Output** | Multiple independent scores | Probability distribution |
| **Computation** | Slower (requires \(N\) models) | Faster (single model) |
| **Use Case** | Works well with SVMs, logistic regression | Common in neural networks |

---