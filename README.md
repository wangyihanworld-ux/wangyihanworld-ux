# 王怡涵

我关注的不只是算出数字，而是把经营问题拆成可解释、可复核、可交付的分析模型：明确业务口径，建立勾稽关系，用情景分析呈现风险，并把结果整理成管理层可以直接阅读的 Excel 报告。

[完整项目作品集](PORTFOLIO.md) · [正式版本](#正式版本) · [联系邮箱](mailto:1230005615@student.must.edu.mo)

## 能力概览

- 财务分析：预算差异、滚动预测、贡献利润、营运资金、现金流与仓储成本。
- 数据建模：Python、pandas、NumPy、Excel、Power BI、多元回归与情景分析。
- 模型治理：输入校验、数量守恒、财务勾稽、样本外回测、基准模型和边界披露。
- 自动化交付：合成数据、一键 Demo、Excel 管理报告、GUI、自动化测试与 GitHub Actions。

## 精选项目

### 仓储成本与经营分析模型

[代码](https://github.com/wangyihanworld-ux/Warehouse-analysis-model) · [v1.5.6](https://github.com/wangyihanworld-ux/Warehouse-analysis-model/releases/tag/v1.5.6)

用 FIFO 重建批次流转，计算仓储费、库龄和期末库存。库存不足时整笔拒绝，避免将未分摊数量误认为实际出库。67 项测试通过；合成演示仓储费 20,101.90 元，期末库存 375 吨，数量守恒异常 0。

![仓储分析报告](https://raw.githubusercontent.com/wangyihanworld-ux/Warehouse-analysis-model/main/docs/images/management-summary.png)

### 预算差异与滚动预测模型

[代码](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model) · [v0.1.0](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model/releases/tag/v0.1.0)

把利润差异拆成销量、价格、结构、单位成本和固定费用影响，并用实际月份与未来情景构建全年预测。22 项测试通过；收入有利差异 17,584 元，经营利润不利差异 10,724.36 元。

![预算差异管理摘要](https://raw.githubusercontent.com/wangyihanworld-ux/Budget-variance-forecast-model/main/docs/images/management-summary.png)

### 客户与产品盈利能力分析模型

[代码](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model) · [v0.1.0](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model/releases/tag/v0.1.0)

从标价收入追溯到净收入、毛利和贡献利润，识别高收入低利润客户与集中度风险。15 项测试通过；客户甲收入第一但贡献利润率仅 11.24%，整体为 29.50%。

### 宏观经济情景与经营预测模型

[代码](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model) · [v1.0.0](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model/releases/tag/v1.0.0)

连接五项宏观驱动与经营收入，用滚动回测、VIF 和季节朴素基准约束解释。18 项测试通过；合成数据 R² 96.57%，24 个月回测 MAPE 1.28%。

### 营运资金与现金流预测模型

[代码](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model) · [v1.0.0](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model/releases/tag/v1.0.0)

用 DSO、DIO 和 DPO 驱动应收、库存、应付与现金滚动，单独披露资金缺口。20 项测试通过；压力缺口 62.63 百万元，改善情景 CCC 从 68 天降至 40 天。

## 正式版本

| 项目 | 版本 | 测试 | 主要输出 |
| --- | --- | ---: | --- |
| 仓储成本与经营分析 | [v1.5.6](https://github.com/wangyihanworld-ux/Warehouse-analysis-model/releases/tag/v1.5.6) | 67 | FIFO、仓储费、库龄、敏感性 |
| 预算差异与滚动预测 | [v0.1.0](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model/releases/tag/v0.1.0) | 22 | 差异桥、年度预测、目标缺口 |
| 客户与产品盈利能力 | [v0.1.0](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model/releases/tag/v0.1.0) | 15 | 贡献利润、集中度、敏感性 |
| 宏观经济情景预测 | [v1.0.0](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model/releases/tag/v1.0.0) | 18 | 回归、回测、VIF、情景预测 |
| 营运资金与现金流预测 | [v1.0.0](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model/releases/tag/v1.0.0) | 20 | 周转天数、现金滚动、资金缺口 |

## 数据与结论边界

五个公开 Demo 全部使用程序生成的合成数据，不包含真实客户、公司、合同、费率、银行账户或 ERP 明细。结果用于展示分析方法与工程能力，不构成真实经营预测。
