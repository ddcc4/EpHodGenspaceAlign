**EpHod**
===============

.. image:: https://zenodo.org/badge/DOI/10.5281/zenodo.15015124.svg
   :target: https://doi.org/10.5281/zenodo.15015124
   :alt: DOI

EpHod is a deep-learning model to predict the optimum pH of enzymes (pHopt). The model is of an ensemble of a neural network (residual light attention or RLAT) and a support vector regression (SVR) model both trained on top of ESM-1v embeddings. The neural network (RLATtr) was first pretrained using 1.9 million proteins with optimal environment pH (pHenv) labels, followed by fine tuning using 9,855 enzyme with catalytic optimum pH labels (pHopt).

We recommend using a conda environment. Dependencies are in `env.yml`. The code was successfully run with PyTorch v1.7.0 and CUDA v 11.7.
Weights of EpHod model and training datasets are available at `Zenodo <https://doi.org/10.5281/zenodo.14252615>`__.



Usage 
-------------

Conda is too annoying. Here's a quicker way to get this running:

.. code:: shell-session

  pip install numpy pandas torch scikit-learn fair-esm tqdm

  python ephod/run.py --csv_path=path/to/predictive-pet-zero-shot-test-2025.csv
..

The output will be in a file called ``prediction.csv``


Citation
----------
If you find EpHod useful, please cite the following:

Gado J.E., Knotts M., Shaw A.Y., et al, 2025. "Machine learning prediction of enzyme optimum pH". `Nature Machine Intelligence <https://doi.org/10.1038/s42256-025-01026-6>`__.

