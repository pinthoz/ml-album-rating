# EIACD (CC1023) - 2022/23 - Practical Assignment 2

## Prevision of Critics Review Scores for Music Albums

### Ana Silva Pinto (up202105085) and Fani Neto (up19900325)
**Faculdade de Ciências - Universidade do Porto**


## Introduction
This notebook uses machine supervised learning classification algorithms to predict if a certain music album has good or bad critic reviews, according to four scores: bad, mediocre, good, or great.

The music albums dataset used was obtained in https://www.kaggle.com/datasets/tobennao/rym-top-5000   

In the notebook, the **Decision Tree Classifier** as well as the **k-Nearest Neighbors (kNN)** classification algorithms, both from Scikit learn modules, are used.

For classification based on the **decision tree** algorithm, both the **holdout** (70/30 for train/test data subsets) and **K-fold cross-validation (CV)** methods are tested. 

In the holdout method, a searh for the **best max_depth and best min_samples_split parameters** is performed.
In the CV method, a k of 10 folds to partition the dataset is used, and a combination of CV with the Grid Search algorithm is performed to obtain first the best (**'max_depth'** and **'max_features** to build the tree. Then a more detailed analysis of the best choices of other parameters is performed (**'max_depth', 'max_features', 'criterion', 'min_samples_split', 'splitter'**), in order to build the decision tree.

In the **kNN** classification algorithm, a search for the **best value of k** is performed. Also, **CV with 10-folds** is used to evaluate how the accuracy of the KNN classifier depends on the value of k.

The metrics **accuracy**, **precision**, **recall** and **F1-score** are used to assess the performance of the Decision Tree Classifier, by using the best parameters found, and of kNN Classifier with the best k value. 


## Coding language

Python 3.10.11
Python Libraries (Pandas, Numpy, ScikitLearn, Matplolib, Graphviz, Seaborn, Warnings, IPython)


## Files

### Code files and files needed to run the notebook:

Besides this README.md file, the following files are included:

- Jupyter notebook: EIACD_Assignment_2_Group_Media_K-FINAL.ipynb
- One .csv file corresponding to the dataser used: albums.csv
- One .png file corresponding to an image explaining the concept behind a decision tree: Decisiontree.png

   All these files should be stored in the same directory as the Jupyter notebook file.

### Additional files:

In addition, the following files are included:
- pdf version of the Jupyter notebook: EIACD-Assignment_2-Group_Media_K_notebook_PDF.pdf
- decision trees generated when running the code:
		- Decision_tree-albums_imbalanced dataset.pdf
		- Decision_tree-albums_imbalanced dataset (.dot)
		- Decision_tree-albums dataset.pdf
		- Decision_tree-albums dataset (.dot)

- pdf version of the slides of Powerpoint presentation: EIACD_Assignment_2_Group_Media_K.pdf

We include the pdf version of the Notebook because there may be some formatting lost when the notebook is transferred to another computer (due to the use of formatted output) and opened in Jupyter Notebook. In this process some formatted text may be lost.

To visualize the output in full extent and quality requires the Notebook to be run locally in the new computer. Except for the cross validation with a grid search for several parameters, which takes a few minutes to run, all the remaining cells run in acceptable execution time. 

May 24, 2023
