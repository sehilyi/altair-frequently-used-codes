# 4ce-frequently-used-codes
This repository contains python codes that I have been using frequently for 4CE projects. The purpose of this repository is for my convenience :)

## Pandas

Long to wide:
```py
df = pd.melt(df, id_vars=['siteid', 'lab', 'period', 'length'], value_vars=days, var_name='day', value_name='value')
```

Sort by value:
```py
df = df.sort_values(by=['siteid'])
```

Append vertical:
```py
meta.append(nometa)
```

Filter by str contains:
```py
df[df['A'].str.contains("hello")]
```

Concat strings in two columns:
```py
df['siteid-phase'] = df.siteid + df.phase.astype(str)
```

## Altair

Channel:
```py
alt.X("day:Q", title=None, bin=alt.Bin(maxbins=20), axis=alt.Axis(labelAngle=0, tickCount=3), scale=alt.Scale(clamp=True)),
```

Text:
```py
text = points.mark_text(
    align='left',
    baseline='middle',
    dx=7
).encode(
    text='label'
)
```

Colors:
```py
color=alt.Color('symbol', scale=alt.Scale(scheme='category20')),
```

Filters:
```py
.transform_calculate(
    order="{'Low Risk':0, 'Medium Risk': 1, 'High Risk': 2}[datum.variable]"  
).transform_filter(
    {'field': 'metric', 'oneOf': [metric]}
)
```
