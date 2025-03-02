# **Voting-Based Ensemble Methods**  

Voting-based ensemble methods combine predictions from multiple models to improve accuracy and robustness.  

---

## **1️⃣ Max Voting**  
✔ **Used for Classification Problems**  
✔ Multiple models predict the class label for each data point.  
✔ Each model’s prediction is considered a **vote**.  
✔ The **majority class** is chosen as the final prediction.  

🔹 **Example:**  
If 3 models predict:  
- Model 1 → Class **A**  
- Model 2 → Class **B**  
- Model 3 → Class **A**  

**Final Prediction** = Class **A** (since A has the most votes).  

📌 **Best When?**  
✔ Models have **diverse learning patterns**.  
✔ Works well when models have **similar accuracy levels**.  

---

## **2️⃣ Averaging Voting**  
✔ **Used for Regression & Probability-Based Classification Problems**  
✔ Takes the **average of predictions** from all models.  
✔ Helps to **smoothen predictions** and reduce variance.  

🔹 **Example (Regression)**:  
- Model 1 → **4.2**  
- Model 2 → **4.8**  
- Model 3 → **5.0**  

**Final Prediction** = **(4.2 + 4.8 + 5.0) / 3 = 4.67**  

🔹 **Example (Classification with Probabilities):**  
For Class A:  
- Model 1: **0.6**  
- Model 2: **0.7**  
- Model 3: **0.8**  

**Final Probability** = (0.6 + 0.7 + 0.8) / 3 = **0.7**  

📌 **Best When?**  
✔ Works well with **continuous values (regression)**.  
✔ Useful when models output **probabilities** instead of labels.  

---

## **3️⃣ Weighted Average Voting**  
✔ **Used for Both Classification & Regression**  
✔ Assigns **different weights** to each model based on its performance.  
✔ Models with **higher accuracy** get **higher weight** in the final decision.  

🔹 **Example (Regression, Weighted Average):**  
- Model 1 → Prediction: **4.2**, Weight: **0.3**  
- Model 2 → Prediction: **4.8**, Weight: **0.5**  
- Model 3 → Prediction: **5.0**, Weight: **0.2**  

**Final Prediction** = (4.2 × 0.3) + (4.8 × 0.5) + (5.0 × 0.2) = **4.66**  

🔹 **Example (Classification with Probabilities, Weighted Average):**  
For Class A:  
- Model 1: **0.6**, Weight: **0.3**  
- Model 2: **0.7**, Weight: **0.5**  
- Model 3: **0.8**, Weight: **0.2**  

**Final Probability** = (0.6 × 0.3) + (0.7 × 0.5) + (0.8 × 0.2) = **0.69**  

📌 **Best When?**  
✔ Some models **perform better than others** and need **higher influence**.  
✔ You have performance metrics to assign **weights effectively**.  

---

# **Comparison of Voting Methods**  

| Method | Type | Works Best for | How it Works |
|--------|------|---------------|--------------|
| **Max Voting** | Classification | Models with similar accuracy | Chooses class with the most votes |
| **Averaging Voting** | Regression & Classification (probabilities) | Smoothing predictions | Takes the average of all model predictions |
| **Weighted Average Voting** | Regression & Classification | Models with different accuracies | Assigns higher weight to stronger models |

---
