# The Temporal Dictionary Ensemble (TDE) Classifier for Time Series Classification

Results for the paper "The Temporal Dictionary Ensemble (TDE) Classifier for Time
Series Classification" published at ECML PKDD 2020, which introduces TDE, a dictionary
based classifier combining advances from earlier dictionary methods with a Gaussian
process based parameter selection, and HIVE-COTE with TDE replacing BOSS (HC-TDE).

The paper is open access and available from
[Springer](https://doi.org/10.1007/978-3-030-67658-2_38).

## Contents

| Path | Description |
|---|---|
| [results/DictionaryComparison.xlsx](results/DictionaryComparison.xlsx) | Test accuracy of six dictionary based classifiers on the UCR datasets (Figure 2) |
| [results/HC-Variants.xlsx](results/HC-Variants.xlsx) | Test accuracy of HIVE-COTE variants with different dictionary components and the state of the art (Figure 7) |
| [results/HC-TDE-vs-SOTA.xlsx](results/HC-TDE-vs-SOTA.xlsx) | Test accuracy of HC-TDE and the state of the art, including ROCKET (Figures 6 and 7) |
| [results/AllMetrics.xlsx](results/AllMetrics.xlsx) | Accuracy, balanced accuracy, AUROC and F1 of all classifiers, averaged over 30 resamples and on the default train/test split, with average ranks |
| [tde.ipynb](tde.ipynb) | Example of using TDE from `aeon` |

Each spreadsheet has a sheet of mean accuracies, a sheet of accuracies on the default
train/test split, and one sheet per classifier with the accuracy on each of 30
resamples. Resample 0 is the default train/test split.

More results, the code and a snapshot of the `tsml` toolkit used in the experiments are
available on Google Drive:

- [Detailed results files](https://drive.google.com/file/d/1xNFmjIBh-wBXU0c1JvHAZC9oU32a4ZfM/view)
  for each classifier and dataset on 30 resamples, which can be processed with the
  `MultipleClassifierEvaluation` class in `tsml`
- [Code used to produce the experiments](https://drive.google.com/file/d/1WRT0xlN0ybsLOORBDWUNVFqiMIHDpEzF/view)
  and the [code as a jar](https://drive.google.com/file/d/1TIORehUURhBnyRSr2BhMGsRzulZ1p-YL/view)

## Datasets

The 112 equal length UCR datasets without missing values are from the
[UCR Time Series Classification Archive 2018](https://doi.org/10.5281/zenodo.11198697),
and are also available as used in the experiments from
[Google Drive](https://drive.google.com/file/d/1jbhAwvg4IhrLhGjCOcLWwwh0vbSoF7gI/view).
More information on the datasets is available at
[timeseriesclassification.com](http://www.timeseriesclassification.com).

## Running TDE

### aeon

TDE is available in the [aeon](https://github.com/aeon-toolkit/aeon) Python package as
`TemporalDictionaryEnsemble`. It follows the `scikit-learn` interface:

    pip install -r requirements.txt

See [tde.ipynb](tde.ipynb) for an example, which can be run online using Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/time-series-machine-learning/temporal-dictionary-ensemble-2020/main?filepath=tde.ipynb)

The example was last checked in November 2026 with `aeon` 1.5.0 on Python 3.12.

### As published

The paper used the Java implementation in the
[tsml](https://github.com/time-series-machine-learning/tsml-java) toolkit, which uses
the WEKA classifier interface. The code and jar used in the experiments are linked
above.

## Citation

If you use this work, please cite the paper:

```bibtex
@inproceedings{middlehurst2020temporal,
  title={The Temporal Dictionary Ensemble ({TDE}) Classifier for Time Series Classification},
  author={Middlehurst, Matthew and Large, James and Cawley, Gavin and Bagnall, Anthony},
  booktitle={Machine Learning and Knowledge Discovery in Databases (ECML PKDD 2020)},
  pages={660--676},
  year={2021},
  publisher={Springer},
  doi={10.1007/978-3-030-67658-2_38}
}
```

## Contact

For questions about the paper or this repository, feel free to contact any of the
authors. Matthew Middlehurst can be reached at
[m.b.middlehurst@bradford.ac.uk](mailto:m.b.middlehurst@bradford.ac.uk) or on the
[aeon Discord](https://discord.gg/D6rzqHGKRJ) (`matthewmiddlehurst`).
