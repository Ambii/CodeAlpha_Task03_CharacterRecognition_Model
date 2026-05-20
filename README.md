# CodeAlpha_Task03_CharacterRecognition_Model
Handwritten digit recognition using Convolutional Neural Networks (CNN) - 99.09% accuracy on MNIST dataset. Built with TensorFlow/Keras for CodeAlpha ML Internship.

# 🔢 Handwritten Digit Recognition using CNN

Deep Learning model for recognizing handwritten digits (0-9) using Convolutional Neural Networks as part of CodeAlpha Machine Learning Internship.

## 📊 Project Overview

This project implements a Convolutional Neural Network (CNN) to classify handwritten digits from the MNIST dataset. The model achieves 99.09% accuracy by learning hierarchical visual features through multiple convolutional layers.

## 🎯 Objective

Build a deep learning model that can accurately recognize handwritten digits, demonstrating understanding of:
- Convolutional Neural Networks (CNNs)
- Image preprocessing and augmentation
- Model training and optimization
- Performance evaluation and error analysis

## 📁 Dataset

- **Source:** MNIST (Modified National Institute of Standards and Technology)
- **Training Set:** 60,000 images
- **Test Set:** 10,000 images
- **Image Size:** 28×28 pixels (grayscale)
- **Classes:** 10 digits (0-9)

## 🏗️ Model Architecture

Conv2D (32 filters, 3×3) → ReLU → MaxPooling (2×2)
↓
Conv2D (64 filters, 3×3) → ReLU → MaxPooling (2×2)
↓
Conv2D (64 filters, 3×3) → ReLU
↓
Flatten → Dense (64) → Dropout (0.5) → Dense (10, softmax)

**Total Parameters:** ~1.2 million

## 🔧 Technologies Used

- **Python 3.x**
- **TensorFlow/Keras** - Deep learning framework
- **NumPy** - Numerical computing
- **Matplotlib/Seaborn** - Visualization
- **Google Colab** - GPU-accelerated training

## 📈 Results

| Metric | Score |
|--------|-------|
| Training Accuracy | 99.05% |
| Validation Accuracy | 99.10% |
| **Test Accuracy** | **99.09%** |
| Test Loss | 0.0275 |
| Misclassified | 91 / 10,000 |

### Per-Digit Performance:
All digits achieved 98-99% precision and recall, with digit 9 being slightly more challenging (98% recall).

## 🔍 Key Findings

1. **No Overfitting:** Train, validation, and test accuracies are nearly identical (99.05%, 99.10%, 99.09%)
2. **Consistent Performance:** All 10 digits achieve 98-99% accuracy
3. **Challenging Cases:** Misclassified images are often ambiguous even for humans
4. **Feature Learning:** First convolutional layer learned edge detectors (horizontal, vertical, diagonal)

## 📊 Visualizations

- Training/Validation accuracy and loss curves
- Confusion matrix showing digit confusions
- Misclassified examples analysis
- Learned convolutional filters

## 🚀 How to Run

```bash
# Clone repository
git clone https://github.com/YOUR_USERNAME/CodeAlpha_HandwrittenDigitRecognition.git

# Install dependencies
pip install tensorflow numpy matplotlib seaborn

# Run the notebook
jupyter notebook mnist_digit_recognition.ipynb

# Or open in Google Colab for GPU access
```

## 📂 Project Structure

CodeAlpha_HandwrittenDigitRecognition/
│
├── mnist_digit_recognition.ipynb    # Main notebook
├── mnist_cnn_model.h5               # Trained model
├── README.md                         # Documentation
├── requirements.txt                  # Dependencies
└── results/                          # Visualizations
├── confusion_matrix.png
├── training_history.png
├── misclassified_examples.png
└── learned_filters.png

## 💡 What I Learned

- **CNN Architecture:** Understanding convolutional layers, pooling, and feature hierarchies
- **Image Preprocessing:** Normalization, reshaping for neural networks
- **Model Evaluation:** Confusion matrices, precision/recall, error analysis
- **Overfitting Prevention:** Dropout, validation monitoring
- **Deep Learning Frameworks:** TensorFlow/Keras model building and training

## 🔮 Future Improvements

- Data augmentation (rotation, shift, zoom) for better generalization
- Try deeper architectures (ResNet, VGG)
- Extend to EMNIST (letters A-Z)
- Deploy as web application using Flask/Streamlit
- Real-time digit recognition from camera input

## 👨‍💻 Author

**[Your Name]**
- LinkedIn: [Your Profile]
- GitHub: [@YourUsername](https://github.com/YourUsername)

## 📜 License

Completed as part of CodeAlpha Machine Learning Internship Program.

## 🙏 Acknowledgments

- Dataset: MNIST Database (Yann LeCun et al.)
- Internship: CodeAlpha
- Framework: TensorFlow/Keras Team

---

⭐ If you found this helpful, please star this repo!
