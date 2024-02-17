# Pokemon Image Classifier using ResNet50 Transfer Learning

## Theory of Transfer Learning

### **What is it?**

Transfer learning leverages knowledge from a pre-trained model on a large dataset for a new task with a smaller dataset. This improves efficiency and avoids overfitting.

### **Why use it?**

Training complex models from scratch with limited data often leads to overfitting. Transfer learning utilizes pre-trained models to extract valuable features, improving performance on new tasks.

### **How does it work?**

Pre-trained models typically have two parts:

* **Feature extractor:** Extracts features from images using convolutional and pooling layers.
* **Classifier:** Classifies the extracted features using dense layers and an activation function.

We can use transfer learning in three ways:

**1. As pre-trained models:** Directly use the model for prediction (similar tasks, large datasets).
**2. Fixed feature extractor:** Freeze the feature extractor and train only the classifier (smaller, similar datasets).
**3. Fine-tuning:** Fine-tune both the feature extractor and classifier (large, dissimilar datasets).

### **Choosing the right approach:**

The appropriate strategy depends on the size and similarity of your new dataset to the original one:

* **Large & Similar:** Fine-tuning often works well.
* **Large & Dissimilar:** Consider training from scratch.
* **Small & Similar:** Use the feature extractor and train a new classifier.
* **Small & Dissimilar:** Fine-tune a small number of layers in the feature extractor.

## Project (Pokemon Image Classifier using Transfer Learning)

This project demonstrates image classification using transfer learning with the ResNet50 model to identify different Pokemon characters.

### Project Structure

The project is divided into three parts:

### **Part 1: Data Preparation**

* **Creating the dataset:** Download and prepare the Pokemon image dataset.
* **Shuffling the dataset:** Randomize the order of data points to avoid bias.
* **Final preprocessing:** Resize and normalize images for compatibility with the model.

### **Part 2: ResNet50 Model**

* **Importing libraries:** Import necessary libraries for working with the model.
* **Loading the model:** Load the pre-trained ResNet50 model.
* **Building our classifier:** Add a new classifier on top of the pre-trained model.
* **Performing feature extractor strategy:** Freeze the convolutional base and train only the classifier.

### **Part 3: Fine-tuning**

* **Making predictions:** Use the trained model to predict labels for new images.
* **Compiling the new model:** Set up the loss function, optimizer, and metrics for training.
* **Fine-tuning the new model:** Unfreeze a few layers in the convolutional base for fine-tuning.
* **Training the model:** Train the model on the prepared dataset.


