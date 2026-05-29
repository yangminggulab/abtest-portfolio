# 第三层：完整实验设计报告（Udacity A/B Testing）

参照 Udacity A/B Testing 课程项目，输出一份工业级实验设计与分析报告。

## 实验背景

Udacity 课程改版实验：将"Start Free Trial"按钮改为弹出时间询问，
目标是过滤掉没有足够时间的学员，提升付费转化质量，同时不显著降低整体注册量。

## 报告结构

### 1. 实验设计
- 选择评估指标（Evaluation Metrics）与不变指标（Invariant Metrics）
- 样本量估算（基于 MDE、显著性水平、检验功效）
- 实验时长与流量分配

### 2. Sanity Check
- 验证不变指标（点击率、Cookie 数）在实验/对照组间无显著差异
- 确认实验执行正确，排除 SRM（Sample Ratio Mismatch）

### 3. 效果分析
- 统计显著性：各评估指标的 p-value 与置信区间
- 业务显著性：lift 是否达到预设最小可检测效应（MDE）

### 4. 上线建议
- 综合统计结论与业务判断，给出明确的上线 / 不上线 / 继续观察建议

## 文件

- `report.ipynb`：完整分析 notebook
- `report.md`：导出的可读报告
- `data/`：课程提供的实验数据
