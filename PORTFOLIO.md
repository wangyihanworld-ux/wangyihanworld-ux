# 王怡涵财务分析与商业分析项目作品集

## 作品集定位

这套作品集面向财务 BP、FP&A、经营分析和商业分析岗位，也用于支持经济与商业分析方向的研究生申请。五个项目覆盖成本、预算、客户、宏观环境和现金流，形成从经营明细到管理决策的分析链条。所有公开案例均使用合成数据，并提供一键 Demo、Excel 管理报告、自动化测试、GitHub Actions 和正式 Release。

## 项目组合

| 决策层次 | 项目 | 回答的问题 |
| --- | --- | --- |
| 交易与运营 | 仓储成本分析 | 库存如何流转，费用如何形成，数量是否守恒 |
| 计划与执行 | 预算差异分析 | 实际为何偏离预算，全年可能达到多少 |
| 客户与产品 | 盈利能力分析 | 谁创造收入，谁真正创造贡献利润 |
| 外部环境 | 宏观情景预测 | 外部变量变化时收入如何变化，模型是否优于基准 |
| 资产负债与现金 | 营运资金预测 | 增长为何占用现金，资金缺口何时出现 |

## 项目一 仓储成本与经营分析模型

**业务问题。** 仓储费取决于批次入库时间、FIFO 出库顺序、存放天数和费率，简单用期末库存乘统一费率无法解释跨批次出库。

**方法与验证。** 按仓库和物料建立 FIFO 队列；出库前检查可用库存，充足时按时间拆分，不足时整笔拒绝并记录缺口。每个批次验证“原始数量等于累计出库加期末剩余”。67 项测试覆盖跨批次分摊、同日流水、库存不足、费率、报表和 Demo。

**结果与局限。** 合成演示仓储费 20,101.90 元，期末库存 375 吨，数量守恒异常 0。当前未按费率变更日分段计费，同日流水仍依赖源数据顺序。

[代码](https://github.com/wangyihanworld-ux/Warehouse-analysis-model) · [Release](https://github.com/wangyihanworld-ux/Warehouse-analysis-model/releases/tag/v1.5.6)

## 项目二 预算差异与滚动预测模型

**业务问题。** 管理层需要区分销量、价格、结构、单位成本和固定费用分别贡献多少利润差异，并判断全年目标是否可实现。

**方法与验证。** 对预算与实际进行键值和期间校验，构建收入与利润差异桥；锁定实际月份，只对未来应用三种情景。差异归因合计必须与经营利润总差异勾稽。22 项测试覆盖输入、历史锁定、情景方向与报告。

**结果与局限。** 收入较预算增加 17,584 元，但经营利润减少 10,724.36 元。情景是条件模拟，差异拆分顺序和交互项归属需与企业口径一致。

[代码](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model) · [Release](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model/releases/tag/v0.1.0)

## 项目三 客户与产品盈利能力分析模型

**业务问题。** 收入排名不等于客户价值，折扣、退货、产品成本、履约和服务投入可能使高收入客户变成低利润客户。

**方法与验证。** 将标价收入拆为净收入、毛利和贡献利润，计算收入占比、累计占比与 HHI，并测试价格、成本和服务投入。客户、产品和月份汇总必须与明细一致；分类阈值可配置。15 项测试通过。

**结果与局限。** 客户甲收入第一但贡献利润率仅 11.24%，整体为 29.50%。HHI 和客户标签只描述演示数据，不能直接作为真实客户去留标准。

[代码](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model) · [Release](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model/releases/tag/v0.1.0)

## 项目四 宏观经济情景与经营预测模型

**业务问题。** 财务团队需要把宏观假设转化为经营情景，但高拟合度可能来自过拟合或共线性，相关关系也不能解释为因果。

**方法与验证。** 使用五项宏观驱动、趋势和季节项建立回归；以扩展窗口回测后 24 个月，同时报告 MAE、RMSE、MAPE、VIF 和季节朴素基准。模型与基准使用相同回测月份。18 项测试通过。

**结果与局限。** 合成数据 R² 96.57%，回测 MAPE 1.28%，模型 RMSE 2.84，季节朴素基准 14.16。合成数据精度不能外推到真实企业。

[代码](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model) · [Release](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model/releases/tag/v1.0.0)

## 项目五 营运资金与现金流预测模型

**业务问题。** 收入和利润增长不等于现金增长，回款放慢、库存增加和账期缩短都可能形成资金缺口。

**方法与验证。** 用 DSO、DIO、DPO 驱动应收、库存和应付，再连接回款、采购、付款和费用到现金余额。应收、库存、应付和现金四套滚动关系必须逐月守恒。20 项测试通过。

**结果与局限。** 压力情景资金缺口 62.63 百万元，增长情景仍缺 19.12 百万元，改善情景 CCC 从 68 天降至 40 天。月度模型不替代日级资金计划、账龄分析或融资安排。

[代码](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model) · [Release](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model/releases/tag/v1.0.0)

## 建议阅读顺序

先看各仓库 README 的报告截图，再运行一键 Demo，随后查看核心计算代码、自动化测试和 Release 说明。评估重点应是业务口径、验证方法、异常处理、模型局限和结果如何支持管理决策，而不只是代码能否运行。
