# PODS: Potential Outcomes for Deferring Systems

We provide here the code associated to the paper A causal framework for evaluating deferring systems.

## Setup

To install the required packages from our `environment.yml` file, run the following command:

```
conda env create -f environment.yml
```

To activate the environment, run the following command:

```
conda activate pods
```

## Running the code

To run the code, you can use the following command:

```
python train.py -data all --defer_system all --seed 42
```

This will train the models for all the datasets and all the deferring systems. 
The results will be saved in the `resultsRAW` folder.

To obtain the final estimates for Q1 and Q3 included in our paper, you can run the following command:

```
python test.py
```

The first command will produce the final estimates for all the datasets and all the deferring systems for Q1 and Q3.

To obtain the final estimates for Q2 included in our paper, you can run the following commands:

```
python demographic.py
python test_conditional.py
```

The first command adds the demographic information to the `xray-airspace` dataset.
The second command will produce the final estimates for all the datasets and all the deferring systems for Q2.
The results will be saved in the `results` folder.

If you do not want to train the models from scratch, you can download them from [here](https://www.dropbox.com/scl/fo/6rxx0sy4dq1c86aqgw5sr/AIdZeeWh6yeSohg4oLjiJKY?rlkey=1in2itm23tx1nh4jaaht4hxwm&dl=0).

All the plots for the main paper and the tables can be retrieved from running the Jupyter notebooks in the `notebooks` folder.
To obtain the plots for density estimation, run the `density_estimation.R` file.

## References

*A Causal Framework for Evaluating Deferring Systems*. Filippo Palomba, Andrea Pugnana, Jose M. Alvarez, and Salvatore Ruggieri. International Conference on Artificial Intelligence and Statistics (AISTATS), 2025.

If you make use of the code, the simulated data, or the evaluation framework in your work, please cite the following paper:

<pre><code>
@inproceedings{DBLP:conf/aistats/PalombaPAR25,
  author       = {Filippo Palomba and
                  Andrea Pugnana and
                  Jos{\'{e}} M. {\'{A}}lvarez and
                  Salvatore Ruggieri},
  title        = {A Causal Framework for Evaluating Deferring Systems},
  booktitle    = {{AISTATS}},
  series       = {Proceedings of Machine Learning Research},
  volume       = {258},
  pages        = {2143--2151},
  publisher    = {{PMLR}},
  year         = {2025}
}
</code></pre>
