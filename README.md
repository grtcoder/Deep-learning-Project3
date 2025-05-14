# Deep-learning-Project3

This project explores adversarial robustness in deep learning by implementing and evaluating several attack methods on image classification models. It uses pretrained models on the ImageNet1K dataset and investigates the impact of different attacks including FGSM, PGD, and localized patch attacks.

---

## 📌 Overview

The project covers:

- **Baseline Evaluation**: Assess ResNet-34 performance on clean (unaltered) data.
- **FGSM Attack**: Generate adversarial examples using the Fast Gradient Sign Method.
- **PGD Attack**: Apply a stronger, iterative attack using Projected Gradient Descent.
- **Patch Attack**: Modify only a small localized image patch to fool the model.
- **Transferability Evaluation**: Evaluate whether adversarial examples created on ResNet-34 also fool DenseNet-121.

---

## 🧪 Results Summary

### 🔹 ResNet-34 Performance (Source Model):

| Attack Type | Top-1 Accuracy | Top-5 Accuracy | Accuracy Drop |
|-------------|----------------|----------------|----------------|
| Original    | 76.00%         | 94.20%         | —              |
| FGSM        | 6.00%          | 35.40%         | 92.1%          |
| PGD         | 0.00%          | 9.20%          | 100.0%         |
| Patch       | 4.80%          | 43.00%         | 93.7%          |

### 🔹 DenseNet-121 Performance (Transfer Evaluation):

| Attack Type | Top-1 Accuracy | Top-5 Accuracy |
|-------------|----------------|----------------|
| Original    | 74.80%         | 93.60%         |
| FGSM        | 63.40%         | 89.20%         |
| PGD         | 63.80%         | 90.20%         |
| Patch       | 68.80%         | 90.80%         |

---

### 📊 Extra results
We used some augmentations for better generalization with PGD and got the following results

#### 🔹 ResNet-34 Performance (Source Model)

| Attack Type | Top-1 Accuracy | Top-5 Accuracy | Accuracy Drop |
|-------------|----------------|----------------|----------------|
| PGD         | 0.20%          | 8.80%          | 99.7%          |
| Patch       | 26.20%         | 65.00%         | 65.5%          |

---

#### 🔹 DenseNet-121 Performance (Transfer Evaluation)

| Dataset            | Top-1 Accuracy | Top-5 Accuracy |
|--------------------|----------------|----------------|
| PGD Adversarial    | 52.00%         | 82.60%         |
| Patch Adversarial  | 64.20%         | 87.40%         |

---

#### ✅ Attack Effectiveness Summary

| Attack | Target Accuracy Drop | Achieved | Status |
|--------|-----------------------|----------|--------|
| FGSM   | > 50%                | 92.1%    | ✅     |
| PGD    | > 70%                | 99.7%    | ✅     |


## 📁 Project Structure

```
Deep-learning-Project3/
├── dl_project_3.ipynb       # Main notebook containing all tasks
├── requirements.txt         # Required Python packages
└── README.md                # Project documentation
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/grtcoder/Deep-learning-Project3.git
cd Deep-learning-Project3
```

### 2. Install Dependencies

Ensure Python 3.x is installed. Then run:

```bash
pip install -r requirements.txt
```

### 3. Run the Notebook

```bash
jupyter notebook dl_project_3.ipynb
```

---

## 📦 Requirements

- Python 3.x
- PyTorch
- torchvision
- numpy
- matplotlib
- tqdm

> 💡 Note: Ensure you have access to ImageNet1K or modify the data loader to use a smaller dataset (e.g., CIFAR-10) for testing purposes.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Contributions, suggestions, and improvements are welcome! Feel free to open issues or pull requests.

---
