# Brain-Tumor-Detection-using-Deep-Learning

### Overview
This project presents an in-silico approach for the detection and segmentation of brain tumors using Deep Learning and Image Processing techniques. By leveraging MRI scans, the system classifies whether a patient has a tumor and, if detected, accurately localizes the tumor at a pixel level. The implementation significantly aids in early diagnosis and cost-effective cancer detection, potentially saving lives.

### How It Works
- MRI images are preprocessed and enhanced using CLAHE (Contrast Limited Adaptive Histogram Equalization) to improve contrast and reduce noise.
- A Deep Learning classifier (ResNet-50) determines whether a tumor is present.
- If a tumor is detected, a segmentation model (ResUNet) predicts and highlights the tumor's exact location.
- The final output consists of the original MRI scan, the actual mask, and the predicted segmentation mask, providing a clear visualization of the tumor region.
  
### Technologies Used
- Python (Programming Language)
- TensorFlow, Keras (Deep Learning Frameworks)
- OpenCV (Image Processing)
- Matplotlib, Seaborn (Data Visualization)
- Pandas, NumPy (Data Analysis)
- ResNet-50 (Classification Model)
- ResUNet (Segmentation Model)
  
### Key Features
✔️ Enhanced MRI scan preprocessing using CLAHE
✔️ Tumor detection using ResNet-50 classification
✔️ Tumor segmentation using ResUNet
✔️ Improved accuracy with Deep Learning techniques
✔️ Cost-effective and efficient early tumor detection

### Steps to Implement
1. Data Preprocessing
- Import required packages and libraries:
  - Data Handling: zipfile, cv2, files
  - Visualization: pandas, numpy, seaborn, matplotlib
  - Model Training: TensorFlow, Keras, Sequential
- Mount and load the dataset.
- Analyze the dataset by checking missing values, column types, and overall structure.
- Visualize the MRI scans and their corresponding tumor masks.
- Drop irrelevant columns (e.g., patient ID) to optimize training.
- Convert categorical data (mask labels) to string format.
- Split the dataset into 75% training and 25% testing for model evaluation.
  
2. Image Enhancement
To improve image quality, CLAHE is applied:
- Divides images into smaller tiles.
- Performs histogram equalization on each tile.
- Maps pixel intensities using cumulative distribution functions.
- Stitches the enhanced tiles back together to form the final output.
  
3. Image Classification
- Model Used: ResNet-50 (a 50-layer deep CNN)
- Purpose: Determines whether a tumor is present in an MRI scan.
  
4. Image Segmentation
- Model Used: ResUNet (a combination of ResNet and U-Net)
- Purpose: If a tumor is detected, the model predicts the tumor’s exact location at a pixel level.
  
Output:
- Original MRI scan
- Ground truth mask (actual tumor location)
- Predicted mask (model's tumor prediction)
- Overlayed MRI with predicted mask
  ![image](https://github.com/user-attachments/assets/0436f34d-2f0c-47c6-92da-d40d09475f1c)
Fig: Input MRI scan and its corresponding mask, the MRI image with the actual mask, the mask predicted by the ResUNet model and the MRI image with the predicted mask.

### Applications
🏥 Early-stage tumor detection in medical diagnostics
🧠 Improved accuracy in brain tumor classification
💰 Cost-effective alternative to traditional cancer diagnosis
⚕️ Supports automated medical imaging analysis



# Dataset :
 https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation

# Architecture Diagram for ResNet50
![image](https://github.com/user-attachments/assets/e3aef69a-568a-48ad-b892-408bb7b6a7ba)

