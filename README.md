###Download data
```
docker-compose run --rm freqtrade download-data --pairs BTC/BUSD --exchange binance --days 5 -t 5m
```

###Back testing
```
docker-compose run --rm freqtrade backtesting --config user_data/config.json --strategy SampleStrategy --timerange
20220327-20220330 -i 5m
```

###Change docker-compose image for freqtradeorg/freqtrade:stable_plot

###Export result in graph  
```
docker-compose run --rm freqtrade plot-dataframe --strategy SampleStrategy --export-filename user_data/backtest_res
ults/backtest-result.json -p BTC/BUSD
```