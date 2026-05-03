# PLT
Plant disease classification across multiple crops

# 🌿 Plant Disease Classification (PLT)

## 📌 Overview
This competition focuses on plant disease classification across multiple crops.

## 🎯 Task Description
Classify plant leaf images into 15 disease categories.

## 🏆 Objective
Accurately detect plant diseases from images.

## 🔗 Dataset Link
https://www.kaggle.com/datasets/emmarex/plantdisease

## 📂 Dataset Description
Derived from PlantVillage, covering multiple crops and diseases.

## 📁 Dataset Structure
train/, test/

### Public vs Private
train public, test labels private

## 🏆 Competition Leaderboard
The real-time rankings and model performance metrics for this competition are hosted on the official PLT dashboard.

[![View Leaderboard](https://img.shields.io/badge/View-Live_Leaderboard-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://tasneem-mselim.github.io/PLT/)

> **Note:** The leaderboard is updated automatically following each successful submission and evaluation cycle. Rankings are primarily sorted by **F1-Score (Macro)** to account for class balance.

---

### 📊 Evaluation Metrics
To ensure the robustness of the models, we evaluate participants based on:
*   **Accuracy:** Overall percentage of correct leaf classifications.
*   **F1-Score:** The harmonic mean of precision and recall (Macro-averaged), which is our primary ranking metric.

You can view the full statistical breakdown of all teams here: [Interactive Results Table](https://tasneem-mselim.github.io/PLT/)
Accuracy-based ranking


## 📝 Submission Format
Your model must output a CSV file named `submission.csv`. It must strictly follow this structure:

| id | label |
| :--- | :--- |
| img_1.JPG | 0 |
| img_2.JPG | 1 |

### 🔍 Constraints:
*   **ID Match:** The `id` must match the provided test image names exactly.
*   **Target Range:** `label` must be an integer.

---

## 🛠 How to Submit Your Results

Follow these steps precisely to ensure your submission is evaluated correctly.

### 1- Fork the Repository
Click the **Fork** button at the top right of this repository to create your own copy.

### 2- Prepare Locally
Navigate to the `submission/` folder in your local environment. Ensure you have the following files in one directory:
1.  `encrypt_submission.py` (Provided in the repo)
2.  `public_key.pem` (Provided in the repo)
3.  Your generated `submission.csv`

### 3- Encrypt Your Submission
Open your terminal or CMD in that folder and run the encryption command:

```bash
python encrypt_submission.py submission.csv submission.enc submission.enc.key public_key.pem
```

This will generate two files:

- `submission.enc` → the encrypted submission  
- `submission.enc.key` → encryption key  

Both files are required for submission. Do **not** submit the original CSV.

### 4- Place Encrypted Files in Submission Folder

Upload these files to the `submission/` folder in your forked repository

### 5- Create a Pull Request
Your submission will be reviewed and evaluated, and the results will be added to the leaderboard.


Only one submission is allowed for each participant. Subsequent submissions will be automatically rejected


## 📏 Evaluation Metric
Accuracy, F1-score

## ✅ Allowed
Augmentation, pretrained CNNs

## ❌ Not Allowed
External plant datasets

## 🧪 Baseline Model
Simple CNN

## 📚 References
PlantVillage Dataset

## 👩‍🏫 Organizer
Tasneem Selim
