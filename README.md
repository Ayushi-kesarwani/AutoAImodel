# 🚢 Titanic Survival Prediction using IBM Watsonx

This project predicts whether a passenger survived the Titanic disaster using machine learning and IBM Watsonx Studio. It uses the Titanic dataset and leverages AutoAI to build and deploy the best model.

---

## 📌 Project Details

- **Dataset**: Titanic Survival Dataset (`train.csv`)
- **ML Task**: Binary Classification
- **Target Column**: `Survived` (0 = No, 1 = Yes)
- **Platform**: IBM Watsonx.ai (AutoAI)

---

## 🧠 Features Used for Prediction

- `Pclass` (Passenger Class)
- `Sex`
- `Age`
- `SibSp` (Number of siblings/spouses aboard)
- `Parch` (Number of parents/children aboard)
- `Fare`
- `Embarked` (Port of Embarkation)

---

## 🛠️ How to Run the Project on IBM Watsonx Studio

1. Go to [IBM Watsonx.ai Studio](https://dataplatform.cloud.ibm.com/)
2. Create a **new project**
3. Upload the dataset (`train.csv`)
4. Click on **Add to project > AutoAI experiment**
5. Select `Survived` as the **target column**
6. Let Watsonx run and choose the best performing pipeline (e.g., P4)
7. Click **Save as model**
8. Go to **Assets > Models** and deploy the saved model
9. After deployment, use the **deployment URL & API key** to test predictions

---

## 📄 Sample Input for Testing (JSON)

```json
{
  "input_data": [{
    "fields": ["Pclass", "Sex", "Age", "SibSp", "Parch", "Fare", "Embarked"],
    "values": [[3, "female", 26, 1, 0, 7.925, "S"]]
  }]
}
