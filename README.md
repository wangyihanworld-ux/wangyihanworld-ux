# Business Analytics & Decision Systems

围绕经营分析、库存与现金流、交易核对和数字资产风险的可复现项目。每个仓库提供运行入口、样例、测试与适用边界。

[English](README.en.md) · [项目与运行索引](PORTFOLIO.md) · [验证记录](VALIDATION.md)

## 经营分析与决策

| 项目 | 解决的问题 | 主要输出 |
|---|---|---|
| [仓储成本与经营分析](https://github.com/wangyihanworld-ux/Warehouse-analysis-model) | 库存流转如何形成仓储费，异常如何追溯？ | FIFO 批次分配、历史月末库存、费用与库龄、异常清单、Excel 报告 |
| [预算差异与滚动预测](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model) | 收入增长为何未必带来利润增长？ | 销量／结构／价格／成本差异桥、情景预测、预测复盘 |
| [营运资金与现金流](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model) | 周转政策和费用假设分别怎样影响现金？ | DSO／DIO／DPO、最低现金与资金缺口、周转与 OPEX 分离比较 |
| [客户与产品盈利分析](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model) | 高收入客户是否真正贡献利润？ | 净收入到贡献利润、集中度、共享费用分配与阈值敏感性 |
| [宏观情景与预测评估](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model) | 宏观变量能提供多少增量预测信息？ | 时间顺序回测、简单基线、发布滞后假设、共同年份稳健性结果 |

## 交易系统与数字金融

| 项目 | 解决的问题 | 主要输出 |
|---|---|---|
| [电商订单与支付对账](https://github.com/wangyihanworld-ux/Payment-settlement-reconciliation-lab) | 银行结算匹配后，订单为何仍可能需要退款复核？ | 订单／发货／取消／退货状态、整数金额对账、幂等收件箱、累计收款与迟到事件检查 |
| [稳定币偏离风险分析](https://github.com/wangyihanworld-ux/Stablecoin-peg-risk-lab) | 如何区分价格偏离、持续时间与恢复确认？ | USDC／DAI 公开数据快照、基点偏离、阈值敏感性、仅用历史信息的预警 |

## 浏览器交互原型

| 项目 | 内容 | 运行方式 |
|---|---|---|
| [求职匹配交互原型](https://github.com/wangyihanworld-ux/ai-job-match) | 本地关键词提取、城市筛选、确定性岗位排序、JD 对照与表达练习；不调用大模型或招聘 API | 直接打开 index.html；可导出独立 HTML |
| [时刻台与晷](https://github.com/wangyihanworld-ux/task-reminder) | 事务提醒、重复任务、番茄钟、浏览器本地保存、JSON 备份校验 | [在线体验](https://wangyihanworld-ux.github.io/task-reminder/) |
| [本项目索引仓库](https://github.com/wangyihanworld-ux/wangyihanworld-ux) | 中英文项目导航、运行命令与验证索引 | 阅读本页与 PORTFOLIO.md |

## 报告预览

来自完全合成的业务演示数据：

![仓储管理摘要](https://raw.githubusercontent.com/wangyihanworld-ux/Warehouse-analysis-model/main/docs/images/management-summary.png)

## 数据、验证与解释

- 经营与支付案例使用合成数据；宏观及稳定币案例另有注明来源、版本和许可的公开数据。
- 测试用于核对实现、边界与可复现性，不等于企业采用、真实收益或个人能力认证。
- 宏观回归在共同年份比较中不一定优于简单基线；稳定币压力案例不证明未来预测能力。
- 求职原型的分数是关键词覆盖率，不是录用概率；提醒网页需要浏览器正常运行，不能替代可靠的后台闹钟服务。
- 实现与验证有 AI 辅助。项目不包含个人简历、申请材料或真实客户业务明细。
