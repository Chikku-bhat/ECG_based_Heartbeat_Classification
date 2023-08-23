# ECG_based_Heartbeat_Classification

This project demonstrates the creation of a Convolutional Neural Network (CNN) model to classify heartbeat sounds into different categories. The dataset consists of audio recordings of heartbeat sounds, and the goal is to build a model that can accurately classify these sounds for medical diagnosis purposes.

## Project Overview

The project is structured as follows:

1. **Data Preparation:**
   - Audio files are loaded using the `librosa` library.
   - The dataset is organized into a structured DataFrame.
   - Short audio clips and certain labels are filtered out.
   - The dataset is shuffled and split into training and testing sets.

2. **Feature Extraction:**
   - Mel-frequency cepstral coefficients (MFCCs) are extracted using `librosa`.
   - The `extract_features` function generates MFCCs from audio files.

3. **Data Preprocessing:**
   - Feature matrices are reshaped for CNN input.
   - Labels are encoded using `LabelEncoder` and converted to categorical using `to_categorical`.
   - Class weights are computed to handle class imbalance.

4. **CNN Model Architecture:**
   - A CNN model is designed using the Keras `Sequential` API.
   - Convolutional layers with activation functions and max-pooling are added.
   - Dropout layers are used to prevent overfitting.
   - A global average pooling layer aggregates spatial information.
   - The model concludes with a dense softmax layer for classification.

5. **Model Compilation and Training:**
   - The model is compiled with appropriate loss, optimizer, and metrics.
   - Class weights are used during training to address class imbalance.
   - Callbacks like `EarlyStopping` and `ModelCheckpoint` are employed.

6. **Training Progress Visualization:**
   - Training and validation loss curves are plotted using `matplotlib`.
   - Training and validation accuracy curves are visualized.

7. **Model Evaluation:**
   - The trained model is saved in the HDF5 format.
   - Model performance is evaluated on the test set using the `evaluate` method.
   - A classification report is generated with metrics such as precision, recall, and F1-score.

8. **Result Visualization:**
   - A normalized confusion matrix is plotted to visualize classification performance.

## Usage

1. Clone the repository: `git clone https://github.com/yourusername/heartbeat-classification.git`
2. Navigate to the project directory: `cd heartbeat-classification`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Run the Jupyter Notebook to explore and execute the project.

## Conclusion

This project showcases proficiency in working with audio data, feature extraction techniques, CNN architecture design, and deep learning training procedures. It can serve as a learning resource for those interested in audio classification tasks and CNN-based models.

Feel free to explore the notebook for a detailed walkthrough of each step in the project!
