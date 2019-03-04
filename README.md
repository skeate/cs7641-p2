# Assignment 2 - Randomized Optimization

The code for this assignment chooses three toy problems, but there are other options available in _ABAGAIL_.

## General

If you are running this code in OS X you should consider downloading Jython directly. The version provided by homebrew does mot seem to work as expected for this code.

## Data

The data loading code expects datasets to be stored in "./data".

The code is currently set up to use the [Gestures dataset](https://www.kaggle.com/kyr7plus/emg-4).
Concatenate the four .csv files into one, located at ./data/gestures.csv.

Because _ABAGAIL_ does not implement cross validation some work must be done on the dataset before the other code can
be run. The data can be generated via

```
python run_experiment.py --dump_data
```

Be sure to run this before running any of the experiments.

## Output

Output CSVs and images are written to `./output` and `./output/images` respectively. Sub-folders will be created for
each toy problem (`CONTPEAKS`, `FLIPFLOP`, `TSP`) and the neural network from the _Supervised Learning Project_ (`NN_OUTPUT`, `NN`).

If these folders do not exist the experiments module will attempt to create them.

## Running Experiments

Each experiment can be run as a separate script. Running the actual optimization algorithms to generate data requires
the use of Jython.

For the three toy problems, run:

- continuoutpeaks.py
- flipflop.py
- tsp.py

For the neural network problem, run:

- NN-Backprop.py
- NN-GA.py
- NN-RHC.py
- NN-SA.py
