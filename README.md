# Analysis-of-Model-Pruning-in-Animals-10-Classification

---

## English Documentation

###  Project Overview
This repository presents a comprehensive analysis of model pruning techniques applied to animal image classification using the Animals-10 dataset. We implement and compare two fundamental pruning approaches:

**Key Components:**
- **Weight Pruning**: Achieved 98.94% model compression (52.46MB → 0.56MB) while maintaining 79.18% accuracy
- **Filter Pruning**: Improved accuracy by 5.74% (77.46% → 83.20%) with 30.76% parameter reduction
- **Hybrid Approach**: Combined pruning strategies for different deployment scenarios

###  Technical Specifications
| Component               | Implementation Details                 |
|-------------------------|----------------------------------------|
| Base Architecture       | Custom CNN (5 Conv + 3 Dense layers)   |
| Pruning Tools           | TensorFlow Model Optimization Toolkit  |
| Training Configuration  | AdamW optimizer (lr=3e-4), 100 epochs  |
| Sparsity Patterns       | Polynomial decay (30%-90% sparsity)    |

### Model Comparison
| Model                   | Accuracy | Size  | Compression |
|-------------------------|----------|-------|-------------|
| Transfer Learning       | 96.98%   | 226MB | -           |
| Weight Pruned Custom CNN| 79.18%   | 0.56MB| 98.94%      |
| Filter Pruned Custom CNN| 83.20%   | 39.8MB| 30.76%      |

###  Key Findings
1. **Accuracy-Sparsity Tradeoff**: Filter pruning at 30% sparsity yields optimal accuracy gain (+5.74%)
2. **Memory Efficiency**: Weight pruning reduces model size by 98.94% with <1% accuracy drop
3. **Hardware Impact**: Pruned models show 2.1-3.7x speedup on edge devices (Raspberry Pi 4)

---

## 中文文档

### 项目概述
本仓库系统分析了模型剪枝技术在Animals-10动物图像分类任务中的应用效果，包含两种核心剪枝方法的对比：

**核心成就：**
- **权重剪枝**：实现98.94%模型压缩(52.46MB → 0.56MB)，精度保持79.18%
- **过滤器剪枝**：准确率提升5.74%(77.46% → 83.20%)，参数量减少30.76%
- **混合策略**：针对不同部署场景的组合剪枝方案

###  技术细节
| 组件                | 实现细节                               |
|---------------------|---------------------------------------|
| 基础架构            | 自定义CNN(5卷积层+3全连接层)          |
| 剪枝工具            | TensorFlow模型优化工具包              |
| 训练配置            | AdamW优化器(学习率3e-4)，100训练周期  |
| 稀疏模式            | 多项式衰减(30%-90%稀疏度)             |

###  性能指标
| 模型                  | 准确率   | 大小   | 压缩率     |
|-----------------------|---------|--------|-----------|
| 迁移学习模型          | 96.98%  | 226MB  | -         |
| 权重剪枝CNN           | 79.18%  | 0.56MB | 98.94%    |
| 过滤器剪枝CNN         | 83.20%  | 39.8MB | 30.76%    |

###  核心发现
1. **精度-稀疏度权衡**：30%稀疏度的过滤器剪枝带来最佳精度提升(+5.74%)
2. **内存效率**：权重剪枝在精度损失<1%前提下实现98.94%模型压缩
3. **硬件影响**：剪枝模型在边缘设备(Raspberry Pi 4)上实现2.1-3.7倍加速

---


##  References
- Dataset: [Animals-10 on Kaggle](https://www.kaggle.com/datasets/alessiocorrado99/animals10)
- Pruning Implementation: [Keras Pruning API](https://www.tensorflow.org/model_optimization)
- Base Model: [EfficientNet B7](https://keras.io/api/applications/efficientnet/)
