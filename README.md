# Lec-1


#### **Computer Vision Overview**
- Purpose:
  - Understand images, animations, videos, and emotions.
  - Extract useful information from single or multiple images.

#### **Machine/Deep Learning Model Workflow**
1. **Import Libraries**
   - Use libraries to build models.
2. **Import Dataset**
   - Examples: CT scans, ultrasound, satellite images.
3. **Data Preparation**
   - Split into training and testing datasets.
4. **Data Processing**
   - Apply processing techniques like filters.
5. **Build Model**
   - Design and structure the model.
6. **Compile Model**
   - Prepare the model for execution.
7. **Project Results**
   - Output the results of the model.

#### **Data Imputation vs. Data Augmentation**
- **Data Imputation**
  - Handles missing data by filling pixel gaps.
  - Example: Predicting missing pixel values based on surrounding data.
- **Data Augmentation**
  - Expands datasets by transforming existing data.
  - Example: Flipping images, changing brightness, or adding noise.

---


#### **Examples of Image Processing in Real Life**
- Brightness adjustments.
- Noise removal.
- Filtering.
- Histogram equalization.
- Color normalization.

#### **Processes in Computer Vision**
1. **Segmentation**
   - Divides images into meaningful parts at the pixel level.
2. **Detection**
   - Locates objects within an image or video.
3. **Recognition**
   - Identifies and classifies detected objects into predefined categories.
   - Note: Detection precedes recognition.
4. **Classification**
   - Binary Classification: Classifies into two groups (e.g., cat vs. dog).
   - Multi-class Classification: Classifies into more than two categories.
------
-----
# lec-2

### Page 1 Explanation: Image Classification

#### **Image Classification Overview**
- **Classification**:
  - Targets/labels are predefined. This is a supervised learning method.
  - Example: Categorizing objects as "Black" or "Red."
- **Clustering**:
  - Targets/labels are unknown. This is an unsupervised learning method.

#### **Types of Classification**
1. **Binary Classification**:
   - Divides data into two classes (e.g., "Cat" vs. "Dog").
2. **Multi-class Classification**:
   - Divides data into more than two classes (e.g., "Shoes," "Clothes," "Accessories").
3. **Hierarchical Classification**:
   - Organizes data hierarchically (e.g., Gender: Male/Female; Hair: Short/Long).

#### **Models for Image Classification**
- KNN (K-Nearest Neighbors)
- ANN (Artificial Neural Network)
- CNN (Convolutional Neural Network)
- SVM (Support Vector Machine)

---

### Page 2 Explanation: Classification Model Workflow

#### **Steps to Build a Classification Model**
1. **Import Libraries**:
   - Load the necessary tools for the model.
2. **Load Dataset**:
   - Prepare the data for analysis.
3. **Preprocessing**:
   - Apply filters, resizing, or histogram equalization to clean and normalize the data.
4. **Divide Data**:
   - Split data into training, testing, and validation sets.
5. **Build Classification Model**:
   - Use models like SVM, ANN, or KNN.
6. **Fit Model**:
   - Train the model on the training dataset.
7. **Compile/Run Model**:
   - Test the model and optimize it.
8. **Calculate Accuracy**:
   - Measure the model's performance.
9. **Predict Results**:
   - Use the trained model to classify new data.

### Page 3 Explanation: K-Nearest Neighbors (KNN)

#### **KNN Overview**
- **Purpose**:
  - Classify a data point based on its neighbors.
- **Key Parameter**:
  - `k`: The number of nearest neighbors considered (e.g., k = 3).

#### **Example**
- Data points:
  - Each point is represented by its (x, y) coordinates.
  - Examples: A(1,6), B(6,3), C(4,5), D(6,7), E(8,3), F(6,10).
- Unknown point:
  - G(5,5): The goal is to classify it using KNN with k = 3.

#### **Steps**
1. **Calculate Distance**:
   - Use the Slide Line Distance (SLD) formula:  
     \( \text{SLD}(P1, P2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} \)
   - Compute distances between G and all points.
   - Example:
     - \( \text{SLD}(G, A) = \sqrt{(5-1)^2 + (5-6)^2} = \sqrt{17} \)
2. **Find the Nearest Neighbors**:
   - Sort points by distance.
   - Select the 3 nearest neighbors (k = 3).
3. **Classify G**:
   - Based on the majority class of the nearest neighbors, G is assigned a class.

---

### Page 4 Explanation: Test Image Classification with KNN

#### **Problem**
- Classify an unknown image using KNN (k = 3).
- The dataset includes images of dogs and cats.

#### **Steps**
1. **Feature Representation**:
   - Each image is represented by pixel intensity values.
   - Examples:
     - Dog: [10, 20, 94, 17, ...]
     - Cat: [34, 101, 179, 88, ...].

2. **Calculate Distance**:
   - Use the distance formula:  
     \( \text{Distance}(I_1, I_2) = \sum |I_{1p} - I_{2p}| \),  
     where \( I_{1p} \) and \( I_{2p} \) are pixel intensities.

3. **Determine Nearest Neighbors**:
   - Find the 3 closest images (k = 3) by calculating distances.

4. **Assign Class**:
   - Based on the majority class of the nearest neighbors, the test image is classified.
   - Example:
     - If the nearest neighbors are 2 dogs and 1 cat, the test image is classified as a dog.

