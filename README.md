# SHM-Tools: Structural Health Monitoring Toolkit

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Status](https://img.shields.io/badge/status-Active-green)

**SHM-Tools** 是一个轻量级、模块化的结构健康监测（Structural Health Monitoring）数据分析与仿真工具包。

本项目旨在为土木工程领域的研究人员和工程师提供一套标准化的算法库，涵盖从传感器原始数据处理到结构状态评估的全流程。

[English Version](./README_EN.md) 

---

## 📚 主要功能 (Features)

### 1. 信号预处理 (Signal Preprocessing)
- **去噪与滤波**: 低通、高通、带通滤波 (Butterworth, Chebyshev)。
- **趋势项消除**: 线性去趋势 (Detrending)、多项式拟合去除。
- **异常值清洗**: 基于统计学 (3$\sigma$准则) 的坏点剔除。

### 2. 结构动力学仿真 (Structural Dynamics)
- **数值积分方法**: 
  - Newmark-\beta 法
  - Wilson-\theta 法
  - Central Difference Method (中心差分法)
- **多自由度体系响应计算**: 支持自定义质量、刚度、阻尼矩阵 ($M, K, C$) 进行时程分析。

### 3. 模态参数识别 (Modal Analysis)
- **频域方法**: 
  - 峰值拾取法 (Peak Picking, PP)
  - 频域分解法 (Frequency Domain Decomposition, FDD)
- **时域方法**: 
  - 随机子空间法 (Stochastic Subspace Identification, SSI-COV/DATA)
  - 特征系统实现算法 (ERA)

### 4. 损伤识别 (Damage Detection)
- 基于模态参数变化的损伤指标计算。
- 基于模型修正 (Model Updating) 的刚度矩阵反演（基础框架）。

---

## 🚀 快速开始 (Quick Start)

### 安装 (Installation)

```bash
# 克隆仓库
git clone [https://github.com/3104792380/SHM-Tools.git](https://github.com/3104792380/SHM-Tools.git)

# 进入目录
cd SHM-Tools

# 安装依赖
pip install -r requirements.txt
