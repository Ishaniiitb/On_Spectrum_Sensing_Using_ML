# On Spectrum Sensing Using Machine Learning

This project proposes a machine learning-based approach for **spectrum sensing** in **Cognitive Radio Systems**, aimed at improving the efficiency of radio spectrum usage. The solution simulates the behavior of primary users in a communication channel and classifies channel occupancy using supervised learning models.

## 📌 Problem Statement

Due to the explosion in wireless communication, radio spectrum—a finite resource—is becoming increasingly congested. Traditional static allocation leads to underutilization and inefficiency. This project applies machine learning to dynamically assess and allocate frequency channels by sensing whether a channel is occupied by a primary user or not.

## 🧠 Objective

Build a system that:
- **Detects spectrum occupancy** using energy statistics.
- **Classifies channels** as occupied (reserved for primary users) or free (available to secondary users).
- Uses **ML classifiers** such as:
  - Random Forest
  - Support Vector Machine
  - Logistic Regression
  - K-Nearest Neighbors
  - Naive Bayes
  - Decision Tree

## 📂 Project Structure

On_Spectrum_Sensing_Using_ML/
│
├── SourceCode.ipynb # Main Jupyter notebook with dataset generation and ML models
├── README.md # Overview of the project
├── Final_Presentation.pptx # Project presentation slides
├── On_Spectrum_Sensing_a_...pdf # Full project report/paper


## ⚙️ How It Works

1. **Data Generation**: 
   - Simulates communication signals with or without primary users using statistical modeling.
   - Calculates **energy statistics** of received signals.
   - Applies **K-Means clustering** to label signals as occupied or free.

2. **Feature Engineering**:
   - Uses log-energy values.
   - Normalizes features for better classifier performance.

3. **Model Training**:
   - Uses a variety of ML classifiers.
   - Trains on simulated labeled datasets.

4. **Evaluation**:
   - Computes **confusion matrices** and **accuracy scores**.
   - Compares performance across models.

## 📊 Dataset

Generated synthetic datasets using custom parameters:
- 10,000 training samples
- 8,000 testing samples

Each sample includes:
- Energy statistic (float)
- Label (0: free, 1: occupied)

## 📈 Results

- Classifiers were evaluated using:
  - Confusion Matrix
  - Accuracy Score
  - Stratified K-Fold Cross-Validation
- Random Forest and SVM showed high performance and stability.

## 🛠 Dependencies

- Python 3.x
- NumPy
- scikit-learn
- Matplotlib (for visualization)

## ▶️ Run Instructions
Clone the repository or unzip the project.

Open SourceCode.ipynb in Jupyter Notebook.

Run the cells sequentially to:

Generate data

Train models

Evaluate performance

## 📚 References
Based on the paper: On Spectrum Sensing, a Machine Learning Method for Cognitive Radio Systems (included in the repo)

Techniques inspired by energy detection and ML classification methods used in signal processing.

## 👥 Authors
Ishan Jha and Aryan Mishra.

Install dependencies using:

```bash
pip install numpy scikit-learn matplotlib

