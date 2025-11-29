# CogGIL: A Cognitive Generation-Indexing-Learning Framework for Remote Sensing Building Extraction

This repository contains the official implementation of the paper:  
> **Abstract:** Building extraction is a fundamental task in remote sensing but faces challenges like semantic confusion, adjacency misjudgment, and geometric fragmentation. Existing methods often rely on shallow representations. We propose **CogGIL**, a brain-inspired "Generation-Indexing-Learning" framework. It emulates human cognitive processes (Imagination, Association, Integration) to address these challenges. 
> 1. **Generation:** A layout-guided diffusion model enriches data diversity.
> 2. **Indexing:** A hard negative sample indexing mechanism mines confusing non-building samples.
> 3. **Learning:** A fine-grained learning network fuses geometric, adjacency, and semantic attributes.

---

## 📢 News
* **[Update]** The code will be made publicly available **upon acceptance**.


---

## 🛠️ Environment and Installation
## Pretrained Backbones & Datasets:
We have provided the pretrained backbones(ResNet-50, Res2Net-50, PVT-v2-b2) and the processed datasets(WHU Building Dataset, Mass Building Dataset, Inria Building Dataset)

You can download the pretrained backbones via Baidu Disk [Link](https://pan.baidu.com/s/16sA3ZejzcItAWa2JE1G6vg?pwd=abmg) Code:abmg 

You can download the three building datasets via Baidu Disk [Link](https://pan.baidu.com/s/1sAE_NUf1NqnMQllAVJpM3g?pwd=UANe) Code: UANe

For the environment setup and dependencies, please refer to the configuration used in **UANet**:
👉 **[https://github.com/Henryjiepanli/Uncertainty-aware-Network](https://github.com/Henryjiepanli/Uncertainty-aware-Network)**

## Training Instructions

To train the UANet model, follow these steps:

1. Set the CUDA visible devices to specify the GPU for training. For example, to use GPU 0, run the following command:
   ```bash
   CUDA_VISIBLE_DEVICES=0 python Code/train.py -c config/whubuilding/CogGIL.py
2. Set the CUDA visible devices to specify the GPU for test. For example, to use GPU 0, run the following command:
   ```bash
   CUDA_VISIBLE_DEVICES=0 python Code/test.py -c config/whubuilding/CogGIL.py -o test_results/whubuilding/CogGIL/ --rgb

## Training Instructions for Multiple Training Sessions

If you want to continue training the model from a checkpoint or perform multiple training sessions, follow this:

1. Adjust the *pretrained_ckpt_path* in the config file.


## 📢 Acknowledgements

We would like to express our sincere gratitude to the authors and developers of [BuildFormer](https://github.com/WangLibo1995/BuildFormer)、[UANet](https://github.com/Henryjiepanli/Uncertainty-aware-Network).  Here, we sincerely express our gratitude to the authors of that paper.



