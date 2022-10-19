# RAMP starting kit on the bike counters dataset

![GH Actions](https://github.com/ramp-kits/bike_counters/actions/workflows/main.yml/badge.svg)

## Getting started

### Download the data,

Download the data files,
 - [train.parquet](https://github.com/ramp-kits/bike_counters/releases/download/v0.1.0/train.parquet)
 - [test.parquet](https://github.com/ramp-kits/bike_counters/releases/download/v0.1.0/test.parquet)

and put them to into the data folder.

### Install

To run a submission and the notebook you will need the dependencies listed
in `requirements.txt`. You can install the dependencies with the
following command-line:

```bash
pip install -U -r requirements.txt
```

It is recommended to create a new virtual environment for this project. For instance, with conda,
```bash
conda create -n bikes-ramp python=3.9
conda activate bikes-ramp
pip install -r requirements.txt
```


### Challenge description

Get started on this RAMP with the
[dedicated notebook](bike_counters_starting_kit.ipynb).

First install [Jupyter](https://jupyter.org/):

```bash
pip install jupyter
```

then launch the notebook using:

```bash
jupyter notebook ./bike_counters_starting_kit.ipynb
```

### Test a submission

The submissions need to be located in the `submissions` folder. For instance
for `my_submission`, it should be located in `submissions/my_submission`.

To run a specific submission, you can use the `ramp-test` command line:

```bash
ramp-test --submission my_submission
```

For instance, you can run the provided `starting_kit` submission example with:

```bash
ramp-test --submission starting_kit
```

You should get an output similar to the following one:

<details>

<summary>Example output</summary>

```
Testing Bike count prediction
Reading train and test files from ./data/ ...
Reading cv ...
Training submissions/starting_kit ...
CV fold 0
        score   rmse      time
        train  0.610  0.084952
        valid  0.983  0.408040
        test   0.703  0.033141
CV fold 1
        score   rmse      time
        train  0.663  0.106090
        valid  0.852  0.399937
        test   0.759  0.032243
CV fold 2
        score   rmse      time
        train  0.682  0.170388
        valid  0.891  0.324898
        test   0.771  0.025760
CV fold 3
        score   rmse      time
        train  0.705  0.208704
        valid  0.844  0.324345
        test   0.875  0.024143
CV fold 4
        score   rmse      time
        train  0.728  0.233596
        valid  0.804  0.319224
        test   0.872  0.024262
CV fold 5
        score   rmse      time
        train  0.737  0.280230
        valid  0.939  0.320182
        test   0.863  0.024391
CV fold 6
        score   rmse      time
        train  0.763  0.327653
        valid  1.131  0.316819
        test   0.843  0.025528
CV fold 7
        score   rmse      time
        train  0.793  0.376762
        valid  0.896  0.324821
        test   0.767  0.024473
----------------------------
Mean CV scores
----------------------------
        score             rmse         time
        train   0.71 +- 0.0546   0.2 +- 0.1
        valid  0.917 +- 0.0962  0.3 +- 0.04
        test   0.807 +- 0.0607   0.0 +- 0.0
----------------------------
Bagged scores
----------------------------
        score   rmse
        valid  0.923
        test   0.765

```

</details>

You can get more information regarding this command line:

```bash
ramp-test --help
```

### To go further

You can find more information regarding `ramp-workflow` in the
[dedicated documentation](https://paris-saclay-cds.github.io/ramp-docs/ramp-workflow/stable/using_kits.html)

You can find the description of the columns present in the `external_data.csv`
in `parameter-description-weather-external-data.pdf`. For more information about this
dataset see the [Meteo France
website](https://donneespubliques.meteofrance.fr/?fond=produit&id_produit=90&id_rubrique=32)
(in French).
