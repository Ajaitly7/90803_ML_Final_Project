# DonorsChoose Project Risk Model

Dataset: https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data 

This project supports DonorsChoose.org, a crowdfunding platform for public school teachers in the United States, by predicting which classroom projects are most at risk of not being fully funded before they expire. The platform currently relies on a digital content expert who can manually review only a small fraction of daily submissions, approximately ten percent. Our objective is to develop a predictive model that ranks projects by their likelihood of going unfunded, thereby helping allocate expert attention where it is most urgently needed.
   The analysis is based on data from the DonorsChoose 2014 KDD Cup, which includes structured, semi-structured, and unstructured features such as project costs, subject categories, grade levels, school-level poverty indicators, and essay content written by teachers. After merging, cleaning, and engineering features, we trained and evaluated three classification models: logistic regression, random forest, and XGBoost.
   Among the three, XGBoost achieved the strongest performance, with an area under the ROC curve of 0.69 and an F1 score of 0.79. It also demonstrated strong precision among the top ten percent of highest-risk predictions, which corresponds to the platform’s expert review capacity. Important predictive features included total project cost, resource quantity, and teacher experience on the platform.
   We recommend integrating this model into DonorsChoose’s project submission system to automatically identify high-risk proposals for review. This targeted intervention approach can help improve funding success rates, optimize limited human resources, and support more equitable educational opportunities.


---

## Code

- `MLF_project.ipynb` – The main Jupyter Notebook for data analysis and modeling.

## Datasets
- Dataset too large to push to github, rather visit ("https://drive.google.com/drive/folders/1USin0LLD1-w-SvOrU_2CohF_1_BxYk1U?usp=sharing")
- `datasets`: `projects.csv`, `outcomes.csv`, `essays.csv`, `resources.csv`, `donations.csv`

---


## Requirements

| Package               | Tested version |
| --------------------- | -------------- |
| Python                | 3.9 +          |
| numpy                 | ≥ 1.24         |
| pandas                | ≥ 2.0          |
| scikit‑learn          | ≥ 1.4          |
| xgboost               | ≥ 2.0          |
| imbalanced‑learn      | ≥ 0.11         |
| matplotlib            | ≥ 3.8          |
| seaborn               | ≥ 0.13         |
| geopandas             | ≥ 0.14         |


Install everything in one step:

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn geopandas
```

---

## Running the Notebook

1. **Clone the repo**

   ```bash
   git clone [https://github.com/<your‑user>/donorschoose-risk-model.git](https://github.com/Ajaitly7/90803_ML_Final_Project.git)
   ```

2. **Add the raw data**
   Download the five CSVs (`projects.csv`, `outcomes.csv`, `essays.csv`, `resources.csv`, `donations.csv`) from the Google Drive link and place them in a folder named `datasets/` at the project root.

3. **Launch Jupyter**

   ```bash
   jupyter notebook MLF_project.ipynb
   ```

   *(JupyterLab, VS Code, or any other Notebook front‑end works just as well.)*

4. **Run all cells**
   The notebook will

   * merge & clean the tables
   * engineer features
   * train logistic regression, random‑forest, and XGBoost models
   * print ROC/F1 metrics and show supporting plots.

