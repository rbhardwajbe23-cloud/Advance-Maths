# 📘 Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

## 👤 Submitted By
**Name:** (Your Name)  
**Roll Number:** 102303424  

---

## 📌 Assignment Overview

This assignment aims to learn the probability density function (PDF) of NO₂ air pollution data using a roll-number-based non-linear transformation. The transformed data is modeled using a Gaussian-like distribution, and its parameters are estimated using curve fitting techniques.

---

## 📂 Dataset

- **Dataset:** India Air Quality Data  
- **Feature Used:** NO₂ concentration (x)  
- **Source:** https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data  

---

## ⚙️ Methodology

The NO₂ data is extracted from the dataset and preprocessed by removing missing values. A roll-number–based sinusoidal transformation is applied to generate a new variable. The empirical distribution of the transformed data is obtained using a normalized histogram. A Gaussian-like probability density function is assumed and its parameters are estimated using curve fitting. The fitted PDF is then visualized along with the histogram to evaluate the model fit.

---

## 🔢 Transformation Details

The transformation applied is:

z = x + a_r sin(b_r x)

where:

a_r = 0.05 (r mod 7)  
b_r = 0.3 ((r mod 5) + 1)

For roll number r = 102303424:

- r mod 7 = 0  →  a_r = 0.05 × 0 = 0.00  
- r mod 5 = 4  →  b_r = 0.3 × (4 + 1) = 1.5  

Therefore,

z = x + 0 · sin(1.5x) = x  

The transformation does not change the original data.

---

## 📈 Probability Density Model

The assumed probability density function is:

p̂(z) = c · e^(−λ (z − μ)²)

Where:

- μ (Mu) → Mean of the data  
- λ (Lambda) → Controls spread of distribution  
- c → Scaling constant  

---

## 📊 Parameter Estimation

The parameters were estimated using non-linear least squares curve fitting on the histogram density of the transformed data.

### Estimated Parameters

| Parameter | Description | Estimated Value |
|----------|------------|----------------|
| λ (Lambda) | Controls spread of distribution | Obtained via curve fitting |
| μ (Mu) | Mean of transformed data | Obtained via curve fitting |
| c | Scaling constant | Obtained via curve fitting |

*(Insert your numerical results here)*

---

## 📉 Result Graph

The output includes:

- Histogram of transformed variable z  
- Fitted Gaussian-like PDF curve  

Insert generated plots below:

<img width="633" height="470" alt="image" src="https://github.com/user-attachments/assets/5bda8c03-8337-4c47-a853-05fce528f2a4" />

<img width="624" height="470" alt="image" src="https://github.com/user-attachments/assets/19389ace-4cfd-4c24-b0b2-840ffeb36199" />

---

## ✅ Conclusion

A roll-number-dependent transformation was applied to NO₂ data, and a Gaussian-like probability density function was successfully learned using curve fitting. For roll number 102303424, the transformation parameter resulted in no modification of the original data, and the fitted model accurately represents the empirical distribution.

---

## 🛠️ Tools & Libraries Used

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- SciPy  

---

## ▶️ How to Run

1. Download the dataset and save it as `data.csv`.
2. Place the file in the project directory.
3. Run the provided Python script.
4. The program will display:
   - Histogram of transformed data
   - Fitted probability density function
   - Estimated parameters

---
