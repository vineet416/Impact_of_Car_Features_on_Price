# Impact of Car Features on Price

An Excel analytics project that measures how engine power, cylinders, fuel efficiency, body style, market category and brand affect a car's MSRP.
It helps a manufacturer decide which features justify a price premium and which segments are worth developing.
Data covers 11,914 US car listings from model years 1990–2017.

## Project Files

| File | Description | 
|---|---|
| `Dataset.xlsx` | Raw data (sheet `Car_data`): 11,914 rows × 16 columns. |
| `Impact_of_Car_Features_on_Price_Analysis.xlsx` | Full workbook (9 sheets): raw and cleaned data, Task 1–5, make/body-style pivots, charts, slicers. |
| `README.md` | Project documentation. |

## Dataset

| Column | Description |
|---|---|
| `Make`, `Model`, `Year` | Manufacturer, model name, model year (1990–2017). |
| `Engine Fuel Type` | Fuel type (regular, premium, diesel, flex-fuel, electric…). |
| `Engine HP`, `Engine Cylinders` | Horsepower and cylinder count. |
| `Transmission Type`, `Driven_Wheels` | Transmission and drive layout. |
| `Number of Doors` | 2, 3 or 4. |
| `Market Category` | Comma-separated tags (Luxury, Crossover, Hybrid…). |
| `Vehicle Size`, `Vehicle Style` | Compact/Midsize/Large; body style. |
| `highway MPG`, `city mpg` | Fuel efficiency. |
| `Popularity` | Popularity score. |
| `MSRP` | List price in USD (target variable). |

The `Cleaned data` sheet splits `Market Category` into two columns and adds `AVG MPG` = (highway + city) / 2.

## Approach

1. **Understand the data:** profile 16 columns, types, nulls and duplicates.
2. **Clean:** remove 715 duplicates and 102 rows missing HP, cylinders, doors or fuel type (11,914 → 11,097); fix data types; trim text; split `Market Category`.
3. **Analyse:** five tasks using pivots, scatter plots with trendlines, a 7-variable regression and `CORREL`.
4. **Report:** charts, slicers and written takeaways inside each task sheet.

## Key Insights

All figures were recomputed from the cleaned data (n = 11,097).

| Question | Finding |
|---|---|
| Power vs price | MSRP ≈ 369 × HP − 51,716. R² = 0.43, r = 0.66. About +$369 per HP. |
| Price drivers | Regression R² = 0.467. All variables significant (p < 0.001) except `Year` (p = 0.83). |
| Strongest driver | Engine HP (standardised β = 0.57), then cylinders (0.22), city mpg (0.13). |
| Cylinders vs MPG | r = −0.61. Avg highway MPG: 4 cyl 31.5, 6 cyl 24.0, 8 cyl 20.2, 12 cyl 17.7. |
| Brand pricing | Overall mean $41,901, median $30,600. Bugatti $1.76M, Rolls-Royce $351k, Porsche $102k, Toyota $29k. |
| Popularity | Highest: Hybrid 2,117, Flex Fuel 2,111, Diesel 1,977. Lowest: Exotic 893 (avg MSRP $240k). Overall 1,557. |
| Largest segments | Crossover (1,986) and Luxury (1,879) are the biggest tagged categories; 3,362 rows are untagged. |
| Body style | Sedan 24%, 4Dr SUV 21%, Coupe 19%, Convertible 14% of total listed MSRP. |
| Drive type | Avg MSRP: AWD $58.8k, RWD $57.2k, FWD $23.2k. |

## Tech Stack

- **Microsoft Excel:** Pivot Tables, Slicers, Power Query, Analysis ToolPak regression, charts.
- **Formulas:** `HLOOKUP`, `INDEX`, `MATCH`, `MAX`, `MIN`, `CORREL`.
- **Techniques:** descriptive statistics, linear regression, correlation analysis.

## How to Use

1. Open `Impact_of_Car_Features_on_Price_Analysis.xlsx` in desktop Excel 2016 or later.
2. Read `Task 1`–`Task 5`. Each sheet has the question, output and takeaway.
3. Use the slicers in `Min and Max MSRP by body style` to filter by body style.
4. To redo the regression, enable Analysis ToolPak and run *Data → Data Analysis → Regression* on `Cleaned data` (Y = `MSRP`).
