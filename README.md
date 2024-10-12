# Image Segmentation for Self-Driving Cars Using HRNet

**Author:** Sumit Prabhakar  
**Date:** October 12, 2024

## Abstract
This report outlines the approach taken to develop an image segmentation model for self-driving cars navigating Indian roadways. The focus was on leveraging HRNet's architecture to create accurate masks for different road features, facilitating better decision-making for autonomous driving systems.

## Introduction
The problem of effectively segmenting images for self-driving cars is critical for ensuring safety and efficiency on the roads. The task involves identifying various objects and surfaces, such as roads, sidewalks, buildings, and vehicles. This segmentation allows the autonomous system to make informed decisions in real time. Understanding the Indian roadway landscape, which varies greatly in terms of infrastructure and traffic patterns, adds another layer of complexity to the problem.

## Approach Overview
The approach utilized HRNet for semantic segmentation, chosen for its capability to maintain high-resolution representations through parallel processing paths. This architecture was deemed suitable for handling the diverse visual challenges present in Indian roadways.

### Model Selection
**Model Used:** The project employed the HRNet model, known for its ability to maintain high-resolution representations.

### Inference Pipeline
The inference pipeline involves the following steps:
1. **Input Image:** Load the image for segmentation.
2. **Model Prediction:** Pass the image through the trained HRNet model to obtain segmentation masks.
3. **Mask Processing:** Convert the predicted mask into a binary format and extract contours for each segmented class.
4. **CSV Conversion:** Extract polygon coordinates and class labels from the masks and save them in a structured CSV file.

## Results
The segmentation results were evaluated using the Dice Coefficient metric, which measures the overlap between the predicted masks and the ground truth. The calculated class-wise Dice coefficients demonstrated the model's performance across different categories. The overall Dice coefficient achieved was **0.000000007235**, which can be significantly improved if the model is fine-tuned.

## Conclusion, Discussions, and Future Scopes
In conclusion, the approach of utilizing HRNet for image segmentation in self-driving cars has shown potential despite the challenges faced in achieving high accuracy, as reflected in the Dice coefficient. The primary advantages of this approach include its capability to maintain high-resolution details and adapt to various scales of features. However, the low Dice coefficient highlights the need for further improvement.
