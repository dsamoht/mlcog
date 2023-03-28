# Gene-based microbiome representation enhances host phenotype classification
The repository contains the ML protocol and data used in the [article](https://github.com/dsamoht/MLCOG). Because the majority of matrices exceed the size limit of Github, they are not included in the repository. To produce the gene clusters matrices with your data, see the [protocol](/doc/geneclusters.md).
## Description

* __main.py__ : command line script.
* __MakeSplits.py__ : produce 100 different train/test splits, apply feature selection and save them in a given directory (on a computer cluster, they are cached into $SLURM_TMPDIR for effiency purpose).
* __Learning.py__: learning protocol with `hyperparameters` tuning and model performance evaluation.

## Dependencies
* numpy, pandas, pickle
* [scikit-learn](https://scikit-learn.org/stable/)
* [pyscm](https://github.com/aldro61/pyscm)
* [randomscm](https://github.com/thibgo/randomscm)

## Usage
*on a computer cluster
```
python3 main.py -ds T2D -dt metaphlan -t $SLURM_TMPDIR
```
## Help
To see the different options available:
```
python3 main.py --help
```
## Authors
* [Thomas Deschênes](https://github.com/dsamoht)
* [Frédéric Raymond](https://github.com/fredericraymond)
