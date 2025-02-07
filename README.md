# Lung-Vision

## Introduction
Medical imaging plays a crucial role in modern healthcare by enabling early detection, diagnosis, and treatment of a variety of diseases, including lung diseases. Chest X-rays, in particular, are essential for diagnosing respiratory conditions like pneumonia, tuberculosis, and lung cancer. Despite their widespread use, challenges persist in the accurate and timely interpretation of these images. One major issue is the limited availability of high-quality, annotated medical imaging datasets. Datasets like the NIH Chest X-ray dataset are often large but imbalanced, with some conditions having significantly fewer annotated images. This imbalance can lead to deep learning models overfitting on the more common diseases, causing poor generalization to rare conditions, which might result in diagnostic errors such as missed abnormalities or false positives. This limitation highlights the need for more effective augmentation techniques to enhance dataset diversity and improve model robustness.

## Objective
The primary goal of this project is to assess the effectiveness of deep learning models (VGG19 and ResNet50) in enhancing diagnostic precision and efficiency for identifying lung diseases from chest X-ray images. This includes leveraging AI and image recognition technologies to improve both diagnostic accuracy and workflow efficiency.

## Research Questions
1. Diagnostic Accuracy: What level of diagnostic accuracy can VGG19 and ResNet50 achieve when applied to the NIH Chest X-ray dataset?
2. Efficiency: How do these models impact diagnostic processes in terms of time and resource utilization when compared to traditional diagnostic methods?
3. Challenges in Clinical Integration: What challenges are encountered when integrating these models into clinical settings, and how can they be addressed?

## Data Acquisition and Preprocessing
- Dataset: The study uses the NIH Chest X-ray dataset, which includes over 112,000 frontal-view X-ray images from 30,805 patients, covering 14 thoracic pathologies like Atelectasis, Consolidation, and Pneumothorax.
- Preprocessing: The data was cleaned by aligning images with disease labels, removing irrelevant or corrupted images, resizing to 224x224 pixels, and normalizing pixel values.

# Data Augmentation
To address the class imbalance in the dataset, a robust data augmentation pipeline was implemented. This included:

- Horizontal flipping, brightness/contrast adjustments, rotations, scaling, and adding Gaussian noise.
- Synthetic samples were generated for underrepresented classes to balance the dataset.

# Exploratory Data Analysis (EDA)
The EDA revealed that 'Infiltration' was the most common pathology, with a higher occurrence rate among males for most pathologies.

## Model Architecture
1. VGG19: A deep convolutional network with 19 layers, leveraging small filters and ReLU activation for complex feature extraction. It uses max pooling to reduce dimensions and ends with fully connected layers for classification.
2. ResNet50: Known for its deeper architecture with residual connections that help in handling vanishing gradients during training.

## Results
- VGG19: The model showed variability in performance, with accuracies ranging from 47.46% to 59.71%. The lowest test loss was 1.597.
- ResNet50: Demonstrated superior performance with accuracies up to 73.42% and a test loss as low as 0.9009.
- Ensemble Models: Using averaging and hard voting techniques, the ensemble models achieved accuracies of 66.19% and 62.50%, respectively. These results suggest that while the ensemble method enhances robustness, it did not outperform the best ResNet50 model.

## Conclusion
Diagnostic Accuracy: ResNet50 outperformed VGG19 in accuracy and loss metrics, indicating that deeper architectures like ResNet50 may be more effective for complex tasks like chest X-ray analysis.
Efficiency: AI models, while promising, still require significant integration effort and validation in real-world clinical settings. They assist in diagnosis but are not yet fully capable of replacing human radiologists.
Clinical Integration: The adoption of AI models in clinical practice faces challenges related to model performance variability, extensive data requirements, and integration into existing workflows.

## Future Work
- The study hints at the use of Generative Adversarial Networks (GANs) for augmenting datasets and improving model performance. GAN-generated synthetic images may offer higher fidelity and diversity in the dataset compared to traditional augmentation methods like rotation and flipping.
- The research explores whether GAN-augmented datasets lead to improved diagnostic model performance, robustness, and generalizability.

## Research Methodology
Sampling: The study uses random sampling to create two groups: one augmented using GAN-generated synthetic images and the other using traditional augmentation techniques.
Pilot Validation: The pilot phase validated the accuracy and Fréchet Inception Distance (FID) scores, showing the potential of GAN-generated images to enhance model performance.

## Key Constructs
1. Augmentation Methods: Comparing traditional and GAN-based augmentations.
2. Model Performance: Measured by accuracy, reflecting the diagnostic capabilities of the model.
3. Image Fidelity: Assessed using FID scores to evaluate the realism of synthetic images.

This study provides valuable insights into how advanced deep learning techniques, including GAN augmentation, can improve the diagnostic accuracy and efficiency of medical imaging systems in real-world healthcare settings.
