# AAI-530-GROUP-1
### Members: Ali Abdul-Hameed, Jack Kim, Jinyuan He

## Project Overview

Wearable health devices are widely used in daily life. Most consumer-grade devices are equipped with only a tri-axial accelerometer and an optical heart-rate sensor based on photoplethysmography (PPG). Despite limited hardware, these devices can monitor dozens of health metrics. This capability is largely enabled by advanced algorithms and machine learning techniques, allowing manufacturers to produce cost-effective devices while maintaining a high-quality user experience.

This project focuses on analyzing IoT data collected from Fitbit wearable devices. We explore the data structure, temporal characteristics, and underlying behavioral patterns.

Several machine learning and time-series models are implemented:

- **Convolutional Neural Network (CNN)** for sleep status classification  
- **Long Short-Term Memory (LSTM)** network for activity-level classification  
- **ARIMA/SARIMA** models for calorie expenditure forecasting  

Due to the class imbalance problem in sleep status distribution, activity-level classification is introduced as an alternative predictive target. The project demonstrates how deep learning and classical time-series approaches can be applied to wearable IoT data for health behavior modeling and prediction.


## Results

### 1️⃣ Sleep Status Classification (CNN)

The Convolutional Neural Network (CNN) model was applied to classify sleep status into three categories: Asleep, Awake, and Restless.

- Overall Accuracy: ~0.90+
- High recall for majority class (Asleep)
- Lower recall for minority classes (Awake, Restless)

Due to significant class imbalance in the dataset, the model tends to favor the dominant sleep state. This indicates that while CNN can capture temporal patterns, imbalance handling techniques (e.g., class weighting or resampling) are necessary for more robust performance.

---

### 2️⃣ Activity-Level Classification (LSTM)

To address the imbalance issue in sleep status, activity-level classification was introduced as an alternative target.

The LSTM model achieved:

- Stable convergence during training
- Improved class separation compared to sleep classification
- Better recall balance across activity categories

This suggests that activity-level prediction is a more suitable classification target for this dataset structure.

---

### 3️⃣ Calories Expenditure Forecasting (ARIMA/SARIMA)

Classical time-series models (ARIMA/SARIMA) were applied to forecast calorie expenditure.

Findings include:

- Clear daily seasonality pattern
- Strong correlation between calories and activity intensity
- SARIMA captures periodic behavior effectively

---

### Key Observations

- Wearable IoT data contains strong temporal and behavioral patterns.
- Deep learning models (CNN/LSTM) are effective for classification tasks.
- Classical statistical models (ARIMA/SARIMA) remain competitive for structured seasonal forecasting.
- Target selection significantly affects classification performance.


## How to Run

```
1. Clone the repository:
   git clone https://github.com/CodingPro777/AAI-530-GROUP-1

2. Install dependencies:
   pip install -r requirements.txt

3. Open Jupyter Notebook:
   jupyter notebook

4. Run all cells in order.
```

or 

Run directly in Google Colab:
[Open in Colab](https://colab.research.google.com/github/CodingPro777/AAI-530-GROUP-1/blob/main/final_project_code.ipynb)


