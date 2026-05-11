---
source_file: "paysim.csv"
profiled_at: "2026-05-11T16:29:04.757662+00:00"
row_count: 6362620
column_count: 11
file_size: "470.7 MB"
delimiter: ","
---

# Dataset: `paysim.csv`

Automatically generated schema description. This file profiles **6,362,620 rows** across **11 columns** (file size: 470.7 MB, delimiter: `,`).

## Schema overview

| # | Column | Logical type | Pandas dtype | Non-null | Nulls | Null % | Unique |
|---|--------|--------------|--------------|----------|-------|--------|--------|
| 1 | `step` | integer | `int64` | 6,362,620 | 0 | 0.00% | 743 |
| 2 | `type` | categorical (string) | `str` | 6,362,620 | 0 | 0.00% | 5 |
| 3 | `amount` | float | `float64` | 6,362,620 | 0 | 0.00% | 5,316,900 |
| 4 | `nameOrig` | string | `str` | 6,362,620 | 0 | 0.00% | 6,353,307 |
| 5 | `oldbalanceOrg` | float | `float64` | 6,362,620 | 0 | 0.00% | 1,845,844 |
| 6 | `newbalanceOrig` | float | `float64` | 6,362,620 | 0 | 0.00% | 2,682,586 |
| 7 | `nameDest` | string | `str` | 6,362,620 | 0 | 0.00% | 2,722,362 |
| 8 | `oldbalanceDest` | float | `float64` | 6,362,620 | 0 | 0.00% | 3,614,697 |
| 9 | `newbalanceDest` | float | `float64` | 6,362,620 | 0 | 0.00% | 3,555,499 |
| 10 | `isFraud` | integer | `int64` | 6,362,620 | 0 | 0.00% | 2 |
| 11 | `isFlaggedFraud` | integer | `int64` | 6,362,620 | 0 | 0.00% | 2 |

## Column details

### `step`

- **Logical type:** integer
- **Pandas dtype:** `int64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 743
- **Statistics:**
  - min: 1
  - max: 743
  - mean: 243.3972
  - median: 239.0000
  - std: 142.3320
  - zeros: 0
  - negatives: 0
- **Sample values:** `1`, `1`, `1`, `1`, `1`

### `type`

- **Logical type:** categorical (string)
- **Pandas dtype:** `str`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 5
- **Top 5 values:**
  - `CASH_OUT` — 2,237,500
  - `PAYMENT` — 2,151,495
  - `CASH_IN` — 1,399,284
  - `TRANSFER` — 532,909
  - `DEBIT` — 41,432
- **Sample values:** `PAYMENT`, `PAYMENT`, `TRANSFER`, `CASH_OUT`, `PAYMENT`

### `amount`

- **Logical type:** float
- **Pandas dtype:** `float64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 5,316,900
- **Statistics:**
  - min: 0.0000
  - max: 92,445,516.6400
  - mean: 179,861.9035
  - median: 74,871.9400
  - std: 603,858.2315
  - zeros: 16
  - negatives: 0
- **Sample values:** `9839.64`, `1864.28`, `181.0`, `181.0`, `11668.14`

### `nameOrig`

- **Logical type:** string
- **Pandas dtype:** `str`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 6,353,307
- **Top 10 values:**
  - `C2098525306` — 3
  - `C400299098` — 3
  - `C1999539787` — 3
  - `C1065307291` — 3
  - `C545315117` — 3
  - `C1976208114` — 3
  - `C1784010646` — 3
  - `C1530544995` — 3
  - `C1902386530` — 3
  - `C1677795071` — 3
- **Sample values:** `C1231006815`, `C1666544295`, `C1305486145`, `C840083671`, `C2048537720`

### `oldbalanceOrg`

