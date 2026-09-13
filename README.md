# Deep Learning Assignment 1 — Fashion-MNIST

This project trains and tunes a neural network on the Fashion-MNIST dataset.
It covers seven parts: backpropagation from scratch, activation study, loss
functions, optimiser comparison, regularisation, and hyperparameter tuning.

## Final Result

- **Test Accuracy:** 86.38%
- **Macro Precision:** 86.48%
- **Macro Recall:** 86.51%
- **Macro F1:** 86.23%

This is a **+14.63 percentage point** improvement over the Part 2 baseline (71.75%).

## Files in This Repo

- `f236014_DLP_A1.ipynb` — the full notebook with all seven parts and outputs
- `Final_Model_Summary.docx` — a one-page summary of the final result
- `README.md` — this file

## Requirements

You need Python 3.9 or higher. Install these packages:

```bash
pip install torch numpy pandas scikit-learn matplotlib jupyter
```

## Dataset

This project uses the Fashion-MNIST training CSV file. The notebook expects
a file named `fashion-mnist_train.csv` in the same folder as the notebook.

You can download it from Kaggle here:
https://www.kaggle.com/datasets/zalando-research/fashionmnist

Place the file in the same folder as the notebook before running it.

## How to Reproduce the Result

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-folder>
   ```

2. Install the required packages (see above).

3. Download `fashion-mnist_train.csv` and place it in the project folder.

4. Open the notebook:
   ```bash
   jupyter notebook f236014_DLP_A1.ipynb
   ```

5. Run all cells from top to bottom, in order. Do not skip any cell.
   Some cells depend on variables created by earlier cells.

6. The final test score will print near the end of Part 7, under the
   heading "Evaluating only ONCE on the test set."

## Notes on Reproducibility

- Random seeds are set with `torch.manual_seed(42)` and `np.random.seed(42)`
  in most cells, so results should be very close to the ones reported here.
- Part 7 uses random search, so the exact hyperparameter search may return
  slightly different top configurations if re-run, even with a seed set,
  due to how PyTorch handles some operations. The final selected
  configuration used in this report was:
  - Learning rate: 0.0019
  - Hidden layer width: 256
  - Dropout rate: 0.487
  - Batch size: 64
  - Optimiser: Adam
  - Training data: 20,000 samples (from Part 6)
