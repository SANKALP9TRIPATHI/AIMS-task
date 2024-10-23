import pandas as pd
import numpy as np

data = {
    'Category': ['small', 'medium', 'large', 'medium', 'small', 'large']
}

df = pd.DataFrame(data)

category_order = ['small', 'medium', 'large']
ordinal_mapping = {category: index for index, category in enumerate(category_order)}
df['Ordinal'] = df['Category'].map(ordinal_mapping)

print(df)
