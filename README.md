# Chess-AI 
Chess-AI trained using deep learning techniques with PyTorch Lightning and a dataset of chess positions and evaluations from Lichess.

## Overview

This project trains a neural network to evaluate chess positions. The model is trained on a dataset of chess positions and their corresponding evaluations, obtained from Lichess. The dataset contains over 37 million evaluations, providing a rich source of data for training the model.

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/ameykunte/Chess-AI.git
   ```
2. Install the required dependencies:
   ```
   pip install peewee pytorch-lightning
   ```

## Dataset

The dataset used in this project is the "2021-07-31-lichess-evaluations-37MM.db" SQLite database, which contains chess positions in FEN notation and their corresponding evaluations. You can download the dataset using the following command:
```
wget https://storage.googleapis.com/chesspic/datasets/2021-07-31-lichess-evaluations-37MM.db.gz
gzip -d "2021-07-31-lichess-evaluations-37MM.db.gz"
```

## Model

The neural network model is implemented using PyTorch Lightning. It consists of multiple linear layers with ReLU activations, with the number of layers being configurable. The model is trained to minimize the L1 loss between the predicted and actual evaluations.

## Training

To train the model, simply run the following command:
```
python train.py
```

You can modify the `configs` variable in the `train.py` script to experiment with different configurations of the model, such as the number of layers and batch size.

## Evaluation

The trained model can be evaluated on a set of random chess positions from the dataset. The evaluation includes the predicted evaluation, actual evaluation, and the loss. Additionally, the positions can be visualized using the SVG format.

## Conclusion

This project demonstrates how to train a neural network to evaluate chess positions using PyTorch Lightning and a large dataset from Lichess. The model can be further improved and customized to suit different requirements and applications in the field of chess AI.
