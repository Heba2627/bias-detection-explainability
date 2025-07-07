# bias-detection-explainability
## 📊 Dataset
Structured data with features like:
- Age, ExperienceYears, InterviewScore, EducationLevel, etc.
- Label: `HiringDecision` (1 = Hire, 0 = No-Hire)
- Sensitive feature: `Gender` (1 = Male, 0 = Female)

## 🧠 Model
- **Logistic Regression** trained on gender-imbalanced data (80% male in training)
- Accuracy: **87.3%**

## ⚖️ Fairness Analysis
- Demographic Parity: 0.304 (M) vs 0.303 (F)
- Equal Opportunity: 0.826 (M) vs 0.768 (F)
- Average Odds Difference: 0.038

## 🧠 Explainability with LIME
- Gender did **not** influence individual predictions
- Top features: `SkillScore`, `InterviewScore`, `RecruitmentStrategy`

## 🔧 Bias Mitigation
- **Reweighing** via AIF360 improved fairness:
  - Average Odds Difference reduced to **0.028**
  - Equal Opportunity gap narrowed to **3.1%**
  - Accuracy preserved

## 📄 Report
See [`report.pdf`](./Uncovering Bias and Explaining Decisions in a Job.pdf) for full explanation, results, and charts.

## ▶️ How to Run
1. Clone the repo or download files
2. Open `Bias.ipynb` in Jupyter Notebook or Colab
3. Run all cells (install dependencies via `pip install -r requirements.txt` if needed)
