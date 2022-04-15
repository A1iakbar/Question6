```python
import pandas as pd
import numpy as np
```


```python
df = pd.read_csv(r"C:\Users\ralia\Desktop\Work\country_vaccination_stats.csv")
```


```python
df['daily_vaccinations'] = df['daily_vaccinations'].fillna(0)
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>date</th>
      <th>daily_vaccinations</th>
      <th>vaccines</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Argentina</td>
      <td>12/29/2020</td>
      <td>0.0</td>
      <td>Sputnik V</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Argentina</td>
      <td>12/30/2020</td>
      <td>15656.0</td>
      <td>Sputnik V</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Argentina</td>
      <td>12/31/2020</td>
      <td>15656.0</td>
      <td>Sputnik V</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Argentina</td>
      <td>1/1/2021</td>
      <td>11070.0</td>
      <td>Sputnik V</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Argentina</td>
      <td>1/2/2021</td>
      <td>8776.0</td>
      <td>Sputnik V</td>
    </tr>
  </tbody>
</table>
</div>




```python
df["daily_vaccinations"].loc[df["date"] == "1/6/2021"].sum()
```




    1466568.0


