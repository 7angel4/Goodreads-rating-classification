This folder contains the majority of resources used in the report and `Main.ipynb`.

The "Datasets" folder contains different versions of the train and test set, in CSV format:
- book_rating_train: The original training set provided
- train_df: identical to train_df_50 below (for simplicity of reference) 
- train_df_50: The preprocessed training set retaining 50 TF-IDF-features (respectively for 'Name' and 'Description').
  * SNB (Stacking Naive Bayes) and SClf (Stacking Classifier), are trained on this dataset.
- train_df_100: The preprocessed training set retaining 100 TF-IDF-features.
- train_df_200: The preprocessed training set retaining 200 TF-IDF-features.
- train_df_300: The preprocessed training set retaining 300 TF-IDF-features.
  * LogR is trained on this dataset.
- LSVM_train: The feature-selected version of train_df_50. The features were selected using Cross-Validated Recursive Feature Elimination (RFECV) on the linear SVM classifier.
  * LSVM is trained on this dataset.
  
The test set files follow the same naming conventions.
 
The "Figures" folder contains the figures used in the report, in PNG format. 
These were generated from the `*_supplementary.ipynb` notebooks.

Other resources:
- BNB_features.txt: The features used by Bernoulli Naive Bayes (a base model in SNB).
- MNB_features.txt: The features used by Multinomial Naive Bayes (a base model in SNB).
- LSVM_RFECV_results.csv: The performance scores of LSVM over multiple iterations of RFECV.
  * This file is pre-generated, since RFECV takes too long to run.
  * The sample code for one iteration is included in `LSVM_supplementary.ipynb`.