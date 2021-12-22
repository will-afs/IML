
# IML

Practical works of "Introduction to Machine Learning" lecture at MS SIO, CentraleSupélec.
    
From a chosen dataset, the goal is to :
- preprocess data in order to exploit it, 
- and then find the most relevant ML algorithm and parameters to predict intel.

The dataset is chosen by the team from an open-data portal.</p>

## Projet documentation

Available (in French) at "doc/Rapport.pdf"

## Chosen dataset

The dataset is accessible at [this link](https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+from+Single+Chest-Mounted+Accelerometer#).

- The dataset collects data from a wearable accelerometer mounted on the chest
- Sampling frequency of the accelerometer: 52 Hz
- Accelerometer Data are Uncalibrated
- Number of Participants: 15
- Number of Activities: 7
- Data Format: CSV

Labels are codified by numbers :
1. Working at Computer
2. Standing Up, Walking and Going up\down stairs
3. Standing
4. Walking
5. Going Up\Down Stairs
6. Walking and Talking with Someone
7. Talking while Standing

In a first approcch, we have chosen to only consider the dataset of the 1st participant.

## Preprocessing of the dataset

Refer to the documentation and to the files :
- "src/transitory_regimes_correction.ipynb" (working),
- "src/data_aggregation.ipynb" (working),
- "src/angle_correction.ipynb" (not working - the resolution of the equation to find angle theta (see the project documentation) does not converge)

## ML alogorithm trained from the datasets

The goal is to train a ML algorithm which could be able to predict the kind of activity, according to acceleration measurements.

We are in the case of a classification problem.

Several approaches are avaluated :
- KNN (K Nearest Neighbours) - supervised approach -> see script "src/KNN_activity_from_acceleration.ipynb" (working)
- DTC (Decision Tree Classifier) - supervised approach -> see script "src/DTC_activity_from_acceleration.ipynb" (working)

Other methods can be considered, but are not used here :
- Kmeans - unsupervised approach -> see script "Kmeans_activity_from_acceleration.ipynb" (not working)
- PCA (Principal Component Analysis) -> see template script "src/template_scripts/08_PCA_Data_Visualization_Iris_Dataset.ipynb"


