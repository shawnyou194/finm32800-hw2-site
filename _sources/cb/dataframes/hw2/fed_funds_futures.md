# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures

Daily ohlcv-1d bars from Databento's CME Globex dataset (GLBX.MDP3), pulled with the parent symbol ZQ.FUT so that one request returns every listed ZQ contract. One row per contract per trading day, with columns date, symbol, open, high, low, close, and volume. A contract settles at 100 minus the average daily effective fed funds rate over its month, so 100 - close is the market's forecast of that average. The symbol column also includes calendar spreads such as ZQU6-ZQZ6; keep only outright contracts (such as ZQU6) with fedwatch.filter_outright_contracts. Months far from expiry trade thinly and may have no bar on a given day. The pull covers the trailing 180 days by default and is free under the course's Databento subscription.


## DataFrame Glimpse

```
Rows: 11764
Columns: 7
$ date   <datetime[ns]> 2026-10-18 00:00:00
$ symbol          <str> 'ZQG7-ZQJ7'
$ open            <f64> 16.5
$ high            <f64> 16.5
$ low             <f64> 16.5
$ close           <f64> 16.5
$ volume          <u64> 31


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/datasets/GLBX.MDP3                                   |
| Tags                           | Monetary Policy, Futures, Fed Funds                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento API via Python                                                   |
| Data available up to (min)     | 2026-10-18 00:00:00                                                             |
| Data available up to (max)     | 2026-10-18 00:00:00                                                             |
| Dataframe Path                 | /Users/shawnyou/Desktop/Data Pipelines/hw2-shawnyou194/_data/fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file:///Users/shawnyou/Desktop/Data Pipelines/hw2-shawnyou194/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-19 15:05:36           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

