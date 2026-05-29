# A/B Test 分析作品集

从统计原理到真实业务场景的三层递进实践，覆盖模拟实验、真实数据集分析与完整实验设计报告。

---

## 项目结构

```text
abtest-portfolio/
├── 01_simulation/          第一层：numpy 模拟实验
├── 02_kaggle_marketing/    第二层：Kaggle 真实数据分析
├── 03_udacity_report/      第三层：完整实验设计报告
└── README.md
```

---

## 三层递进

### 第一层：统计原理可视化（`01_simulation/`）

用 numpy 模拟二项分布，直观验证 A/B Test 的核心统计规律。

- 固定效应大小（p_A=0.10 vs p_B），改变样本量，观察 p-value 变化
- 固定样本量，改变效应大小，观察检出率
- 核心结论：**样本越大越能检出小差异；效应越小所需样本量越大**

### 第二层：真实数据集分析（`02_kaggle_marketing/`）

基于 [Kaggle Marketing A/B Testing 数据集](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)，分析广告投放策略的转化率差异。

- 实验组（ad）vs 对照组（psa）转化率对比
- 双比例 Z 检验 + 95% 置信区间
- 业务结论与上线建议

### 第三层：完整实验设计报告（`03_udacity_report/`）

参照 Udacity A/B Testing 课程项目，输出一份完整的实验设计与分析报告。

- 实验设计：指标选择、流量分配、样本量估算
- Sanity Check：不变指标验证实验执行是否正确
- 统计显著性 + 业务显著性双重判断
- 上线建议

---

## 评估指标体系

| 层次 | 数据 | 检验方法 | 核心产出 |
|---|---|---|---|
| 模拟实验 | numpy 生成 | 双比例 Z 检验 | 功效曲线、样本量与 p-value 关系图 |
| Kaggle | 真实广告数据 | Z 检验 + 置信区间 | 转化率 lift、业务结论 |
| Udacity | 课程项目数据 | 多指标联合判断 | 完整实验报告 |
