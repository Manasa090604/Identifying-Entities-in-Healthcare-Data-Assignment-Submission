## Project Title: Identifying Entities in Healthcare Data Assignment Submission
## Goal of the Project
The goal of this project is to develop a Named Entity Recognition (NER) model specifically designed to identify medical entities such as diseases and treatments from text. This model can be used to automate the extraction of medical information, which is crucial for research, clinical documentation, and other applications in the healthcare sector.

### Objectives
#### Data Preparation:

Collect and preprocess medical text data.
Label the data with relevant entities (diseases and treatments).
#### Model Development:

Implement a Conditional Random Field (CRF) model to identify named entities in the text.
Extract features necessary for the CRF model using libraries like spaCy.
#### Evaluation:

Assess the performance of the CRF model using metrics such as F1 Score and classification reports.
Visualize the predictions to understand model performance better.
#### Visualization:

Create visual representations of the predictions to facilitate analysis.
## Dataset
Training Data: train_sent.txt and train_label.txt
Testing Data: test_sent.txt and test_label.txt
## Implementation Details
1. Data Preparation
Feature Extraction:
Extract features like Part-of-Speech (PoS) tags and preceding words using spaCy.
2. Model Development
Model: Conditional Random Field (CRF)
3. Evaluation
4. Visualization
## Libraries Used:
sklearn_crfsuite for CRF implementation

seqeval for evaluation metrics
## Metrics Used:
F1 Score

Classification Report

## Plotting Libraries:
matplotlib for creating visual plots of model predictions.
## Install Dependencies:

pip install sklearn_crfsuite seqeval matplotlib spacy
## Download and Prepare Data:

Ensure the dataset files are in the correct directory paths.

### Example sentence containing the disease 'hereditary retinoblastoma'
example_sentence = ["The", "patient", "was", "diagnosed", "with", "hereditary", "retinoblastoma", "and", "was", "prescribed", "chemotherapy", "and", "radiation", "therapy"]

###  Process the sentence to extract features
example_features = extract_features(example_sentence)

###  Predict the labels using the CRF model
example_prediction = crf_model.predict_single(example_features)

###  Combine the sentence with the predicted labels for easier analysis
predicted_labels = list(zip(example_sentence, example_prediction))



## Conclusion
In this project, we developed a Named Entity Recognition (NER) model to extract medical entities from text, specifically targeting diseases and treatments. The key steps included data preparation, model development, evaluation, and visualization. Here’s a summary of the findings:

### Data Preparation:

We successfully preprocessed the dataset by extracting relevant features such as Part-of-Speech (PoS) tags and preceding words. This ensured that the model had the necessary input to learn effectively.
Model Development:

The Conditional Random Field (CRF) model was implemented to recognize medical entities. This model is well-suited for sequence labeling tasks, making it a good choice for NER applications.
Evaluation:

The model’s performance was assessed using metrics such as the F1 Score and classification report. These metrics provided insights into the model’s accuracy and ability to correctly identify and classify medical entities.
Visualization:

Predictions were visualized to better understand the model’s output. The visual representation helped in analyzing how well the model identified diseases and treatments within the text.
Predictions and Results
F1 Score: The F1 Score achieved by the model reflects its balance between precision and recall. It indicates how well the model performs in identifying entities accurately while minimizing false positives and false negatives.

Classification Report: The detailed classification report provided information on the precision, recall, and F1 Score for each entity class (e.g., B-Disease, I-Disease, B-Treatment, I-Treatment). This report is crucial for understanding the model’s strengths and areas for improvement.

Visualization: The visualizations showed how the model predicted labels for each token in the input sentence. For example, the model correctly identified "hereditary retinoblastoma" as a disease and "chemotherapy" and "radiation therapy" as treatments.

## Future Work
### Model Improvement:

Explore advanced models or hybrid approaches that combine CRF with other techniques (e.g., deep learning-based embeddings) to enhance performance.
### Data Expansion:

Increase the dataset size and diversity to improve model robustness and generalization.
### Additional Entities:

Extend the model to recognize other types of medical entities or concepts beyond diseases and treatments.
## Real-World Application:

Integrate the model into healthcare applications for automating medical documentation and research.
By addressing these areas, future work can significantly advance the capabilities and accuracy of NER systems in medical contexts.
