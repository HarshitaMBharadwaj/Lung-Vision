# Lung-Vision

## Introduction
The project aimed to leverage deep learning models, specifically VGG19 and ResNet50, to improve the accuracy and efficiency of diagnosing lung diseases from chest X-rays. This was motivated by the challenges radiologists face in interpreting chest X-rays accurately amidst high variability and complexity.

## Data Acquisition and Preprocessing
The National Institutes of Health (NIH) chest X-ray dataset, consisting of 112,120 images, was utilized. Labels for thoracic pathologies were extracted from radiological reports using advanced natural language processing techniques. Data preprocessing involved aligning images with disease labels, cleaning, resizing, and normalization. Data augmentation techniques were employed to address class imbalance and enhance model generalization.

## Machine Learning Models
VGG19 and ResNet50, renowned for their deep learning capabilities, were employed. For VGG19, three models were developed, each with variations in architecture and training regimen. Similarly, four iterations of ResNet50 models were developed, with enhancements in training strategies. An ensemble method was also explored, combining outputs from VGG19 and ResNet50 models.

## Results and Analysis
The performance of individual models varied, with ResNet50 consistently outperforming VGG19. The best-performing model achieved a diagnostic accuracy of 73.42%. Ensemble models showed improved accuracy compared to individual VGG19 models but did not surpass the top-performing ResNet50 model. Results were summarized in a table, highlighting the test loss and accuracy of each model.

## Conclusion
The study demonstrated the potential of deep learning models, particularly ResNet50, in enhancing chest X-ray diagnosis. Despite notable achievements, current AI models serve as supplementary tools and cannot replace human expertise. Challenges remain in integrating AI into clinical workflows, including variability in model performance and the need for extensive data. Efforts to optimize model accuracy and streamline integration into clinical practice are essential for realizing the full potential of AI in medical diagnostics.
