# Audio Generator

## About
This repository is an in-progress generative AI system for producing the next FFT frame in an audio file.

## Resource needs
The default training device is CUDA, and MPS is the first fallback, with a CPU as the last-level default. When training, the estimated time remaining is output. This helps with gauging resource consumption.

## Setup
You will need to install the following packages to use this repository:
`aus_analyzer`, `numpy`, `pedalboard`, `torch`, `torchaudio`, `regex`, and `soundfile`.

Visit https://pytorch.org/get-started/locally/ for PyTorch installation instructions (this is a good idea if you want to use CUDA).

The `aus_analyzer` package needs to be compiled separately using `maturin`. Contact the developer of this repository for details.

## Training a model
Install the dependencies listed above, and compile the Cython code, then follow these steps:
1. Specify the location of your audio corpus in the `train.py` file, using the `TRAINING_PATH` variable.
2. Run the `train.py` program. NOTE: Before running, make sure that file locations are correctly specified.
