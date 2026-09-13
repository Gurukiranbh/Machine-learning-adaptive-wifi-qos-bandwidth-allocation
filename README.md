# 📡 Adaptive Wi-Fi Bandwidth Allocation Using Machine Learning

> 🚀 An intelligent Machine Learning-based system for **adaptive Wi-Fi bandwidth allocation and Quality of Service (QoS) priority prediction** using real-time network parameters such as **Delay, Packet Loss, and Throughput**.

---

## 🌐 Overview

Wi-Fi networks connect a large number of devices including smartphones, laptops, IoT devices, and other connected systems. As the number of users increases, network congestion can lead to:

- ⏱️ Increased delay
- 📦 Higher packet loss
- 🚀 Reduced throughput
- 📉 Poor Quality of Service (QoS)
- 😕 Reduced user experience

Traditional Wi-Fi bandwidth allocation methods generally depend on fixed rules and are unable to adapt effectively to changing network conditions.

This project proposes a **Machine Learning-based adaptive Wi-Fi bandwidth allocation system** that analyzes key QoS parameters and predicts the priority of a network connection.

The system uses:

- ⏱️ **Delay**
- 📦 **Packet Loss**
- 🚀 **Throughput**

to classify network priority into:

🔴 **High Priority**  
🟡 **Medium Priority**  
🟢 **Low Priority**

The predicted priority is then mapped to an appropriate **bandwidth allocation recommendation**.

---

## 🎯 Objectives

- 🤖 Develop an adaptive Wi-Fi bandwidth allocation system using Machine Learning.
- 📊 Predict network priority as **High, Medium, or Low**.
- ⏱️ Analyze network **Delay**.
- 📦 Analyze **Packet Loss**.
- 🚀 Analyze **Throughput**.
- 🌳 Implement and evaluate a **Decision Tree** classifier.
- 🌲 Implement and evaluate a **Random Forest** classifier.
- 📈 Compare both models using multiple performance metrics.
- 🖥️ Develop an interactive **Streamlit dashboard**.
- 📶 Provide bandwidth allocation recommendations based on predicted network priority.
- 🔍 Analyze feature importance and model overfitting.

---

## ✨ Key Features

- 📡 Adaptive Wi-Fi bandwidth allocation
- 🤖 Machine Learning-based QoS prediction
- ⏱️ Delay analysis
- 📦 Packet loss analysis
- 🚀 Throughput analysis
- 🌳 Decision Tree classification
- 🌲 Random Forest classification
- 🧪 Synthetic dataset generation
- 🔧 Feature engineering
- 🎯 High / Medium / Low priority classification
- 🔄 80:20 train-test split
- 🔁 Five-fold cross-validation
- 📊 Accuracy, Precision, Recall and F1-Score evaluation
- 🔍 Feature importance analysis
- ⚠️ Overfitting analysis
- 📈 Model comparison
- 🖥️ Interactive Streamlit dashboard
- 🎯 Real-time priority prediction
- 📶 Bandwidth allocation recommendation

---

## 🧠 Problem Statement

Traditional Wi-Fi bandwidth allocation uses fixed rules and cannot dynamically adapt to changing network conditions.

During network congestion, this can result in increased delay, packet loss, and reduced throughput.

Therefore, an intelligent system is required to:

