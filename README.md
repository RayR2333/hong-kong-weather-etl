# Hong Kong Weather ETL Pipeline

使用 Open-Meteo API 拉取香港多个地点的小时天气数据，存入 DuckDB，并生成日汇总表。

## 项目说明
- **Extract**：从 Open-Meteo API 抽取小时级天气数据
- **Transform**：清洗合并、计算日均温度、总降水量等衍生字段
- **Load**：写入 DuckDB 的 `raw_weather` 和 `daily_weather_summary` 两张表
- 支持防重复写入，可重复运行

## 技术栈
- Python
- requests + pandas
- DuckDB
- Google Colab

## 如何使用
1. 打开 `Open_Meteo_Practice1.ipynb`
2. 修改脚本中的 `locations` 列表或 `FORECAST_DAYS`
3. 运行完整脚本单元格即可

## 数据表
- `raw_weather`：原始小时数据
- `daily_weather_summary`：按地点+日期聚合的日汇总数据
