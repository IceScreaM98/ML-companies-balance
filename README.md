# ML-companies-balance
This small project aims for the evaluation of ML models on a set of different datasets containing 
companies' financial balances.

This repository can be seen as a sort of "collection" of all the different dataset built from the raw files 
(.xlsx and .csv formats) provided from AIDA. All the used records come from Italian companies ranging from
North and South Italy and a wide range of different financial-economic "status".

The root directory provides a simple requirements.txt which allows to create a working python runtime with required
version of each used library. Furthermore on each notebook there is a small starting section that includes
the basic instructions to install the used libraries for that specific notebook.

## Repository structure

All the files cited are mostly jupyter notebooks, with only a few exceptions.

```
    /Application/*.ipynb
```
Notebook that builds a Gradio application from an exported scikit-learn model .sav file.

```
    /AutoML/*.ipynb
```
Notebook that searches for the best supervised model using the TPOT library.

```
    /Data_ETL/*.ipynb
```
The core of the data pipeline process in charge of different topics like:

- Loading data from raw csv and xlsx file
- Data cleaning
- Data transformation
- Invalid data filtering
- Outlier filtering
- etc.

Each notebook generates a dataset with a certain number of features and records that depends on the type of requested
analysis. For example, certain dataset will contain only a subset of raw features, etc.

In this section under the folder "Limiti01012018" there is a point map of the Italy country in order to generate the
geographical heatmap of the dataset.

```
    /ML_model/*.ipynb
```

The core of the model pipeline divided in five categories:

- Decision Tree Models
- Random Forest Models
- Gradient Boosting Models
- Logistic Regression Models
- Support Vector Machines Models

Each one is customizable with a series of parameters at the head of the interested notebook like:

- train/test split
- imbalanced data technique
- dimensionality reduction algorithm
- model exclusive parameters (like the number of tress for the Random Forest one)
- etc.

Plus it is possible to export each obtained model score into a simple file in order to generate a series of plot to
show the difference of each configuration.

N.B. this repository is used only as a scientific research, the code could be written in a more sophisticated way, but 
for the sake of simplicity and testing a loto of different scenarios the code is stored as separated notebooks.