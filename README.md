# goit-rdb-hw-07
# goit-rdb-hw-07

Домашня робота з PostgreSQL, time-series features, JSONB та індексації.

## Data source

Для роботи використано NYC Yellow Taxi dataset за March 2024.

Дані завантажуються у Google Colab з офіційного Parquet-файлу через Python-код.

## Main tasks

У notebook реалізовано:

- daily aggregation по `pickup_zone_id` і `ts_day`;
- lag features: 1 day, 7 days, 30 days;
- rolling 7-day average fare;
- rolling 30-day fare volatility;
- cumulative та expanding features;
- JSONB event-log з різними event types;
- JSONB queries через `@>`, `?`, `?|` та JSONPath;
- GIN index для JSONB;
- expression B-tree index для `device`;
- `EXPLAIN ANALYZE` до і після індексів;
- порівняння JSONB та normalized checkout table.

## How to run

1. Відкрити `Oksana_Levchenko_hw7.ipynb` у Google Colab.
2. Виконати всі клітинки через **Runtime → Restart and run all**.
3. Notebook автоматично встановлює потрібні бібліотеки, запускає PostgreSQL через `pgserver` і завантажує дані.

## Files

- `Oksana_Levchenko_hw7.ipynb` — основний notebook
- `README.md` — опис домашньої роботи

## Result

У роботі побудовані time-series ML features, JSONB event-log, індекси та виконано аналіз продуктивності через `EXPLAIN ANALYZE`.
