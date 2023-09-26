# 💾Tree-structured Implicit Neural Compression (TINC)
Our paper was accepted to CVPR2023. You can also find our full-version paper [on arXiv](https://arxiv.org/abs/2211.06689)
<img src="docs/assets_readme/TINC_method.jpg" width="80%"/>

<img src="docs/assets_readme/TINC_compare_roi.jpg" width="50%"/>

# 🚀Quickstart

### 1. Setup a conda environment and install the pytorch

    conda create -n TINC python=3.9
    conda activate TINC
    conda install pytorch torchvision torchaudio cudatoolkit=11.1 -c pytorch -c nvidia

### 2. Installing python libraries

    pip install -r requirements.txt
### 3. Compression
(1) Single compression task

relevant compression parameters can be modified in **opt/SingleTask/default.yaml**.

    python main.py -p opt/SingleTask/default.yaml -g 0 

final compressed file path: **outputs/default_{time}/compressed/**

final decompressed file path: **outputs/default_{time}/decompressed.tif**

training result: 

    tensorboard --logdir=outputs/default_{time}

(2) Run multiple tasks at once

relevant compression parameters can be modified in **opt/MultiTask/default.yaml**.

    python MultiTask.py -p opt/MultiTask/default.yaml -g 0,1,2,3 -stp main.py -debug
# 😘Citations
	@misc{yang2022tinc,
      title={TINC: Tree-structured Implicit Neural Compression}, 
      author={Runzhao Yang and Tingxiong Xiao and Yuxiao Cheng and Jinli Suo and Qionghai Dai}, 
      year={2022},
      eprint={2211.06689},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
# 💡Contact
If you need any help or are looking for cooperation feel free to contact us.
yangrz20@mails.tsinghua.edu.cn
