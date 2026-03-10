# Image-Classification-vgg16
This project demonstrates transfer learning by adapting VGG16 — a deep CNN pre-trained on ImageNet — to a custom classification task. Rather than training from scratch, the convolutional base is frozen and a new classification head is trained on top, allowing high accuracy even with limited data. Data augmentation is used to improve generalization.

Model Architecture

VGG16 (frozen, ImageNet weights)
  
  └── Flatten
  
  └── Dense(256, relu)
  
  └── Dropout(0.5)
  
  └── Dense(N_CLASSES, softmax)

How to Run
bashgit clone https://github.com/Khalfani04/image-classification-vgg16
cd image-classification-vgg16
pip install tensorflow matplotlib
jupyter notebook Assignment_3_Cosc_31000.ipynb

Dataset should be organized in train/, val/, and test/ subdirectories by class.

Training Details
Setting               Value
Optimizer             Adam (lr=1e-4)
Loss                  Categorical Crossentropy
Epochs                50
Augmentation          Rotation, flip, zoom, shift
Base Model            VGG16 (frozen)

What I Learned:
How transfer learning dramatically reduces training time and data requirements
How data augmentation prevents overfitting on small datasets
How to interpret training vs. validation accuracy/loss curves to diagnose model behaviour
