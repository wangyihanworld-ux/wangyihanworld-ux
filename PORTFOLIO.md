# 项目运行与验证索引

所有命令均从对应仓库根目录运行。安装建议使用独立虚拟环境；生成文件为合成演示或注明来源的公开数据。

## [Warehouse-analysis-model](https://github.com/wangyihanworld-ux/Warehouse-analysis-model)

python -m pip install -r requirements.txt

```text
python -m unittest discover -s tests -v
python -m warehouse_analysis.demo
```

2026-10-27：74 项主测试通过。详细边界和样例见仓库 README。

## [Budget-variance-forecast-model](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model)

python -m pip install -e .

```text
python -m unittest discover -s tests -v
python -m budget_variance_forecast.demo
python -m budget_variance_forecast.baseline
```

2026-10-27：34 项主测试通过。详细边界和样例见仓库 README。

## [Working-capital-cashflow-forecast-model](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model)

python -m pip install -e .

```text
python -m unittest discover -s tests -v
python -m working_capital.demo
python -m working_capital.evidence
python -m working_capital.comparison
```

2026-10-27：32 项主测试通过。详细边界和样例见仓库 README。

## [Customer-profitability-analysis-model](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model)

python -m pip install -e .

```text
python -m unittest discover -s tests -v
python -m customer_profitability.demo
python -m customer_profitability.allocation
```

2026-10-27：24 项主测试通过。详细边界和样例见仓库 README。

## [Macroeconomic-scenario-forecast-model](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model)

python -m pip install -e .

```text
python -m unittest discover -s tests -v
python -m macro_forecast.demo
python -m macro_forecast.benchmark_evidence
python -m macro_forecast.public_case
python -m macro_forecast.robustness
```

2026-10-27：31 项主测试通过。详细边界和样例见仓库 README。

## [Payment-settlement-reconciliation-lab](https://github.com/wangyihanworld-ux/Payment-settlement-reconciliation-lab)

Python 3.10+; standard-library analysis

```text
python -m unittest -v
python -m demo_flow
```

2026-10-27：35 项主测试通过。详细边界和样例见仓库 README。

## [Stablecoin-peg-risk-lab](https://github.com/wangyihanworld-ux/Stablecoin-peg-risk-lab)

Python 3.10+; standard-library analysis

```text
python -m unittest -v
python -m analyze
```

2026-10-27：18 项主测试通过。详细边界和样例见仓库 README。

## [ai-job-match](https://github.com/wangyihanworld-ux/ai-job-match)

Node.js 22+ for tests; no runtime dependencies for the web pages

```text
npm test
```

2026-10-27：8 项主测试通过。详细边界和样例见仓库 README。

## [task-reminder](https://github.com/wangyihanworld-ux/task-reminder)

Node.js 22+ for tests; no runtime dependencies for the web pages

```text
npm test
```

2026-10-27：2 项主测试通过。详细边界和样例见仓库 README。
