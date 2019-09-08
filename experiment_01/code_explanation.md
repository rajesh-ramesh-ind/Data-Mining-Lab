#### Imporing necessary packages
```python3
import pandas as pd
from apyori import apriori
```

#### Loading the dataset
```python3
store_data = pd.read_csv("../datasets/apiori.csv", header=None)
```

#### Printing the dataset
```python3
print(store_data)
```

#### Convert Pandas DataFrame into a list of lists
```python3
for i in range(0, 22):
    records.append([str(store_data.values[i, j]) for j in range(0, 6)])
```

#### Building the Apriori model
```python3
association_rules = apriori(records, min_support=0.50, min_confidence=0.7, min_lift=1.2, min_length=2)
```

#### Building the Apriori model and fetching results
```python3
association_rules = apriori(records, min_support=0.50, min_confidence=0.7, min_lift=1.2, min_length=2)
association_results = list(association_rules)
```

#### Print the model's result or summary of the dataset
```python3
print(association_results)
```
