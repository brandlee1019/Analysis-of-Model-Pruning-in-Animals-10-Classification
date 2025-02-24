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

## Key Insights
1. **Pruning Paradox**: Moderate sparsity (30-70%) often improves model performance
2. **Storage Optimization**: Weight pruning + gzip achieves extreme compression
3. **Architecture Matters**: Filter pruning works better with shallow networks

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

## 主要结论
1. **剪枝悖论**：适度稀疏度(30-70%)常提升模型表现  
2. **存储优化**：权重剪枝+gzip实现极致压缩  
3. **架构差异**：过滤器剪枝更适用于浅层网络  

---


##  References
- Dataset: [Animals-10 on Kaggle](https://www.kaggle.com/datasets/alessiocorrado99/animals10)
- Pruning Implementation: [Keras Pruning API](https://www.tensorflow.org/model_optimization)
- Base Model: [EfficientNet B7](https://keras.io/api/applications/efficientnet/)
