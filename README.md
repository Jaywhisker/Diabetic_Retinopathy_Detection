# Diabetic_Retinopathy_Detection
This is the repository for 60.001 Applied Deep Learning Diabetic Retinopathy Severity Detection CNN Project. 
<br/>
The report can be found here: https://drive.google.com/file/d/1c9fDaT3SttWfrUAfwUnbV0ts4Tupdc_h/view?usp=sharing

## Setup
### Library Dependcies
Run the following code to download all required libraries for the first setup
```
git clone https://github.com/Jaywhisker/Diabetic_Retinopathy_Detection.git
cd Diabetic_Retinopathy_Detection
pip install -r requirements.txt
```
___
### Dataset
Please download the dataset here: https://drive.google.com/drive/folders/1A4Fo2uBpeNlDQ6iH1IEG8QUbIZBTPPBP?usp=sharing

Export the dataset and move the `Classification` and `Segmentation` folder into the input folder.
___

## Running the code
To train your own models, please follow run the different notebooks in the `/notebooks` folder. 

Note: You do not need to run the `dataset_creation.ipynb` as the dataset has already been curated
```
├── notebooks
│   ├── dataset_creation.ipynb                    <- notebook to create the dataset for Ben Graham's processing, Segmentation with OpenCV and UNET segmentation
│   ├── diabetic_retinography_training.ipynb      <- notebook to train all classification models mentioned in the report
│   ├── lesion_segmentation.ipynb                 <- notebook to train a binary and multiclass u-net model for lesion segmentation
│   └── vessel_segmentation.ipynb                 <- notebook to train a binary u-net model for vessel segmentation
```

## File Structure
```
Diabetic_Retinopathy_Detection
├───input                        <- folder for the dataset
├───models                       <- folder containing the DenseNet and MaxVit models that resulted in the best svm as well as the best svm model
│   ├───ben
│   ├───lesion                   <- folder containing binary and multiclass u-net lesion model
│   ├───opencv
│   ├───unet_b
│   ├───unet_m
│   └───vessel                   <- folder containing binary u-net vessel model
├───notebooks
└───results
    ├───classification           <- folder containing svm results
    └───segmentation             <- folder containing dice coefficient and jaccard index results from u-net
```
