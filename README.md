# MambaMorph: a Mamba-based Framework for Medical MR-CT Deformable Registration

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
We implement MambaMorph on our brain MR-CT data SR-Reg which is developed from SynthRAD 2023 (https://synthrad2023.grand-challenge.org/). The SR-Reg dataset is undergoing careful processing and will be published with the next version of MambaMorph.

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


# Paper
https://arxiv.org/abs/2401.13934

# Citation

@article{guo2024mambamorph,  

  title={MambaMorph: a Mamba-based Framework for Medical MR-CT Deformable Registration},  

  author={Guo, Tao and Wang, Yinuo and Shu, Shihao and Chen, Diansheng and Tang, Zhouping and Meng, Cai and Bai, Xiangzhi},  

  journal={arXiv preprint arXiv:2401.13934},  

  year={2024}  

}
