# tf-deep-omr

TensorFlow code to perform end-to-end Optical Music Recognition on monophonic scores through Convolutional Recurrent Neural Networks and CTC-based training.

## Citation

This repository was used for the experiments reported in the paper:

[End-to-End Neural Optical Music Recognition of Monophonic Scores](http://www.mdpi.com/2076-3417/8/4/606)

```
@Article{Calvo-Zaragoza2018,
  AUTHOR = {Calvo-Zaragoza, Jorge and Rizo, David},
  TITLE = {End-to-End Neural Optical Music Recognition of Monophonic Scores},
  JOURNAL = {Applied Sciences},
  VOLUME = {8},
  YEAR = {2018},
  NUMBER = {4},
  ARTICLE NUMBER = {606},
  URL = {http://www.mdpi.com/2076-3417/8/4/606},
  ISSN = {2076-3417},
  DOI = {10.3390/app8040606}
}
```
## Installation
### Install conda
Install Miniconda or Anaconda

#### Download Miniconda
- Go to the [Miniconda download page](https://docs.conda.io/en/latest/miniconda.html).

### Download Anaconda
- Visit the [Anaconda download page](https://www.anaconda.com/products/distribution).

### Clone the repo
`git clone https://github.com/MasonDill/tf-end-to-end.git`

### Switch to branch
`git fetch origin tf2c && git checkout tf2c`

### Set up the conda enviroment
#### Install the tf conda enviroment
`conda env create -f environment.yml`

#### Activate the tf conda enviroment
`conda activate tf`

### Modify config.json
1. Set `corpus_path` to the directory containing the Primus dataset
2. Set `model_path` to a directory that will store the model outputs

### Modify model.json
You may wish to adjust `max_epochs` and `save_period_epochs`.

### Modify otfa.json
You may wish the adjust the augmentation.

## Usage
### Training
`python .\ctc_training.py`
- no augmentation
`python .\ctc_training.py -weave-distortions-ratio 0.15`
- 15% augmentation rate