```text
📡 Monitor Network Conditions
          ↓
📊 Analyze QoS Parameters
          ↓
🤖 Predict Network Priority
          ↓
📶 Recommend Bandwidth Allocation
          ↓
✨ Improve Network QoS
🏗️ System Architecture
                📡 Wi-Fi Network
                       │
                       ▼
        ┌─────────────────────────────┐
        │     Network Parameters      │
        │                             │
        │  ⏱️ Delay                   │
        │  📦 Packet Loss             │
        │  🚀 Throughput              │
        └──────────────┬──────────────┘
                       │
                       ▼
              🧪 Synthetic Dataset
                  Generation
                       │
                       ▼
             🎯 Priority Score
                Computation
                       │
                       ▼
              🏷️ Priority Labelling
                       │
                       ▼
                80:20 Split
              Train / Test Data
                       │
              ┌────────┴────────┐
              ▼                 ▼
      🌳 Decision Tree    🌲 Random Forest
              │                 │
              └────────┬────────┘
                       ▼
              📊 Performance
                 Evaluation
                       │
                       ▼
                 🏆 Best Model
                  Selection
                       │
                       ▼
              🎯 Priority Prediction
                       │
              ┌────────┼────────┐
              ▼        ▼        ▼
           🔴 High  🟡 Medium  🟢 Low
              │        │        │
              └────────┼────────┘
                       ▼
             📶 Bandwidth Allocation
                Recommendation
                       │
                       ▼
              🖥️ Streamlit Dashboard
📊 QoS Parameters

The Machine Learning models use three important network Quality of Service parameters.

Parameter	Range	Unit
⏱️ Delay	1 – 200	ms
📦 Packet Loss	0 – 20	%
🚀 Throughput	1 – 100	Mbps

These parameters are used to calculate a composite priority score for each generated network record.

🧮 Priority Score Calculation

The project calculates network priority using:

S = D/200 + L/20 - T/100

Where:

D = Delay
L = Packet Loss
T = Throughput
S = Composite Priority Score
📌 Priority Interpretation
⏱️ High Delay
      +
📦 High Packet Loss
      +
🚀 Low Throughput
      ↓
🔴 HIGH PRIORITY
Moderate Network Conditions
      ↓
🟡 MEDIUM PRIORITY
⏱️ Low Delay
      +
📦 Low Packet Loss
      +
🚀 High Throughput
      ↓
🟢 LOW PRIORITY
🧪 Dataset Generation

A public dataset containing Wi-Fi client sessions labelled according to the required priority classes was not available for this project.

Therefore, a synthetic QoS dataset was generated using realistic ranges of:

Delay
Packet Loss
Throughput

Each generated record is assigned a priority label using the composite priority score.

Dataset Workflow
📊 QoS Parameters
       ↓
🧪 Data Generation
       ↓
🧮 Priority Score
       ↓
🏷️ Priority Labelling
       ↓
📁 Training Dataset
🤖 Machine Learning Models
🌳 Decision Tree

The Decision Tree classifier uses threshold-based decisions on the three QoS parameters to classify network priority.

Advantages:

Easy to interpret
Lightweight inference
Simple decision structure
Suitable for low-dimensional feature spaces
🌲 Random Forest

Random Forest is an ensemble Machine Learning algorithm that combines multiple Decision Trees to improve generalization and reduce overfitting.

The Random Forest model was evaluated against the Decision Tree model to identify the better-performing classifier.

🔄 Machine Learning Pipeline
📁 Dataset
    ↓
🔧 Feature Selection
    ↓
✂️ Train-Test Split
    │
    └── 80% Training
    └── 20% Testing
    ↓
🤖 Model Training
    │
    ├── 🌳 Decision Tree
    └── 🌲 Random Forest
    ↓
📊 Performance Evaluation
    ↓
🔍 Model Comparison
    ↓
🏆 Best Model Selection
    ↓
🎯 Priority Prediction
    ↓
📶 Bandwidth Recommendation
🏆 Results & Performance

The experimental results show that Random Forest outperformed Decision Tree for network priority prediction.

📊 Metric	🌳 Decision Tree	🌲 Random Forest
🎯 Test Accuracy	89.40%	94.60%
🔄 5-Fold CV Accuracy	87.10%	92.90%
🚀 Major Result

Random Forest achieved:

94.60% test accuracy

compared with:

89.40% test accuracy

for Decision Tree.

This represents an improvement of:

⭐ 5.20 percentage points
🌳 Decision Tree
     89.40%
        │
        │ +5.20%
        ▼
🌲 Random Forest
     94.60%
🔍 Feature Importance

Feature importance was analyzed for both Machine Learning models.

🌳 Decision Tree
📦 Packet Loss   → 0.354
⏱️ Delay         → 0.340
🚀 Throughput    → 0.306
🌲 Random Forest
⏱️ Delay         → 0.362
📦 Packet Loss   → 0.327
🚀 Throughput    → 0.312

For the Random Forest model, Delay was the most influential feature, followed by Packet Loss and Throughput.

📈 Performance Evaluation

The models were evaluated using:

🎯 Accuracy

Measures the overall correctness of classification.

🎯 Precision

Measures the correctness of predicted priority classes.

🎯 Recall

Measures how effectively each priority class is identified.

🎯 F1-Score

Provides a balance between Precision and Recall.

🔄 Five-Fold Cross-Validation

Used to evaluate model stability across different data partitions.

⚠️ Overfitting Analysis

Model performance was analyzed by varying tree depth and Random Forest ensemble size.

🖥️ Streamlit Dashboard

An interactive Streamlit dashboard was developed to provide an accessible interface for network monitoring and Machine Learning predictions.

📊 Dashboard Features
📡 Network overview
🤖 Model comparison
🌳 Decision Tree analysis
🌲 Random Forest analysis
🎯 Live priority prediction
📈 Accuracy comparison
🔍 Feature importance visualization
🧩 Confusion matrix
📊 Performance metrics
📶 Bandwidth recommendation
🎯 Class probability visualization
🎯 Live Prediction

The dashboard allows users to enter network readings:

⏱️ Delay
📦 Packet Loss
🚀 Throughput

The system processes the input and provides:

Network Parameters
       ↓
🤖 Machine Learning Model
       ↓
🎯 Priority Prediction
       ↓
🔴 High / 🟡 Medium / 🟢 Low
       ↓
📶 Bandwidth Recommendation
📶 Adaptive Bandwidth Allocation

The predicted priority is mapped to a corresponding bandwidth allocation recommendation.

Priority	Network Condition	Bandwidth Recommendation
🔴 High	Poor / Congested	Highest Allocation
🟡 Medium	Moderate	Moderate Allocation
🟢 Low	Good	Lowest Allocation

The Random Forest model was selected to drive the bandwidth recommendation logic because of its higher accuracy and more balanced performance, while the Decision Tree model is retained for comparison and visualization.

🛠️ Technologies & Tools
💻 Programming
🐍 Python 3.x
💻 Visual Studio Code
🤖 Machine Learning
Scikit-learn
Decision Tree
Random Forest
Supervised Classification
Cross-Validation
Model Evaluation
📊 Data Processing
Pandas
NumPy
📈 Data Visualization
Matplotlib
Seaborn
🖥️ Dashboard
Streamlit
🔧 Techniques Used
🧪 Synthetic Dataset Generation
🔧 Feature Engineering
🌳 Decision Tree Classification
🌲 Random Forest Classification
🎯 QoS Priority Prediction
📶 Adaptive Bandwidth Allocation
✂️ 80:20 Train-Test Split
🔄 Five-Fold Cross-Validation
📊 Accuracy Evaluation
🎯 Precision Evaluation
🔍 Recall Evaluation
📈 F1-Score Evaluation
📊 Feature Importance Analysis
⚠️ Overfitting Analysis
🖥️ Real-Time Dashboard Visualization
💡 Advantages
⚡ Lightweight Machine Learning approach
📊 Uses only three important QoS parameters
🤖 Data-driven network priority prediction
📶 Adaptive bandwidth recommendations
🌲 Improved prediction performance using Random Forest
🖥️ Interactive Streamlit interface
🔍 Feature importance analysis
🔄 Cross-validation-based evaluation
💻 Python-based implementation
📡 Suitable for adaptive Wi-Fi QoS management
🌍 Potential Applications
📡 Wi-Fi network management
🏫 Campus networks
🏢 Enterprise networks
🏠 Smart home networks
📱 Multi-user wireless networks
🌐 Network congestion management
📶 QoS-aware bandwidth allocation
🖥️ Network monitoring systems
🤖 Intelligent network management
📊 Real-time network analytics
🔮 Future Scope
📡 Integration with live Wi-Fi telemetry
⚡ Real-time automatic bandwidth enforcement
🌐 Software Defined Networking (SDN) integration
🤖 Reinforcement Learning-based bandwidth allocation
🧠 Advanced Machine Learning models
📊 Larger real-world Wi-Fi datasets
☁️ Cloud-based network monitoring
📱 Mobile network monitoring
🔄 Continuous model retraining
🎯 More advanced QoS prediction techniques
📚 Technical Keywords
Machine Learning
Adaptive Wi-Fi
Wi-Fi QoS
Quality of Service
Adaptive Bandwidth Allocation
Bandwidth Allocation
Network Priority Prediction
Network Congestion
Delay
Packet Loss
Throughput
Decision Tree
Random Forest
Supervised Learning
Classification
Feature Engineering
Synthetic Dataset
Train-Test Split
Cross-Validation
Accuracy
Precision
Recall
F1-Score
Feature Importance
Overfitting Analysis
Python
Scikit-learn
NumPy
Pandas
Matplotlib
Seaborn
Streamlit
Real-Time Dashboard
Wireless Networks
IEEE 802.11
Network Optimization
QoS Management
📌 Project Information

📚 Subject: Computer Networks & Protocols
💡 Project Type: Problem-Based Learning (PBL)
🌐 Domain: Computer Networks + Machine Learning
🎯 Focus: Adaptive Wi-Fi Bandwidth Allocation & QoS Prediction
🤖 Models: Decision Tree & Random Forest
🖥️ Interface: Streamlit Dashboard
🐍 Language: Python

👨‍💻 Project Team
Gurukiran B H

Electronics & Communication Engineering

Nishaanth K S

Electronics & Communication Engineering

⭐ Project Highlights
📡 Adaptive Wi-Fi Bandwidth Allocation
🤖 Machine Learning-Based QoS Prediction
🌳 Decision Tree
🌲 Random Forest
🎯 High / Medium / Low Priority Classification
⏱️ Delay Analysis
📦 Packet Loss Analysis
🚀 Throughput Analysis
📊 94.60% Random Forest Test Accuracy
⭐ 5.20 Percentage-Point Improvement
🔄 Five-Fold Cross-Validation
🔍 Feature Importance Analysis
⚠️ Overfitting Analysis
🖥️ Streamlit Real-Time Dashboard
📶 Bandwidth Recommendation
🐍 Python + Scikit-learn
📖 References
Alvarado, R., Ospina, B., Tellez, J., & Triana, V., Dynamic Bandwidth Allocation with Machine Learning in Dense WiFi Network, FACETS, 2025.
Hao, X., She, C., Yeoh, P. L., Liu, Y., Vucetic, B., & Li, Y., Hybrid-Task Meta-Learning: A GNN Approach for Scalable and Transferable Bandwidth Allocation, IEEE Transactions on Wireless Communications, 2024.
Wilhelmi, F., Szott, S., Kosek-Szott, K., & Bellalta, B., Machine Learning & Wi-Fi: Unveiling the Path Towards AI/ML-Native IEEE 802.11 Networks, 2024.
Yi, P., Cheng, W., Ju, Z., Wang, J., Pan, J., Ouyang, Y., & Zhang, W., Fair AI-STA for Legacy Wi-Fi: Enhancing Sensing and Power Management with Deep Q-Learning, 2024.
Szott, S., Kosek-Szott, K., Gawłowicz, P., Gómez, J. T., Bellalta, B., Zubow, A., & Dressler, F., Wi-Fi Meets ML: A Survey on Improving IEEE 802.11 Performance with Machine Learning, 2021.
⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐ Star!
