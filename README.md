# Analysis-of-Model-Pruning-in-Animals-10-Classification
[中文](#中文) | [English](#english)

<a id="english"></a>
## 🌟 Project Overview
This project explores the benefits of model pruning techniques (weight pruning and filter pruning) on CNN architectures for animal image classification using the Animals-10 dataset. We compare performance and efficiency between:
- Custom CNN model
- Transfer learning model (EfficientNet B7)
- Their pruned variants

Key Findings:
- Achieved **98.94% size reduction** with weight pruning on custom CNN
- Filter pruning boosted custom CNN accuracy by **6.86%** at 30% sparsity
- Transfer learning model maintained **95% accuracy** with 0.46% size reduction

<a id="中文"></a>
## 🌟 项目概述
本项目使用Animals-10数据集，探索模型剪枝技术(权重剪枝和过滤器剪枝)在CNN架构中的效果。我们比较了：
- 自定义CNN模型
- 迁移学习模型(EfficientNet B7)
- 剪枝后变体

核心发现：
- 自定义CNN权重剪枝实现**98.94%模型压缩**
- 过滤器剪枝在30%稀疏度下提升准确率**6.86%**
- 迁移学习模型保持**95%准确率**同时减小0.46%体积

## 🚀 Key Features
**Bilingual Support** | **双语言支持**  
📊 Comparative analysis of pruning techniques  
🦾 Resource-efficient model deployment solutions  
📈 Detailed metrics visualization

## 🛠️ Methodology
### Technical Framework
| Component        | Specifications                          |
|------------------|-----------------------------------------|
| Base Models      | Custom CNN, EfficientNet B7            |
| Pruning Methods  | Weight Pruning, Filter Pruning         |
| Sparsity Levels  | 30%, 50%, 70%, 90%                     |
| Training Epochs  | 30-100 (with early stopping)           |

### 技术框架
| 组件            | 规格参数                               |
|-----------------|---------------------------------------|
| 基础模型        | 自定义CNN, EfficientNet B7           |
| 剪枝方法        | 权重剪枝, 过滤器剪枝                  |
| 稀疏度          | 30%, 50%, 70%, 90%                   |
| 训练周期        | 30-100 (含早停机制)                  |

## 📊 Results Highlights
### Model Comparison
| Model                   | Accuracy | Size  | Compression |
|-------------------------|----------|-------|-------------|
| Transfer Learning       | 96.98%   | 226MB | -           |
| Weight Pruned Custom CNN| 79.18%   | 0.56MB| 98.94%      |
| Filter Pruned Custom CNN| 83.20%   | 39.8MB| 30.76%      |

### 核心结果
| 模型                  | 准确率   | 大小   | 压缩率     |
|-----------------------|---------|--------|-----------|
| 迁移学习模型          | 96.98%  | 226MB  | -         |
| 权重剪枝CNN           | 79.18%  | 0.56MB | 98.94%    |
| 过滤器剪枝CNN         | 83.20%  | 39.8MB | 30.76%    |

## 🧠 Key Insights
1. **Pruning Paradox**: Moderate sparsity (30-70%) often improves model performance
2. **Storage Optimization**: Weight pruning + gzip achieves extreme compression
3. **Architecture Matters**: Filter pruning works better with shallow networks

## 核心洞见
1. **剪枝悖论**：适度稀疏度(30-70%)常提升模型表现  
2. **存储优化**：权重剪枝+gzip实现极致压缩  
3. **架构差异**：过滤器剪枝更适用于浅层网络  

## 📚 References
- Dataset: [Animals-10 on Kaggle](https://www.kaggle.com/datasets/alessiocorrado99/animals10)
- Pruning Implementation: [Keras Pruning API](https://www.tensorflow.org/model_optimization)
- Base Model: [EfficientNet B7](https://keras.io/api/applications/efficientnet/)

## 📜 License
MIT License - See [LICENSE](LICENSE) for details
