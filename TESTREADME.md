# 基于Tianmouc实现的智能算法
> 基于Tianmouc实现的光流估计
> 基于Tianmouc实现的双通路融合推理

---

## 1. 项目简介
本项目通过利用天眸芯的双通路数据，开发了适配的智能算法，释放硬件潜力，这是实现的两个智能算法，分别是光流估计，以及双通路融合视频推理，本文件里，包含了可运行程序，可视化结果，以及运行手册
 
- **项目目标**：为天眸芯硬件搭载智能算法，从而实现开放世界的光流估计以及视频推理

---

## 2. 功能特性
- ✅ AOP通路实现光流估计 
- ✅ AOP+COP双路融合实现视频推理


---

## 3. 环境依赖

### 光流估计
```bash
conda create -n [YOUR ENV NAME] --python=3.10
conda activate [YOUR ENV NAME]
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia

pip install tianmoucv

pip install jupyter notebook

```
### 双通路融合视频推理
```bash
cd /TMC_algorithms/TMC_fusion
conda create -n [YOUR ENV NAME] --python=3.10
sh install.sh

```

## 4. 运行指南
