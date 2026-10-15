# WYH — Finance and Economic Analysis Portfolio

[中文](README.md) · [Detailed portfolio in Chinese](PORTFOLIO.md)

I build reproducible models that connect business questions to financial definitions, reconciliations, scenario analysis and management reports. My interests include FP&A, finance business partnering, business analysis and postgraduate study in economics and analytics.

## Selected work

| Project | Decision question | Evidence and limitations |
| --- | --- | --- |
| [Budget variance and forecast review](https://github.com/wangyihanworld-ux/Budget-variance-forecast-model/blob/main/README.en.md) | Why did profit miss budget, and how did forecast vintages perform? | Reconciled profit bridge; preserved actuals; versioned forecasts; MAE/RMSE/bias/WAPE by lead time. Reconstructed synthetic vintages, not forecasts issued historically. |
| [Working capital and cash flow](https://github.com/wangyihanworld-ux/Working-capital-cashflow-forecast-model/blob/main/README.en.md) | When does growth create a funding gap? | Receivable/inventory/payable/cash rollforwards; nonnegative purchase constraints; explicit undefined ratios. No automatic borrowing or daily liquidity claim. |
| [Macroeconomic scenario evaluation](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model/blob/main/README.en.md) | What can a macro model explain, and what can it forecast? | Separate conditional and lagged evaluations; VIF and transparent benchmarks; official public-data extension. No causal or real-time-vintage claim. |
| [Customer profitability](https://github.com/wangyihanworld-ux/Customer-profitability-analysis-model/blob/main/README.en.md) | Which high-revenue customers contribute little profit? | Net-revenue/contribution reconciliation, concentration and configurable tiers. Price sensitivities assume constant volume. |
| [Warehouse cost analysis](https://github.com/wangyihanworld-ux/Warehouse-analysis-model/blob/main/README.en.md) | How do batch movements and inventory age determine cost? | FIFO, quantity conservation, insufficient-stock rejection and Excel reports. Uses synthetic transactions. |

## Public economic-data case

The [Hong Kong WDI case](https://github.com/wangyihanworld-ux/Macroeconomic-scenario-forecast-model/blob/main/docs/public-data-case.md) uses World Bank annual GDP growth, inflation and ILO-modelled unemployment for 1991–2024. A lagged expanding-window regression is evaluated over 2009–2024.

RMSE is 3.87 percentage points, versus 3.95 for a historical-mean baseline. The limited improvement is part of the finding. Latest-vintage data incorporate revisions; this is not a real-time historical backtest. Raw responses, retrieval metadata, checksums and offline reproduction commands are available in the repository.

## Reproducibility and boundaries

Each project includes source, tests, CI configuration and reproducible examples. The five business demonstrations contain synthetic data, not private records or claimed business impact. The public macro case is separately attributed. English READMEs explain execution, definitions and limitations; older release tags are historical snapshots and may not include the current enhancements.

Skills demonstrated: Python, pandas, NumPy, Excel report automation, financial reconciliation, forecast evaluation and communication of model limitations.
