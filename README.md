# Intrusion-Detection-and-Automated-Response-System
___

## Cybersecurity – Intrusion Detection and Automated Response System

## Problem

As cyber threats become increasingly complex, organizations require intelligent systems to proactively detect and respond to malicious activities. You are tasked with building a **machine learning-based intrusion detection system (IDS)** using the **NSL-KDD dataset** to classify network traffic as normal or an attack.

To enhance your solution, you must integrate an **automated incident response** system that sends **email alerts** when an intrusion is detected. Your model will use a **Random Forest classifier** for detection and should achieve high accuracy on the test set.

---

## Input Format

You are provided with two CSV files:

* `KDDTrain+.csv`: Training dataset.
* `KDDTest+.csv`: Testing dataset.

Each row represents a connection record with 43 features, including categorical and numerical attributes, and a label indicating whether it is a normal connection or an attack.

---

## Constraints

* Input files are in CSV format and have no header row.
* Some columns are categorical and require encoding.
* The `class` label must be converted into binary format:

  * `normal.` → `0`
  * any attack label → `1`
* The system must:

  1. Train a model on the preprocessed dataset.
  2. Predict on test data.
  3. Send email alerts for each prediction classified as an attack.
  4. Display performance metrics and a confusion matrix.

---

## Output Format

The program should output:

* Model accuracy as a percentage.
* A detailed classification report (precision, recall, F1-score).
* Individual alert messages for predicted attacks (including index).
* A visual **confusion matrix** showing prediction results.
* Email notifications for every intrusion detected.

---

## Sample Output

```
Accuracy: 100.00%

              precision    recall  f1-score   support

           1       1.00      1.00      1.00     22544

    accuracy                           1.00     22544
   macro avg       1.00      1.00      1.00     22544
weighted avg       1.00      1.00      1.00     22544

⚠️ ALERT: Possible intrusion detected at index 0.
🚨 Alert email sent successfully!
...
✅ Normal traffic at index 5
...
```

---

## Evaluation Criteria

* Correct preprocessing (encoding, label binarization).
* High prediction accuracy.
* Functional automated email alert system.
* Effective visualization using seaborn.

---
