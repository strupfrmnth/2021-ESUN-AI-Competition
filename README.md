# 2021-ESUN-AI-Competition
This is a Chinese handwriting recognition project. The dataset is provided by Esun Bank and our group.

## Structure
We put the code and data as the structure below.
```
├── create_images // create images for increasing dataset
│   ├── add_images_2000
│   │   ├── 我
│   │   │   ├──300001_我.jpg
│   │   │   ├──300002_我.jpg
│   │   │   └── ...
│   │   └── ...
│   ├── isnull
│   │   └── ...
│   ├── add_images.py
│   └── word2000.txt
├── model_data  // for model training and testing
│   ├── train
│   │   ├── 戶
│   │   │   ├──0_戶.jpg
│   │   │   ├──1_戶.jpg
│   │   │   └── ...
│   │   ├── 經
│   │   └── ...
│   ├── val
│   │   └── ...
│   └── test
│       └── ...
├── esun_data // for model evaluation, structure also like model_data
│   └──...
├── models
│   └── efficientnet-b3-3000.pth
├─ EfficientNet-3000.ipynb
├─ Evaluation.ipynb
├─ idx2class3000.pkl
├─ wordset800.txt
└─ README.md
```
## Training
We use 'model_data' to train model. 'model_data' is part of Esun Bank data and our created images.

Run EfficientNet-3000.ipynb to train the model.

## Evaluation
We use 'idx2class3000.pkl' to change the indices of model prediction into Chinese words for simplicity. 'wordset800.txt' is the 800 classes of the competition. We transform the words which is not in 800 classes into 'isnull'.

Run Evaluation.ipynb to evaluate the model.

## Create Images
We use the plain images provided by Esun Bank to draw text on them. Plain images are put in 'isnull' folder and 'word2000.txt' provides the common words of 2037 classes which is not in the competition classes.

Run add_images.py to create images.
