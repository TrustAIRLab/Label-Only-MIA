# Label-Only Membership Inference Attack

[![arXiv](https://img.shields.io/badge/arxiv-2007.15528-b31b1b)](https://arxiv.org/abs/2007.15528)
<a href="https://pytorch.org/get-started/locally/"><img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-ee4c2c?logo=pytorch&logoColor=white"></a>

This is the code for our ACM CCS 21 paper [Membership Leakage in Label-Only Exposures](https://dl.acm.org/doi/abs/10.1145/3460120.3484575).
We propose the first label-only membership inference attack that solely relies on the final prediction of the target model, i.e., the predicted label, as their attack model’s input.

## Prepare
Users should install Python3 and PyTorch at first. We recommend using conda to install it based on the official documents.

Specifically, please follow the requirements below:
```
numpy<1.24.0
foolbox==3.0.0
adversarial-robustness-toolbox==1.5.0
scipy==1.7.0
```
For others, please install the latest version.

## Run
Check ```argparse.ArgumentParser``` for dataset, model, etc.

Set ```args.action``` to run the following attacks.
### Label-Only MIA Based on Shadow Model (Transfer Attack)
```action=1``` Train_Target_Model(args)

```action=2``` Train_Shadow_Model(args)

```action=3``` AdversaryOne(args)

### Label-Only MIA Based on Decision Boundary (Boundary Attack)
```action=1``` Train_Target_Model(args)

```action=4``` AdversaryTwo(args)

### Calculate the Radius to the Decision Boundary.

## Citation
```bibtex
@inproceedings{LZ21,
author = {Zheng Li and Yang Zhang},
title = {{Membership Leakage in Label-Only Exposures}},
booktitle = {{ACM SIGSAC Conference on Computer and Communications Security (CCS)}},
publisher = {ACM},
year = {2021}
}
```

## License

Label-Only MIA is freely available for free non-commercial use, and may be redistributed under these conditions. For commercial queries, please drop an e-mail at zhang[AT]cispa.de. We will send the detail agreement to you.

