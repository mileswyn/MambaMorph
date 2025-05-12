# Mamba-based deformable medical image registration with an annotated brain MR-CT dataset

## Abstract
Deformable registration is essential in medical image analysis, especially for handling various multi- and mono-modal registration tasks in neuroimaging. Existing studies lack exploration of brain MR-CT registration, and face challenges in both accuracy and efficiency improvements of learning-based methods. To enlarge the practice of multi-modal registration in brain, we present SR-Reg, a new benchmark dataset comprising 180 volumetric paired MR-CT images and annotated anatomical regions. Building on this foundation, we introduce MambaMorph, a novel deformable registration network based on an efficient state space model Mamba for global feature learning, with a fine-grained feature extractor for low-level embedding. Experimental results demonstrate that MambaMorph surpasses advanced ConvNet-based and Transformer-based networks across several multi- and mono-modal tasks, showcasing impressive enhancements of efficacy and efficiency.

# Tutorial
Install Mamba via https://github.com/state-spaces/mamba

### Framework
![MambaMorph-nocl-v2-github](https://github.com/Guo-Stone/MambaMorph/assets/77957555/8c14c6a4-012c-4153-8442-a1ad5555367f)

### Result
![Result](https://github.com/Guo-Stone/MambaMorph/assets/77957555/6318dfcb-0325-4d49-b8b2-4bd78823a303)

### **Train**

```
python ./scripts/torch/train_cross.py --gpu 1 --epochs 1 --batch-size 1 --model-dir output/train_debug --model mm-feat
```

### **Test**

```
python ./scripts/torch/test_cross.py --gpu 0 --model mm-feat --load-model "/home/guotao/code/voxelmorph-dev/output/train_s46/min_train.pt"
```

# Data
We implement MambaMorph on our brain MR-CT data SR-Reg which is developed from SynthRAD 2023 (https://synthrad2023.grand-challenge.org/). Please go [Here](https://github.com/mileswyn/MambaMorph) to access the SR-Reg dataset.

### Dataset Link
#### Baidu Cloud Drive
```
https://pan.baidu.com/s/1TlxqZHl6T17on_f3BDixmA (Extract code：hwwd)
```
#### Google Cloud Drive
```
https://drive.google.com/file/d/1idT6rCKXry-Yc8GF-DBxEn6e32-pBiFF/view?usp=sharing
```

### Data sample
![data-sample](https://github.com/Guo-Stone/MambaMorph/assets/77957555/f715aa06-0cf7-41b6-915c-e3ee98756f75)

# Citation

@article{2025mambamorph,  

  title={MambaMorph: a Mamba-based Framework for Medical MR-CT Deformable Registration},  

  author={Yinuo Wang, Tao Guo, Weimin Yuan, Shihao Shu, Cai Meng, Xiangzhi Bai,},  

  journal={Computerized Medical Imaging and Graphics},  

  year={2025}  

}
