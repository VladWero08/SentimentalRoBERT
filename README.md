# RomanianBERT

### Structure of model.json
- *title*: boolean, *true* if the title of the reviews was used, *false* otherwise
- *content*: boolean, *true* if the content of the reviews was used, *false* otherwise
- *laroseda_split*: boolean, *true* if the LaRoSeDa default split was used, *false* otherwise
- *preprocessing*: list, methods used to preprocess the text before tokenizing it
- *optimizer*: string, the optimizer used for training
- *learning_rate*: string | float
- *path*: string, where the full models is saved
- *epoch*: list, all epochs of training and testing, each one of them defined as:
  - *train_loss*: float
  - *validation_loss*: float
  - *validation_accuracy*: float
  - *validation_precision*: float
  - *validation_recall*: float
  - *validation_f1*: float
