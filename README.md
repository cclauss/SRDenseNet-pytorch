# SRDenseNet-pytorch
# PyTorch LapSRN
Implementation of paper: "Deep Laplacian Pyramid Networks for Fast and Accurate Super-Resolution"(http://vllab1.ucmerced.edu/~wlai24/LapSRN/) in PyTorch

## Usage
### Training
```
usage: main.py [-h] [--batchSize BATCHSIZE] [--nEpochs NEPOCHS] [--lr LR]
               [--step STEP] [--cuda] [--resume RESUME]
               [--start-epoch START_EPOCH] [--threads THREADS]
               [--pretrained PRETRAINED]

Pytorch SRDenseNet

optional arguments:
  -h, --help            show this help message and exit
  --batchSize BATCHSIZE
                        training batch size
  --nEpochs NEPOCHS     number of epochs to train for
  --lr LR               Learning Rate. Default=1e-4
  --step STEP           Sets the learning rate to the initial LR decayed by
                        momentum every n epochs, Default: n=10
  --cuda                Use cuda?
  --resume RESUME       Path to checkpoint (default: none)
  --start-epoch START_EPOCH
                        Manual epoch number (useful on restarts)
  --threads THREADS     Number of threads for data loader to use, Default: 1
  --pretrained PRETRAINED
                        path to pretrained model (default: none)

```
### Test
```
usage: test.py [-h] [--cuda] [--model MODEL] [--imageset IMAGESET] [--scale SCALE]

Pytorch SRDenseNet Test

optional arguments:
  -h, --help     show this help message and exit
  --cuda         use cuda?
  --model MODEL  model path
  --imageset IMAGESET  imageset name
  --scale SCALE  scale factor, Default: 4
```

### Prepare Training dataset
 The training data is generated with Matlab Bicubic Interplotation, please refer [Code for Data Generation](https://github.com/twtygqyy/pytorch-LapSRN/tree/master/data) for creating training files.

