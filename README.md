# 🧠 Fungi Classifier (Macroscopic & Microscopic Images)

A deep learning pipeline for fungal species classification using both **macroscopic** and **microscopic** image data.

This project leverages Convolutional Neural Networks (CNNs) to detect patterns in fungal morphology, ranging from colony structures to microscopic features, enabling high-accuracy species identification.

### 🚀 Features
- 📊 Statistical evaluation tools  
- 📈 Interactive visualizations  
- 🔬 Multiple experimental configurations  

Developed as part of the **OpenFungi** initiative, this repository accompanies the peer-reviewed publication:

📄 **Anca Cighir, Roland Bolboacă, and Teri Lenard**  
*OpenFungi: A Machine Learning Dataset for Fungal Image Recognition Tasks*  
_Life_, **15**(7):1132, 2025  

🔗 [Read the article](https://www.mdpi.com/2075-1729/15/7/1132)

📁 **Dataset**: [Zenodo - OpenFungi Dataset](https://zenodo.org/records/15692070)

---

## 📚 Citation

If you use this code or dataset in your research, please cite our article:

```bibtex
@Article{life15071132,
  AUTHOR = {Cighir, Anca and Bolboacă, Roland and Lenard, Teri},
  TITLE = {OpenFungi: A Machine Learning Dataset for Fungal Image Recognition Tasks},
  JOURNAL = {Life},
  VOLUME = {15},
  YEAR = {2025},
  NUMBER = {7},
  ARTICLE-NUMBER = {1132},
  URL = {https://www.mdpi.com/2075-1729/15/7/1132},
  ISSN = {2075-1729},
  DOI = {10.3390/life15071132}
}
```

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

| Metric                | Description                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------|
| Sensitivity (TPR)     | Proportion of true positives correctly identified; also known as Recall.                        |
| Specificity (TNR)     | Proportion of true negatives correctly identified.                                              |
| Positive Predictive Value (PPV) | Proportion of positive predictions that are truly positive; corresponds to Precision.    |
| Negative Predictive Value (NPV) | Proportion of negative predictions that are truly negative.                                |
| F1 Score (F1)         | Harmonic mean of Sensitivity and PPV; balances precision and recall, useful with imbalanced data.|
| Accuracy (ACC)        | Overall proportion of correct classifications across all classes.                               |

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

**Roland Bolboaca, Lenard Teri and Anca Cighir**  