- **Logical type:** float
- **Pandas dtype:** `float64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 1,845,844
- **Statistics:**
  - min: 0.0000
  - max: 59,585,040.3700
  - mean: 833,883.1041
  - median: 14,208.0000
  - std: 2,888,242.6730
  - zeros: 2102449
  - negatives: 0
- **Sample values:** `170136.0`, `21249.0`, `181.0`, `181.0`, `41554.0`

### `newbalanceOrig`

- **Logical type:** float
- **Pandas dtype:** `float64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 2,682,586
- **Statistics:**
  - min: 0.0000
  - max: 49,585,040.3700
  - mean: 855,113.6686
  - median: 0.0000
  - std: 2,924,048.5030
  - zeros: 3609566
  - negatives: 0
- **Sample values:** `160296.36`, `19384.72`, `0.0`, `0.0`, `29885.86`

### `nameDest`

- **Logical type:** string
- **Pandas dtype:** `str`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 2,722,362
- **Top 10 values:**
  - `C1286084959` — 113
  - `C985934102` — 109
  - `C665576141` — 105
  - `C2083562754` — 102
  - `C248609774` — 101
  - `C1590550415` — 101
  - `C451111351` — 99
  - `C1789550256` — 99
  - `C1360767589` — 98
  - `C1023714065` — 97
- **Sample values:** `M1979787155`, `M2044282225`, `C553264065`, `C38997010`, `M1230701703`

### `oldbalanceDest`

- **Logical type:** float
- **Pandas dtype:** `float64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 3,614,697
- **Statistics:**
  - min: 0.0000
  - max: 356,015,889.3500
  - mean: 1,100,701.6665
  - median: 132,705.6650
  - std: 3,399,180.1130
  - zeros: 2704388
  - negatives: 0
- **Sample values:** `0.0`, `0.0`, `0.0`, `21182.0`, `0.0`

### `newbalanceDest`

- **Logical type:** float
- **Pandas dtype:** `float64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 3,555,499
- **Statistics:**
  - min: 0.0000
  - max: 356,179,278.9200
  - mean: 1,224,996.3982
  - median: 214,661.4400
  - std: 3,674,128.9421
  - zeros: 2439433
  - negatives: 0
- **Sample values:** `0.0`, `0.0`, `0.0`, `0.0`, `0.0`

### `isFraud`

- **Logical type:** integer
- **Pandas dtype:** `int64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 2
- **Statistics:**
  - min: 0
  - max: 1
  - mean: 0.0013
  - median: 0.0000
  - std: 0.0359
  - zeros: 6354407
  - negatives: 0
- **Sample values:** `0`, `0`, `1`, `1`, `0`

### `isFlaggedFraud`

- **Logical type:** integer
- **Pandas dtype:** `int64`
- **Non-null:** 6,362,620 (100.00%)
- **Nulls:** 0 (0.00%)
- **Unique values:** 2
- **Statistics:**
  - min: 0
  - max: 1
  - mean: 0.0000
  - median: 0.0000
  - std: 0.0016
  - zeros: 6362604
  - negatives: 0
- **Sample values:** `0`, `0`, `0`, `0`, `0`

## Sample rows (first 5)

| `step` | `type` | `amount` | `nameOrig` | `oldbalanceOrg` | `newbalanceOrig` | `nameDest` | `oldbalanceDest` | `newbalanceDest` | `isFraud` | `isFlaggedFraud` |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | PAYMENT | 9839.64 | C1231006815 | 170136.0 | 160296.36 | M1979787155 | 0.0 | 0.0 | 0 | 0 |
| 1 | PAYMENT | 1864.28 | C1666544295 | 21249.0 | 19384.72 | M2044282225 | 0.0 | 0.0 | 0 | 0 |
| 1 | TRANSFER | 181.0 | C1305486145 | 181.0 | 0.0 | C553264065 | 0.0 | 0.0 | 1 | 0 |
| 1 | CASH_OUT | 181.0 | C840083671 | 181.0 | 0.0 | C38997010 | 21182.0 | 0.0 | 1 | 0 |
| 1 | PAYMENT | 11668.14 | C2048537720 | 41554.0 | 29885.86 | M1230701703 | 0.0 | 0.0 | 0 | 0 |

## Notes for downstream use

This description is intended to be passed to an LLM as schema context. Pair it with the user's analytical question so the model can reason about columns, types, and value distributions without needing to load the raw CSV.
