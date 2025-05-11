
```markdown
# 🧠 Fashion MNIST Image Classification (CNN with Hyperparameter Tuning)

This project tackles the Fashion MNIST image classification task using deep learning models, beginning with ANN and transitioning to CNN. Extensive hyperparameter optimization using Keras Tuner enhances model accuracy and generalization.

---

## 📦 Dataset Overview

- **Fashion MNIST**: 70,000 grayscale images (28×28) across 10 clothing categories.
- **Labels**: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot
- **Split**: 60,000 training + 10,000 test samples

---

## ⚙️ Project Workflow

1. **Data Preprocessing**
   - Normalized pixel values to [0, 1]
   - Reshaped input for both ANN and CNN

2. **Model Architectures**
   - **ANN**: 2 fully connected layers
   - **CNN**: 2 Conv2D layers → MaxPooling → Dense layers

3. **Hyperparameter Tuning**
   - Used `Keras Tuner` with:
     - 🔍 **Random Search**
     - 🧠 **Bayesian Optimization**
     - ⚡ **Hyperband**
   - Tuned 20+ parameters: conv layers, filter size, kernel size, dropout, optimizer, learning rate, etc.

4. **Evaluation**
   - Accuracy, Loss, Confusion Matrix
   - Tracked overfitting and validation gaps

---

## 📈 Training Performance

### 📉 Loss & Accuracy Curves

<p align="center">
  <img src="[https://raw.githubusercontent.com/yourusername/yourrepo/main/a7680b9f-56c6-4c6f-bfa7-70fcaa7856e5.png](https://github.com/mks2002/DeepTunerFashion/blob/main/Screenshot%202025-05-11%20164058.png)" width="400" title="Loss & Accuracy Curves"/>
  <img src="[https://raw.githubusercontent.com/yourusername/yourrepo/main/e0c4d915-ca5b-4c15-b4e7-3c39b1347ffb.png](https://github.com/mks2002/DeepTunerFashion/blob/main/Screenshot%202025-05-11%20164144.png)" width="400" title="Confusion Matrix"/>
</p>

 

---

## ✅ Final Results (Best CNN)

| Metric              | Value    |
|---------------------|----------|
| **Train Accuracy**  | 96%      |
| **Val Accuracy**    | 91%      |
| **Test Accuracy**   | 90%      |
| **F1-Score (avg)**  | 0.90     |
| **Parameters Tuned**| 20+      |
| **Tuning Trials**   | 60+      |

---

## 🧠 Observations

- CNN outperformed ANN by **+6%** accuracy.
- Best test accuracy of **93%** was achieved using **Bayesian Optimization**.
- Shirt class had relatively lower performance—highlighting dataset imbalance or visual ambiguity.

---

## 🛠 Tech Stack

- **Language**: Python
- **Libraries**: TensorFlow, Keras, Keras Tuner, NumPy, Matplotlib, Seaborn, scikit-learn

---

## 🗂 Directory Structure

```

📁 Fashion-MNIST-CNN-Tuning
├── mnist\_fashion\_classification.ipynb
├── README.md

```

---

## 🚀 How to Run

1. Clone this repo  
   `git clone https://github.com/yourusername/yourrepo.git`

2. Install dependencies  
   `pip install -r requirements.txt`

3. Run notebook  
   `jupyter notebook mnist_fashion_classification.ipynb`

---

## 📌 Key Takeaways

- Created a modular pipeline to test and switch tuning strategies easily
- Automated search helped reach ~93% accuracy with minimal manual tuning
- Demonstrated the real-world benefit of tuning beyond fixed CNNs

---

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.
```


