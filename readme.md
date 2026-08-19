# PyTorch

Working notebooks from learning deep learning with PyTorch — tensors and autograd through to convolutional networks on custom image datasets.

## Contents

| Notebook | Topic |
|---|---|
| `fundamentals.ipynb` | Tensors, shapes, dtypes, device handling, autograd |
| `workflows.ipynb` | The end-to-end loop: data → model → loss → optimizer → train → evaluate |
| `workflows_red0.ipynb` | Second pass at the same workflow, rebuilt from scratch |
| `classification.ipynb` | Binary and multi-class classification, non-linearity, decision boundaries |
| `cv_and_cnn.ipynb` | Computer vision basics and the first convolutional architectures |
| `cnn2.ipynb` | Deeper CNN work |
| `custom_datasets.ipynb` | Loading your own image data with `Dataset` and `DataLoader` |
| `random_tests.ipynb` | Scratchpad |
| `CNN_pracice/` | Standalone CNN exercises |

`helper_functions.py` holds shared plotting and evaluation utilities — accuracy, decision boundary plots, loss curves — imported across the notebooks rather than redefined in each.

## Setup

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

If you have a CUDA GPU, install the matching PyTorch build from [pytorch.org](https://pytorch.org/get-started/locally/) instead of the default CPU wheel. The notebooks set device with the usual `torch.device("cuda" if torch.cuda.is_available() else "cpu")` pattern, so they run either way — just slower on CPU.

## Notes

Datasets are downloaded at runtime and excluded from version control.