# Deep Learning methodologies for action segmentation applied to manufacturing scenarios

This repository provides I3D and Skeletal features extracted from the HA4M dataset ([available here](https://baltig.cnr.it/ISP/ha4m)), for the analysis performed in the paper Deep Learning methodologies for action segmentation applied to manufacturing scenarios.

## I3D and Skeletal Features

All the features, the ground truth, and the test-train splits considered are available [at this link](https://cloud.cnr.it/owncloud/index.php/s/ZBrMapYdFkL6xy2).

Each folder contains a specific set of features for each video, namely RGB, RGBA, Depth, UpSkel, and ArmSkel. The repository includes also the Ground Truth folder.

The directory tree is as follows:

```
RGB:
    IDU001V001.npy
    IDU001V002.npy
    ...

RGBA:
    IDU001V001.npy
    IDU001V002.npy
    ...

Depth:
    IDU001V001.npy
    IDU001V002.npy
    ...

UpSkel:
    IDU001V001.npy
    IDU001V002.npy
    ...

ArmSkel:
    IDU001V001.npy
    IDU001V002.npy
    ...

GroundTruth:
    IDU001V001.txt
    IDU001V002.txt
    ...
```

RGB, RGBA and Depth sets of features have been extracted using the I3D model, resulting in 1024 features per frame for each video.

UpSkel and ArmSkel sets of features have been extracted from the videos using the Azure Kinect Body Tracking DK, resulting in 23 and 14 skeletal 3D coordinates.

## Dataset Splittings

The files "test.splitN.bundle" and "train.splitN.bundle" contain the test-train splitting protocol of the 205 videos within the HA4M dataset, where N=1 stands for Cross-Subject splitting, while N=2 and N=3 stand for Cross-Location splittings, namely C-Loc12 and C-Loc21. "test.split1_newData.bundle" contains the test set of the new data collection. For further analysis, we also provide a Cross-Subject splitting for all the 217 videos of the HA4M dataset, at N=4.

## Contacts:

Laura Romeo: laura.romeo@stiima.cnr.it

Roberto Marani: roberto.marani@stiima.cnr.it

## Cite:

If you want to use this repository, please remember to cite the paper where the HA4M dataset is presented:

```
@article{Cicirelli2022,
  title={The HA4M dataset: Multi-Modal Monitoring of an assembly task for Human Action recognition in Manufacturing},
  author={Cicirelli, Grazia and Marani, Roberto and Romeo, Laura and Dom{\'\i}nguez, Manuel Garc{\'\i}a and Heras, J{\'o}nathan and Perri, Anna G and D’Orazio, Tiziana},
  journal={Scientific Data},
  volume={9},
  number={1},
  pages={1--12},
  year={2022},
  publisher={Nature Publishing Group}
}
```
