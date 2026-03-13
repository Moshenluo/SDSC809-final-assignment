# SDSC8009 Final Assignment - Climate Forecasting with CatBoost

## 📖 项目简介

**SDSC8009 课程最终作业**

本项目使用机器学习方法（主要是 CatBoost 梯度提升算法）对气候韧性相关数据进行预测建模。通过 Optuna 进行超参数优化，实现了准确的气候数据预测。

| 项目 | 信息 |
|------|------|
| **课程** | SDSC8009 |
| **主要方法** | CatBoost, Optuna 超参数优化 |

---

## 📁 项目结构

```
assignment-final/
├── development.ipynb          # 开发 Notebook（探索性分析）
├── final_model.ipynb          # 最终模型 Notebook
├── final-assignment.pdf       # 作业报告 PDF
├── data/
│   ├── df-train.csv           # 训练数据集
│   └── df-forecast.csv        # 预测数据集
├── catboost_info/             # CatBoost 训练日志（已忽略）
└── optuna_results/
    ├── best_params.json       # Optuna 最优参数
    ├── final_model_params.json # 最终模型参数
    └── catboost_hyperopt.db   # 超参数优化数据库（已忽略）
```

---

## 🚀 快速开始

### 环境要求

- Python 3.8+
- Jupyter Notebook
- CatBoost
- Optuna
- Pandas, NumPy, Scikit-learn

### 安装依赖

```bash
pip install jupyter
pip install catboost
pip install optuna
pip install pandas numpy scikit-learn matplotlib seaborn
```

### 运行 Notebook

1. **探索性分析与开发**：
   ```bash
   jupyter notebook development.ipynb
   ```

2. **最终模型训练与预测**：
   ```bash
   jupyter notebook final_model.ipynb
   ```

---

## 📊 数据集

### 训练数据 (`data/df-train.csv`)
用于模型训练的历史气候数据。

### 预测数据 (`data/df-forecast.csv`)
需要进行预测的气候数据。

---

## 🔧 模型与方法

### CatBoost

CatBoost 是一个基于梯度提升决策树（GBDT）的机器学习算法，具有以下优势：
- 自动处理类别特征
- 防止过拟合
- 高精度预测

### Optuna 超参数优化

使用 Optuna 自动搜索 CatBoost 的最优超参数组合，包括：
- learning_rate
- depth
- n_estimators
- l2_leaf_reg
- 等

---

## 📈 实验结果

### 最优参数（`optuna_results/best_params.json`）

Optuna 搜索得到的最优超参数已保存在 `best_params.json` 中。

### 训练日志

- 训练误差和测试误差记录在 `catboost_info/` 目录
- 可通过 CatBoost 可视化工具查看训练过程

---

## 📝 使用说明

### 1. 准备数据

确保数据文件位于 `data/` 目录下：
- `df-train.csv`
- `df-forecast.csv`

### 2. 运行模型训练

打开 `final_model.ipynb`，依次执行单元格：
1. 导入依赖库
2. 加载数据
3. 数据预处理
4. 加载最优参数
5. 训练 CatBoost 模型
6. 进行预测
7. 保存结果

### 3. 查看结果

预测结果将保存在 Notebook 输出中，或根据代码保存到指定文件。

---

## 📄 文件说明

| 文件 | 说明 |
|------|------|
| `development.ipynb` | 开发阶段的探索性分析 Notebook |
| `final_model.ipynb` | 最终模型训练与预测 Notebook |
| `final-assignment.pdf` | 作业报告 PDF 文档 |
| `data/df-train.csv` | 训练数据集 |
| `data/df-forecast.csv` | 预测数据集 |
| `optuna_results/best_params.json` | Optuna 最优超参数 |
| `optuna_results/final_model_params.json` | 最终模型参数配置 |

---

## 📧 联系方式

- **作者**: 唐翊杰
- **Email**: 1411795718@qq.com
- **GitHub**: [@Moshenluo](https://github.com/Moshenluo)

---

**最后更新**: 2026-03-13
