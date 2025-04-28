---

# Spam Classifier

This project is a spam classifier built to filter messages and accurately identify spam, including challenging email types with encoded content or heavy use of URLs.

## Overview

- **Dataset**: Downloaded, cleaned, and prepared for model training.
- **Preprocessing**:
  - Used `TfidfVectorizer` for feature extraction.
  - Developed a custom `EmailToWordCounter` transformer for additional text processing.
- **Modeling**:
  - Trained a `LogisticRegression` model, evaluated using `cross_val_score`.
  - Achieved approximately **97%** cross-validation accuracy, with:
    - **Precision**: 95.80%
    - **Recall**: 95.08%
- **Optimization**:
  - Used `GridSearchCV` to fine-tune hyperparameters.
- **Additional Experiments**:
  - Tried a `VotingClassifier` combining Logistic Regression, Random Forest, and Gradient Boosting, but it did not outperform the single Logistic Regression model.

## Conclusion

The final Logistic Regression model, optimized with `GridSearchCV`, provided strong performance and generalization ability for spam detection tasks.

---
