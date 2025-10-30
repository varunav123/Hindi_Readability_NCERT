# Hindi Readability using NCERT Textbooks
This repository contains the NCERT dataset consisting of prose text from grades 1 to 8. Each .txt file contains 1 grade's text.
The ipynb file named ncertdataexp.ipynb contains self contained code with installation for all the libraries required. It can be loaded on Google Colab and run by uploading each .txt file from the dataset. A .py file for the same code has also been provided to preview the code, or to run all the tasks at once
The name of the files is set according to the number of lines in that file, and the code file stores the files' content in the appropriate variable.
File names and path may need to be changed to run the files in local environment.
The code file follows the following flow:
  1. Load text data (stories) for grades 1 through 8.
  2. Generate baseline readability scores (Levels 1-6) for each sentence using the finetuned Muril-base model provided by readmepp library, provided by Naous et al, 2024.
  3. Implement six surface level features based on Hindi linguistic characteristics (e.g., matras, Jukta Akshars).
  4. Train a Linear Regression model to predict the readability scores obtained from the Muril-base model using these six features.
  5. Evaluate the model using cross-validation and statistical analysis (OLS).
  6. Visualize dataset distribution and results.

The code also contains some holdover code from previous experiments, such as code for a random forest model, additional feature implementation, code to compile the complete dataset and its statistical values in a .csv file. These can be commented out, or added to to conduct additional experiments on the dataset.
T4 GPU provided by a free Google Colab account is enough to run all the code given in the file under 15 minutes. 
# Dependencies  
  1. readmepp: For generating baseline readability scores (Hindi).
  2. indic-nlp-library: For Indic language processing. Can use in-built python string parsing tools instead, the current ipynb uses in-built methods.
  3. pandas & numpy: For data manipulation.
  4. scikit-learn: For Linear Regression, metrics, and cross-validation.
  5. statsmodels: For OLS regression analysis (P-values, T-values).
  6. matplotlib & seaborn: For plotting (Heatmap, Violin plots).

All the latest versions of each library have been used as of 30/10/2025, in Python version 3.12.12
