# Human Activity Recognition using Torch7

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)

Recognize human activities of individuals using body pose joint annotations on video sequences.


# WARNING

This repo is a work in progress. This warning shall be removed when code is working. For now, this repo represents only the scafold structure for the code.

## Installation

### Requirements

- NVIDIA GPU with compute capability 3.5+ (2GB+ ram)
- [Torch7](http://torch.ch/docs/getting-started.html)
- [dbcollection](https://github.com/dbcollection/dbcollection-torch7)

### Packages/dependencies installation

To use this example code, some packages are required for it to work.

```bash
luarocks install loadcaffe
luarocks install cudnn
```

### dbcollection

To install the dbcollection package do the following:

- install the Python module (Python>=2.7 and >=3.5).

```
pip install dbcollection
```

- install the Lua/Torch7 dbcollection wrapper:

    1. download the Lua/Torch7 git repo to disk.

    ```
    git clone https://github.com/dbcollection/dbcollection-torch7
    ```

    2. install the package.
    ```
    cd dbcollection-torch7 && luarocks make
    ```

> For more information about the dbcollection package see [here](https://github.com/dbcollection/dbcollection-torch7).


# Getting started

## Download/Setting up this repo

To start using this repo you'll need to clone this repo into your home directory:

```
git clone https://github.com/farrajota/human_activity_torch
```

By default, this repo points to the home directory when running the scripts. If you want to save it into another directory, just remember to edit the `projectdir.lua` file and set the proper path to the save directory.

Next, you'll need to setup the necessary data for this code to run. First, download the `VGG16` model by running the `download_vgg.lua` script in the `download/` dir:

```
th download/download_vgg.lua
```

The `vgg16` model uses the `cudnn` library, so make sure this package is installed on your system before proceeding any further.

## Train

To train a network, simply run the `train.lua` script to start optimizing a pre-defined network (vgg16 + LSTM). This script is configured to train the network specified in the paper [TODO- insert paper link]().

In the `scripts/` dir there are several scripts to train other networks with different networks and on different conditions. Check them out to see more training configurations specs.

## Test

TODO

## Demo

TODO

## Results

TODO

## License

MIT license (see the [LICENSE](LICENSE.md) file)