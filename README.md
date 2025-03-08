# 🧠 AI - FashionMNIST Feedforward Neural Network

## 📌 Overview
This repository contains an implementation of a **Feedforward Neural Network (FNN)** trained on the **FashionMNIST** dataset. The project explores the impact of different **activation functions** and **optimizers** on model performance and further improves training using **learning rate scheduling and additional epochs**.

## 🚀 Features
- **Custom Feedforward Neural Network** with 3 hidden layers.
- **Experimentation** with:
  - Three **activation functions**: ReLU, Sigmoid, and Tanh.
  - Two **optimizers**: SGD and Adam.
- **Performance Improvement** using:
  - **Learning rate scheduling (StepLR)**
  - **Extended training epochs**

## 📂 Files and Structure
- `main.ipynb` - Jupyter Notebook containing code, training, and experiments.
- `Results Report.docx` - A concise report analyzing the findings and results.
- `README.md` - This documentation file.
- `requirements.txt` - Python dependencies required for running the code.

## 🔧 Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/FashionMNIST-FNN.git
cd FashionMNIST-FNN
```

### 2️⃣ Set Up Virtual Environment
```bash
# Windows (Run PowerShell as Administrator)
Set-ExecutionPolicy Unrestricted -Scope Process    

# Create Virtual Environment
python -m venv venv         
venv\Scripts\activate        # Windows
# OR
source venv/bin/activate     # MacOS/Linux

# Install dependencies
pip install -r requirements.txt
```

### 3️⃣ GPU Setup (Optional)
If CUDA is not detected but a GPU is available:
```bash
pip uninstall torch torchvision torchaudio
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```

## 📊 Experiment Results

### **(b) Activation Function & Optimizer Comparison**
| Activation | Optimizer | Test Accuracy (%) | Rank |
|------------|------------|------------------|------|
| **ReLU**   | **SGD**    | 79.26            | 5    |
| **ReLU**   | **Adam**   | **87.08** 🏆     | 1    |
| **Sigmoid**| **SGD**    | 10.00 ❌         | 6    |
| **Sigmoid**| **Adam**   | 86.27            | 3    |
| **Tanh**   | **SGD**    | 81.83            | 4    |
| **Tanh**   | **Adam**   | 87.06            | 2    |

🔹 **Best Model:** **ReLU + Adam (87.08%)**  
🔹 **Worst Model:** **Sigmoid + SGD (10.00%)** (Vanishing gradient problem)  

### **(c) Improving the Best Model**
| Activation | Optimizer | Test Accuracy (%) | Epochs |
|------------|------------|------------------|--------|
| **ReLU**   | **SGD**    | 88.15            | 5      |
| **ReLU**   | **SGD**    | **89.53** 🚀     | 15     |

🔹 **By increasing epochs and applying learning rate scheduling, we improved accuracy from 87.08% → 89.53%** 🎯  

## 📜 Key Learnings
✅ **ReLU performs best**, avoiding vanishing gradient issues.  
✅ **Adam optimizer is more effective** than SGD for this dataset.  
✅ **Training longer (more epochs) and using a Learning Rate Scheduler significantly improves accuracy.**  

## 📌 Usage
To run the experiments and train the model:
```bash
jupyter notebook main.ipynb
```

## 👨‍💻 Author
**Ong Jung Yi**
📧 Contact: [ong.jung.yi.1503@gmail.com]
