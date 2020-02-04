## 3D Hand Shape and Pose Estimation from a Single RGB Image
![prediction example](teaser.png)

### Introduction
This work is based on [this CVPR 2019 paper](https://docs.google.com/viewer?a=v&pid=sites&srcid=ZGVmYXVsdGRvbWFpbnxnZWxpdWhhb250dXxneDo3ZjE0ZjY3OWUzYjJkYjA2). 
Here is the [original repository](https://github.com/geliuhao/3DHandShapePosefromRGB).

### Installation
1. Install pytorch == v1.4.0 (not >=0.4.0 as the original repo says) following [official instruction](https://pytorch.org/).
2. Clone this repo, and we'll call the directory that you cloned as ${HAND_ROOT}.
3. Install dependencies:
    ```
    pip install -r requirements.txt
    ```

### Pre-trained models
~~Download pre-trained models from [online drive](https://mega.nz/#!yfZXBayC!izaLXi4X8LsgPuRWqKlUrCKBWNLVKTvfgAuFIS7SSFY), and unzip the file to ${HAND_ROOT}/model.~~

### Running the code
1. Evaluate on our real-world dataset and visualize the results of hand mesh and pose.
    ```
    python eval_script.py --config-file "configs/eval_real_world_testset.yaml"
    ```
   The visualization results will be saved to ${HAND_ROOT}/output/configs/eval_real_world_testset.yaml/

2. Evaluate on STB dataset.

    Download [STB dataset](https://www.dropbox.com/sh/ve1yoar9fwrusz0/AAAfu7Fo4NqUB7Dn9AiN8pCca?dl=0) to ${HAND_ROOT}/data/STB.
    
    Run the following script:
    ```
    python eval_script.py --config-file "configs/eval_STB_dataset.yaml"
    ```
   The pose estimation results will be saved to ${HAND_ROOT}/output/configs/eval_STB_dataset.yaml/pose_estimations.mat
