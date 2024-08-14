# deep-learning-challenge

### **Report on the Performance of the Deep Learning Model for Alphabet Soup**

#### Overview of the Analysis: 

The purpose of this analysis was to use machine learning and neural networks, and the features in the provided dataset, to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup charity. The goal was to achieve a predictive accuracy of over 75%, leveraging deep learning techniques to handle the complexities and subtleties in the data.

----------

#### Data Preprocessing: 

-   **Target Variable:** 
    -   The target variable for the model was `IS_SUCCESSFUL`, which indicates whether a charity donation was successful.
-   **Feature Variables:**
    -   The feature variables for the model included all columns related to the characteristics of each application, such as `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`.
-   **Variables Removed:**
    -   Columns like `EIN` and `NAME` were removed from the input data because they are identifiers and do not directly contribute to predicting the success of a donation.


#### Compiling, Training, and Evaluating the Model:  

-   **Model Architecture:** 
    
    -   **Neurons:**
        -   The initial model was designed with a total of 111 neurons across 2 hidden layers.
        -   First layer: 80 neurons
        -   Second layer: 30 neurons
        -   Output layer: 1 neuron
    -   **Layers:**
        -   The model consists of two hidden layers with ReLU activation functions. 
        -   The output layer uses a Sigmoid activation function to handle the binary classification problem.
    -   **Activation Functions:**
        -   **ReLU (Rectified Linear Unit):** Chosen for the hidden layers due to its effectiveness in handling non-linearities and its wide usage in deep learning models.
        -   **Sigmoid:** Used in the output layer to output probabilities for the binary classification task.
        
-   **Initial Model Performance:**
    -   After training the model, the initial accuracy achieved was 72.6%, which did not meet the target accuracy of 75%.
    
-   **Optimisation Steps Taken:**
   Some steps were taken to try and improve the accuracy.
    -   **Increased Neurons:** The number of neurons in the first and subsequent layers was increased to 200 and 100, respectively, to capture more complex patterns in the data.
    -   **Increased Layers:** An Additional hidden layer was introduced to deepen the model, allowing it to learn more intricate patterns in the data.
    -   **Epoch Adjustment:** Also, the model was trained for 200 epochs to ensure sufficient learning while monitoring for overfitting.

----------

#### **Summary:**

The deep learning model created for Alphabet Soup demonstrated the ability to predict the success of charitable donations, achieving a final accuracy of 72.4%. The model architecture, consisting of three hidden layers and a dropout layer, was chosen to try and balance model complexity and overfitting. Unfortunately, the accuracy did not improve.

**Recommendation:** While the deep learning model performed reasonably well, it did not achieve the target accuracy. A different model, such as a Random Forest or Gradient Boosting Machine (GBM), could be considered for this classification problem. These models are often more interpretable and can handle categorical data more efficiently without requiring extensive preprocessing. 
By exploring these alternative models, the Alphabet Soup charity could achieve higher accuracy and better understand the key factors driving the success of their donation campaigns.

