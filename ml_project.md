This post is an archieve for machine learning project structure for effectively organize an clean and colaborateable project. [Source](https://medium.com/@l.charteros/scalable-project-structure-for-machine-learning-projects-with-pytorch-and-pytorch-lightning-d5f1408d203e)
```
.
├── .data
│   ├── processed
│   │   ├── test.csv
│   │   └── train.csv
│   └── raw
│       └── data.csv
|
├── .experiments
│   └── model1
│       ├── version_0
|       |   └── ...
|       └── ...
└── src
    |
    └── ml
        ├── data
        │   ├── make_dataset.py
        │   └── preprocessing.py
        |
        ├── datasets
        │   ├── dataset1
        │   |   ├── datamodule.py
        │   |   └── dataset.py
        |   └── ...
        |
        ├── models
        │   ├── model1.py
        │   └── model2.py
        |
        ├── scripts
        │   ├── predict.py
        │   ├── test.py
        │   └── train.py
        |
        └── utils
            ├── constants.py
            └── helpers.py
```
