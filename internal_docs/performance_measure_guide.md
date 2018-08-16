## Guideline for Measuring Performance

Each benchmark result is the median of five run results produced using the integer random number generator seeds 1 through 5. All five run results must also be reported. The following measurements should be included:
  * quality of the model
  * running time
  * cloud cost 

### Quality of the Model

The quality of the model is measured by a certain evaluation metric e.g. MAPE. Please use common utility script `evaluate.py` to get the benchmark quality value in each run
```bash
python <benchmark directory>/common/evaluate.py <submission directory>/submission_seed_<seed value>.csv
``` 

### Running Time

The wallclock running time of each run should be measured by 
```bash
time -p python <submission directory>/train_score.py
```

### Cloud Cost

Include the total cost of obtaining the median run result using fixed prices for the general public at the time the result is collected. Do not use spot 
pricing. If you use Azure, you can estimate the costs for Azure products using this [online pricing calculator](https://azure.microsoft.com/en-us/pricing/calculator/).  