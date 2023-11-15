---
layout: page
title: Lightning: module and data_module is all you need
permalink: posts/lightning/
---

## Lightning: module and data_module is all you need
To start a ML task with lightning and without complex training settings, you only need:
- Module
    - An available pytorch model - you can always find one
    - Add `self.save_hyperparameters()`
    - Change the inherit object type from nn.module to LightningModule
    - Add `loss_fuc`, `training_step`, `validation_step`, `test_step`, `predict_step` - if you have ever written or found them once, you just copy & paste them for the rest of your life

- Data module
    - A dataset with `__getitem__ ` method returns x and y - you know what they mean
    - A data_module divide your dataset into train/val/test
    - `train_dataloader`, `val_dataloader`,`test_dataloader`, `predict_dataloader` - also a copy & paste thing

- Trainer
    - Trainer will do train, test and predict for you
    - Hyperparameter will be saved automatically
    - Log will be saved, loss will show with progress bar
