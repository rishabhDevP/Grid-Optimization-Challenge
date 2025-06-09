#  Grid Optimization Challenge – IIIT Bhagalpur (Enyugma 2025)

This repository contains the solution to the [Grid Optimization Challenge](https://www.kaggle.com/competitions/grid-optimization-challenge-iiit-bhagalpur-enyugma) hosted on Kaggle as part of the Enyugma 2025 event by IIIT Bhagalpur. The challenge is focused on predicting the stability of an electrical grid system using machine learning techniques.

---

##  Problem Statement

Participants are required to predict the **`stab`** value — a numerical indicator of the linear stability of a grid system — based on features related to power generation, consumption, and response times of participants in the system.

---

##  Dataset Overview

The dataset includes the following files:

- `train.csv`: Contains features and target `stab`
- `test.csv`: Contains only features (target to be predicted)
- `sample_submission.csv`: Format to be used for predictions

### Features include:

- `tau[x]`: Reaction time for producer/consumers (e.g., `tau1`, `tau2`, ...)
- `p[x]`: Nominal power produced or consumed (e.g., `p1`, `p2`, ...)
- `g[x]`: Price elasticity coefficients
- `stab`: Target variable (real number)
- `stabf`: Stability label (categorical: `'stable'` or `'unstable'`)

---

##  Solution Overview

The solution pipeline consists of:

1. **Data Exploration**  
   - Feature correlation with `stab`
   - Distribution of stability labels (`stabf`)
   
2. **Preprocessing**  
   - Feature selection and scaling using `StandardScaler`
   - Dropping non-numeric or non-essential columns

3. **Modeling**  
   - Trained a `LightGBMRegressor` for predicting `stab`
   - Used 5-Fold Cross-Validation to ensure generalization

4. **Submission**  
   - Generated a CSV file with predictions for the test set
   - Format aligned with `sample_submission.csv`

---

##  Getting Started

To run this project locally or on Kaggle:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/grid-optimization-challenge.git
   cd grid-optimization-challenge

2.   Run the notebook on Kaggle or locally with:
   jupyter notebook grid_optimization_solution.ipynb

4. Download or submit the generated submission.csv.

**Contact**
Feel free to open issues or reach out via mishra.rishabh11@gmail.com for questions or collaboration.


---

Let me know if you'd like:
- The final `.ipynb` notebook linked in the README
- To include results from feature importance plots
- A short demo GIF or chart

I'll help you finalize it.

