# 🧠 Fungi Classifier (Macro & Micro Images)

A deep learning pipeline for classifying fungal species using macro and micro image data. This project uses a Convolutional Neural Network (CNN) to identify patterns in fungal structures, enabling accurate species classification. It also includes statistical evaluations, visualization tools, and multiple experimental configurations.

---

## 📁 Project Structure
Both notebooks do the same thing but on diferent datasets: run (macro) and run_micro(micro).

Each notebook is organized into modular blocks:

- **Module Imports**  
  Loads all necessary Python libraries.

- **Hyperparameter and Parameter Configuration**  
  Sets model-related parameters (e.g., image size, data path, learning rate, etc.).

- **CNN Model Construction**  
  Defines the architecture of the CNN.

- **Model Training**  
  Trains the CNN using your dataset.

- **Model Evaluation**  
  Evaluates the trained model using medically relevant **diagnostic performance metrics** for multi-class classification:

- ✅ **Accuracy** – Overall proportion of correctly classified cases.
- 💉 **Sensitivity (TPR)** – Ability to correctly identify positive cases.
- 🛡️ **Specificity (TNR)** – Ability to correctly identify negative cases.
- 📈 **Positive Predictive Value (PPV)** – Proportion of predicted positives that are correct.
- 📉 **Negative Predictive Value (NPV)** – Proportion of predicted negatives that are correct .
- 🔄 **F1 Score** – Harmonic mean of Sensitivity and PPV, balancing precision and recall.

- **Run Model (Without Hyperparameter Tuning)**  
  Trains and evaluates the model with static parameters.

- **Run Model (With Hyperparameter Tuning)**  
  Uses automated tuning to find the best-performing parameters.

- **Additional Plots**  
  Produces visualizations of the data and training results.

- **Train/Test Split Experiment**  
  Measures performance with different train/test splits.

- **Confidence Interval Experiment**  
  Repeats training/testing 100 times to calculate mean, std, and metric distributions.

---

## ▶️ How to Use

0. **Select One Script**

1. **Prepare Your Dataset**
   - Place your images inside:  
     ```
     data/yourfoldername/
     ```

2. **Update Configuration**
   - In the notebook, change the `data_path` in the configuration block.
   - Modify other parameters (batch size, epochs, etc.) as needed.

3. **Customize the Model (Optional)**
   - Edit the CNN layers in the **CNN Model Construction** block.

4. **Initialize**
   - Run all blocks up to **Run Model** to load code and functions.

5. **Run Your Experiments**
   - Run Model without Hyperparameter Tuning  
   - Run Model with Hyperparameter Tuning  
   - Plot Data & Results  
   - Train/Test Split Experiment  
   - Confidence Interval Experiment

---

## 📊 Performance Metrics

The model is evaluated using the following classification metrics:

| Metric         | Description                                      |
|----------------|--------------------------------------------------|
| Accuracy       | Overall correctness of the model predictions     |
| Precision      | Macro-average precision across all classes       |
| Recall         | Macro-average recall across all classes          |
| F1 Score       | Harmonic mean of precision and recall (macro)    |
| Cohen’s Kappa  | Measures agreement adjusted for chance           |
| MCC            | Balanced metric even with imbalanced datasets    |

---

## 📌 Use Cases

- 🔬 **Biological Image Classification**  
  Classify fungal species using macro and micro image data.

- 📊 **Visual Data Exploration in Mycology**  
  Generate plots to analyze data distributions and class balances.

- 🧠 **Educational Tool for Deep Learning**  
  A practical example of CNN usage in biological contexts, ideal for teaching or self-study.

- 🧪 **Benchmarking for Scientific Research**  
  Use confidence interval experiments to assess model robustness across repeated trials.

- 📚 **AI in Life Sciences**  
  Demonstrates the application of machine learning in biological and ecological research domains.

---
To install:

pip install -r requirements.txt

---
## 👤 Authors

**Roland Bolboaca and Lenard Teri**  
