# Machine Learning Classification Project

This project implements supervised learning algorithms on the **Spambase** and **Language** datasets. Both custom implementations and standard models are used to evaluate performance across different hyperparameters and feature combinations.

## Project Overview
The datasets used in this project are:

- **Spambase dataset:** Contains features extracted from emails, labeled as spam or not spam.  
- **Language dataset:** Contains text samples from different languages for classification.

The main goal of this project is to classify the data points correctly using three different algorithms:

- **Perceptron**  
- **Logistic Regression**  
- **Support Vector Machine (SVM)**

Performance is evaluated using **accuracy scores** and **confusion matrices**.

## Project Structure
```
Machine-Learning-Projects/
│
├─ Perceptron_SMV_log.ipynb          # Notebook containing models, experiments, and printed outputs
├─ spambase.data                     # Spambase dataset
├─ spambase.names                    # Spambase feature names
├─ english.txt                       # English dataset
├─ dutch.txt                         # Dutch dataset
├─ English_test_valid.txt            # English test/validation set
├─ Dutch_test_valid.txt              # Dutch test/validation set
├─ Linear_Classification_Models.pdf  # Report summarizing experiments, results, and analysis
└─ README.md
```

## Usage
1. Open the notebook **Perceptron_SMV_log.ipynb** in **Google Colab**.  
2. Results and plots are already included in the notebook.  
3. To reproduce the results, ensure all dataset files are in the same folder as the notebook.  
4. Click **"Run All"** at the top of the notebook to rerun experiments.

## Author
**Anushka Hada** – anhada@ucsc.edu
