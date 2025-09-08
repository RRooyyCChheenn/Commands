# 基于 Tianmouc 的智能算法实现

> 本项目基于天眸芯的双通路数据，开发了光流估计与双通路融合推理算法，旨在充分发挥硬件潜力，支持开放世界的动态场景理解。

---

## 1. 项目简介

本项目通过对 **Tianmouc 硬件** 输出的 AOP / COP 通路数据进行处理，实现了以下两个核心算法：

* **光流估计**：利用 AOP 通路实现快速光流估计
* **双通路融合推理**：基于 AOP + COP 双路融合数据实现视频级别的推理任务

项目内包含：

* 可运行的程序
* 实拍数据
* 可视化结果
* 运行手册

**项目目标**：在天眸芯硬件上部署智能算法，支持开放世界的光流估计与视频推理。

---

## 2. 功能特性

* ✅ 基于 AOP 的光流估计
* ✅ 基于 AOP + COP 的双路融合视频推理

---

## 3. 目录结构

项目的主要目录结构如下：

```bash
TMC_algorithms/
├── datareader/          # 数据读取与预处理
│   ├── lib
│   ├── scripts
│   └── tools/rod_decode_pybind
├── tianmoucv/           # Tianmouc Python 封装库
├── TMC_fusion/          # 双通路融合推理算法
│   ├── data/            # 实验数据
│   ├── demo/            # 融合推理 Demo
│   ├── KalmanTrackor/   
│   ├── YOLOPv1/         # 基于 YOLOPv1 的检测模块
│   └── YOLOv5/          # 基于 YOLOv5 的检测模块
└── TMC_optical_flow/    # 光流估计算法
    ├── data/            # 实验数据
    └── demo/            # 光流估计 Demo
```

---

## 4. 环境依赖

### 光流估计

```bash
conda create -n [YOUR FLOW ENV] --python=3.10
conda activate [YOUR FLOW ENV]
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia

pip install tianmoucv
pip install jupyter notebook
```

### 双通路融合视频推理

```bash
cd ./TMC_algorithms/TMC_fusion
conda create -n [YOUR FUSION ENV] --python=3.10
sh install.sh
```

---

## 5. 运行指南

### 光流估计

```bash
cd ./TMC_algorithms
conda activate [YOUR FLOW ENV]
jupyter notebook
```

运行 `opticalflow_spynet.ipynb` 以复现光流估计结果。

### 双通路融合视频推理

```bash
cd ./TMC_algorithms
conda activate [YOUR FUSION ENV]
jupyter notebook
```

运行 `Evaluation_complex.ipynb` 以复现视频推理结果。
