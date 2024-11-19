# Transformers Learn to Achieve Second-Order Convergence Rates for In-Context Linear Regression

This is an official repository for our paper, [Transformers Learn to Achieve Second-Order Convergence Rates for In-Context Linear Regression](https://arxiv.org/abs/2310.17086).


```bibtex
@inproceedings{
    fu2024transformers,
    title={Transformers Learn to Achieve Second-Order Convergence Rates for In-Context Linear Regression},
    author={Deqing Fu and Tian-qi Chen and Robin Jia and Vatsal Sharan},
    booktitle={The Thirty-eighth Annual Conference on Neural Information Processing Systems},
    year={2024},
    url={https://openreview.net/forum?id=L8h6cozcbn}
}
```

Codes are mostly modified from [this prior work](https://github.com/dtsip/in-context-learning/).

## Getting started
You can start by cloning our repository and following the steps below.

1. Install the dependencies for our code using Conda. You may need to adjust the environment YAML file depending on your setup.

    ```
    conda env create -f environment.yml
    conda activate transformers_icl_opt
    ```

2. Download [model checkpoints](https://github.com/dtsip/in-context-learning/releases/download/initial/models.zip) and extract them in the current directory.

    ```
    wget https://github.com/dtsip/in-context-learning/releases/download/initial/models.zip
    unzip models.zip
    ```

3. Run probing for each Transformers layer

    ```
    cd src
    python probing.py
    ```

4. Compute Transformer's similarities to both Iterative Newton's Method and Gradient Descent
   
   ```
   python eval_similarity.py
   ```

   This will plot Fig. 1(a) and Fig. 3 in the [paper](https://arxiv.org/abs/2310.17086), under a new folder `eval`.
