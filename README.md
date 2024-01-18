# Multi-Class Weather Prediction

## Abstract

This project compares the performance of Simple CNN and ResNet-18 convolutional neural network architectures for multi-class weather classification in images. The study utilizes the Multi-class Weather Dataset, assessing model performance using precision, recall, and ROC-AUC metrics. The objective is to enhance meteorological image analysis and contribute to the improvement of weather prediction models, particularly in classifying diverse weather conditions.

## Introduction

### Background
Accurate weather prediction is essential for various sectors, influencing daily operations in transportation, agriculture, and hospitality. Traditional techniques often rely on numerical models and sensor data, but deep learning, specifically CNNs, offers a potential solution by analyzing visual signals in outdoor imagery.

### Problem Statement
This project aims to address the limitations of traditional weather forecasting techniques by developing a CNN model capable of accurately categorizing outdoor images into distinct weather patterns based on visual characteristics like cloud cover, sunshine intensity, and precipitation.

### Objectives
1. Image Classification: Train a CNN model on the Multi-class Weather Dataset to accurately classify images into predefined weather categories.
2. Model Assessment: Evaluate the trained model's performance using relevant metrics.
3. Real-Time Weather Forecasting: Use the CNN model for real-time weather prediction, allowing for automated and rapid forecasts based on visual input.

### Significance
By focusing on visual indicators and utilizing a well-monitored dataset, this project aims to offer a precise and useful method for weather forecasting, potentially transforming how weather prediction incorporates visual inputs.

## Impacts

- **Farming:** Accurate weather forecasts assist farmers in crop management, irrigation, and pest control.
- **Hospitality Services:** Reliable weather forecasts benefit tourism and outdoor event planning, enhancing the visitor experience.
- **Vehicle Usage:** Self-driving cars can improve road safety by adapting to weather conditions.

## Methodology

### Data Set Source
The [Multi-class Weather Dataset (MWD)](https://data.mendeley.com/datasets/4drtyfjtfy/1) serves as the primary dataset for image classification, containing outdoor photos labeled with four weather categories: 'cloudy,' 'shine,' 'rain,' and 'sunrise.'

### Data Processing
1. **Load Dataset:** Open MWD containing 1123 images.
2. **Arrange Information & Managing Null Values:** Divide the dataset into training and validation sets using data loaders, eliminating any null values.
3. **Retrieve File Names & Vector Format Conversion:** Transform images into a vector format for model input.

### Model Selection
- **Simple CNN:** Chosen for its success in image-related tasks, particularly in identifying spatial connections in weather patterns.
- **ResNet-18:** Selected for its advanced features, including residual learning and skip connections, addressing missing flux issues and improving training stability.

### Training Process
1. **Divided Feature Extraction Hierarchy:** Use three convolutional layers to gradually extract hierarchical features from input images.
2. **Reducing Space with MaxPooling:** Downsample feature maps to eliminate spatial redundancy.
3. **Completely Networked Layers for Categorization:** Two fully connected layers form the classifier for weather categories.

### Implementation
- **Code Structure:** Includes data preparation, model construction, training, assessment, and real-time prediction.
- **Data Loading:** Utilizes data loaders for both Simple CNN and ResNet-18.
- **Model Definition:** Defines architectures for both models, incorporating standard preprocessing operations.

### Problems and Solutions
- **Memorization Efficiency:** Addressed with batch loading, data generators, and code optimization.
- **Unbalanced Classes:** Mitigated through data augmentation techniques, especially for the 'rain' class.
- **Model Overfitting:** Reduced using regularization and dropout techniques.

## Results and Discussions

### Model Performance

- **CNN Model Outcome:** Achieves an 82% overall accuracy, demonstrating good balance between recall and accuracy across all classes.
- **ResNet18 Performance:** Impressive 96% overall accuracy on the test set, showcasing resilience across various classes.

#### Class-wise Comparison (ResNet18 vs. Simple CNN)

1. **Class 0 (Cloudy):** ResNet18 shows significant improvement in precision (63% to 94%) and achieves 100% recall, resulting in a F1-Score increase from 77% to 97%.

2. **Class 1 (Shine):** ResNet18 outperforms Simple CNN with increased precision (90% to 92%) and recall (68% to 96%), leading to a remarkable F1-Score increase from 78% to 94%.

3. **Class 2 (Rain):** ResNet18 outperforms Simple CNN with perfect precision (100%) for rainy weather prediction, achieving a 98% F1-Score.

4. **Class 3 (Sunrise):** ResNet18 consistently outperforms Simple CNN, with improved F1-Score (93% to 97%), precision (92% to 100%), and steady recall (94%).

## Ethical Concerns

The project addresses ethical concerns related to data privacy and bias by ensuring privacy protection, transparent data handling, and avoiding biases in data collection and model training.

## Conclusion

In conclusion, ResNet18 outperforms Simple CNN in multi-class weather prediction, demonstrating superior accuracy and recall across various weather conditions. The study acknowledges certain limitations and suggests future work to improve dataset biases, enhance model robustness, and integrate real-time data for more accurate weather forecasting. The project contributes to the advancement of weather prediction models by leveraging deep learning techniques and visual inputs.

## Acknowledgments
Special thanks to Maharshi Mehta for the contribution that helped in the development of this project.

If you have any questions or suggestions, please feel free to open an issue or contact mohammedbilalkhan10@gmail.com.

Happy analyzing and predicting!
