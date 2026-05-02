# Mathematical-Symbol-Classifier

**🚀 Project Overview**

This project focuses on building a Convolutional Neural Network (CNN) to classify handwritten mathematical symbols such as digits, operators, and Greek symbols. The model is trained on a large dataset and achieves ~95% accuracy, demonstrating strong performance in multi-class image classification.

**🎯 Objective**

Classify handwritten mathematical symbols into their correct classes  
Build an efficient deep learning model using CNN  
Evaluate performance using multiple metrics  
Provide real-time prediction capability    

**📊 Dataset**

Source: Kaggle Handwritten Math Symbols Dataset  
Total Images: ~375,000  
Training Images: ~300,000  
Validation Images: ~75,000  
Number of Classes: 82  
Example Classes:  
- Digits: 0–9  
- Operators: +, -, ×, /, =  
- Symbols: α, β, π, Σ, ∫, etc.  

**⚙️ Data Preprocessing**

Converted images to grayscale  
Resized images to 64×64  
Normalized pixel values (0–1)  
Used ImageDataGenerator for efficient data loading  

**🧠 Model Architecture**

The model is a Custom CNN designed for symbol recognition.

**Architecture:**

Conv2D (32 filters) + BatchNorm + MaxPooling  
Conv2D (64 filters) + BatchNorm + MaxPooling  
Conv2D (128 filters) + BatchNorm + MaxPooling    
Conv2D (256 filters) + BatchNorm + MaxPooling  
Flatten Layer  
Dense Layer (256 neurons)  
Dropout (0.5)  
Output Layer (Softmax – 82 classes)  

**🔍 Why CNN instead of EfficientNet?**

Initially, transfer learning (EfficientNet) was used, but:  
- Handwritten symbols are simple patterns
- CNN performed better and faster
- Reduced computational cost  

👉 Hence, a custom CNN was chosen.

**🏋️ Training Details**

Batch Size: 64  
Epochs: 10  
Optimizer: Adam  
Loss Function: Categorical Crossentropy  
Callbacks Used:  
EarlyStopping  
ReduceLROnPlateau  

**📈 Results**

Accuracy: 95.06%
Precision: 94.51%
Recall: 95.06%
F1 Score: 94.61%

**🔮 Prediction System**

The model can:
- Take a new handwritten image
- Preprocess it
- Predict the correct mathematical symbol

**💻 Tech Stack**
- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
