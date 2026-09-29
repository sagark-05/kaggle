# Digit Recognizer

A handwritten digit classification project using the MNIST-style Digit Recognizer dataset. The notebook builds and trains a small neural network using NumPy, then checks predictions on a validation split and displays a few example images.

## Model

The network takes 784 pixel values as input (28 x 28 grayscale image), uses a 10-unit hidden layer with ReLU activation, and produces probabilities for the 10 digit classes with softmax. Weights are trained with backpropagation and gradient descent.

The notebook shuffles the training data, reserves 1,000 rows for validation, normalizes pixel values to the range 0-1, and runs 500 training iterations with a learning rate of 0.10.

## Project files

- `digit_recognizer.ipynb` - data preparation, model implementation, training, and validation examples.
- `train.csv` - labeled training images. The `label` column contains the digit; the remaining 784 columns contain pixel values.
- `test.csv` - unlabeled images supplied with the dataset. The current notebook does not yet use this file.
- `sample_submission.csv` - example Kaggle submission format. The current notebook does not yet generate a submission file.

## Run the notebook

### In Kaggle

1. Add the Digit Recognizer competition data to a Kaggle notebook.
2. Open `digit_recognizer.ipynb` in Kaggle or upload its cells to a Kaggle notebook.
3. Run the cells from top to bottom. The training CSV path in the notebook is set to `/kaggle/input/competitions/digit-recognizer/train.csv`.

### Locally

Use Python 3 and install the notebook dependencies:

```bash
python -m pip install numpy pandas matplotlib kagglehub jupyter
```

Open the project notebook:

```bash
jupyter notebook digit_recognizer.ipynb
```

The notebook currently uses a Kaggle-specific CSV path. To run it locally, change the `pd.read_csv(...)` path in the data-loading cell to:

```python
data = pd.read_csv("train.csv")
```

Then run the cells in order.

## Notes

- The notebook uses a random shuffle, so the validation split and learned weights can vary between runs.
- No accuracy score is reported here because the notebook has not been run as part of this repository.
- The supplied test data is not currently used for inference or submission generation.