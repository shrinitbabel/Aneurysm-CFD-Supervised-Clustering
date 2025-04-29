# readme

## Overview
This project aims to develop a predictive model for aneurysms using machine learning techniques. By analyzing patient data and aneurysm characteristics, we seek to identify patterns and predictors that can help in early detection and intervention. The Jupyter Notebook `supervised_clustering_analysis.ipynb` contains the code and methodology for preprocessing data, training models, and evaluating their performance.

The contents of this repository have been submitted for consideration to a scholarly journal and are subject to copyright protection. Unauthorized duplication or reproduction is prohibited. 
## Prerequisites
To run this notebook, you need the following installed:
- Python 3.x
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## Installation
Ensure you have Python and Jupyter Notebook installed on your system. You can install the required Python libraries using the following command:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn

```

## Usage
To use the Aneurysm_Prediction.ipynb notebook:

1. Clone this repository or download the files to your local machine.
2. Navigate to the directory containing the notebook.
3. Launch Jupyter Notebook by running jupyter notebook in your terminal or command prompt.
4. Open Aneurysm_Prediction.ipynb from the Jupyter Notebook interface.
5. Run the cells in sequence to perform data loading, preprocessing, model training, and evaluation.

# Aneurysm Prediction Model

## Datasets
The analysis utilizes one primary dataset:
- `Merged_Aneurysm.csv`: A merged dataset combining patient demographics with aneurysm-specific information from Computational Flow Dynamics (CFD) to provide a comprehensive overview for analysis. The `Data Source` is the [Emory AneuriskWeb Dataset](http://ecm2.mathcs.emory.edu/aneuriskweb/repository)

## Preprocessing
Preprocessing steps included:
- Removing non-predictive features (e.g., 'case_id', 'patient_id').
- Encoding categorical variables using one-hot encoding.
- Imputing missing values in numerical features.
- Scaling features to standardize the data range.

## Feature Selection
Feature selection was performed to identify the most predictive features. Methods included:
- Correlation analysis to remove highly correlated features.
- Recursive Feature Elimination with Cross-Validation (RFECV).
- Grid Search to optimize hyperparameters.

## Model
A K-Nearest Neighbors (KNN) classifier was chosen due to its simplicity and effectiveness for small datasets.

### Hyperparameters
- `n_neighbors`: The number of neighbors to consider. Optimal value determined through cross-validation.
- `weights`: Weight function used in prediction. Options include 'uniform' or 'distance'.
- `p`: Power parameter for the Minkowski metric.

## Evaluation
The model was evaluated using accuracy and a classification report that includes precision, recall, and F1-score for both 'Ruptured' and 'Unruptured' classes.

## Features
The following features are used in the model to predict aneurysm rupture status:

- Age of the patient (`age`)
- Aneurysm sac volume (`sacVolume`)
- Surface area of the aneurysm sac (`sacSurfaceArea`)
- Volume of the vessel dissection cavity (`vdcVolume`)
- Surface area of the vessel dissection cavity (`vdcSurfaceArea`)
- Cross-sectional area of the aneurysm sac (`sacSectionArea`)
- Volume of the ellipsoid model of the aneurysm sac (`ellipsoidVolume`)
- Maximum semi-axis length of the ellipsoid model (`ellipsoidMaxSemiaxis`)
- Mid semi-axis length of the ellipsoid model (`ellipsoidMidSemiaxis`)
- Minimum semi-axis length of the ellipsoid model (`ellipsoidMinSemiaxis`)
- Centerline length of the aneurysm sac (`sacCenterlineLength`)
- Area of the ostium, or the opening of the aneurysm (`ostiumSectionArea`)
- Perimeter of the ostium (`ostiumSectionPerimeter`)
- Minimum size of the ostium (`ostiumMinSize`)
- Maximum size of the ostium (`ostiumMaxSize`)
- Shape factor of the ostium (`ostiumShapeFactor`)
- Aspect ratio of the aneurysm sac (`aspectRatio_star`)
- Size ratio of the aneurysm sac (`sizeRatio_star`)
- Diameter of the vessel from which the aneurysm sac protrudes (`vesselDiameter`)
- Angle between the neck of the aneurysm sac and the vessel (`neckVesselAngle`)
- Angle between the aneurysm sac and the vessel (`sacVesselAngle`)
- Average radius of the vessel (`meanRadius`)
- Average curvature of the vessel (`meanCurvature`)
- Average torsion of the vessel (`meanTorsion`)
- Tortuosity of the vessel (`tortuosity`)
- Minimum radius of the vessel (`minRadius`)
- Maximum radius of the vessel (`maxRadius`)
- Maximum curvature of the vessel (`maxCurvature`)
- Maximum torsion of the vessel (`maxTorsion`)
- Angle in the plane of the bifurcation (`bifurcationAngleInPlane`)
- Angle out of the plane of the bifurcation (`bifurcationAngleOutOfPlane`)

## Results
The results section provides an in-depth analysis of the models' performance.

## Contact
Shrinit Babel - shrinitbabel@gmail.com

Project Link:

## Acknowledgements
We would like to extend our gratitude to the AneuriskWeb project and team for providing access to their valuable dataset. The AneuriskWeb project is hosted by the Department of Mathematics and Computer Science at Emory University. 

## Citations
AneuriskWeb project website, http://ecm2.mathcs.emory.edu/aneuriskweb. Emory University, Department of Math&CS, 2012.
