# 第二层：Kaggle Marketing A/B Testing 分析

基于真实广告投放数据，分析"看广告"vs"看公益广告"对转化率的影响。

## 数据集

[Kaggle - Marketing A/B Testing](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)

- 实验组（ad）：看到真实广告
- 对照组（psa）：看到公益广告（PSA）
- 目标指标：是否转化（converted: 0/1）

## 分析流程

1. 数据探索：样本量、转化率分布、是否存在 SRM
2. 假设检验：双比例 Z 检验，H₀: p_ad = p_psa
3. 置信区间：95% CI for (p_ad - p_psa)
4. 业务结论：lift 是否达到上线门槛，给出建议

## 文件

- `analysis.ipynb`：完整分析 notebook
- `data/`：原始数据（.gitignore 排除大文件）
