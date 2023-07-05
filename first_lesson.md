# Introduction to Data Science:

Using pandas to read and visualise the data
```
import pandas as pd
data_frame = pd.read_csv("ratings.csv")
data_frame.columns = ["usuarioID", "filmeID", "nota", "momento"]
data_frame.head(20)
```

```
print("Media", data_frame.nota.mean().round(3))
print("Mediana", data_frame.nota.median())
print("Mode", data_frame.nota.mode())
```

```
import seaborn as sns
import matplotlib.pyplot as plt
sns.catplot(x = "original_language",
            kind = "count",
            aspect = 2,
            data = data_frame.query("original_language!='en'"),
            order = order,
            palette= "GnBu_d"
            )
```
