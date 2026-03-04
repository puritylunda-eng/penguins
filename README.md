# penguins
# Business Undertanding

This is meant to be a fun dataset for you to learn on and use it as something to play around with. This dataset includes data about different species of penguins from different islands with their dimensions and genders. What kind of insights can you get out of this?


In a professional context, the "Business Understanding" phase focuses on defining what success looks like. For this dataset, your objective is to quantify the physical differences between penguin populations to understand how species and environment (islands) influence growth.

Business Goals:
- Identify Patterns: Determine if physical traits (flipper length, beak size, weight) are distinct enough to identify a species without a DNA test.
- Environmental Impact: Assess if the specific island a penguin inhabits correlates with its physical health or size.
- Sexual Dimorphism: Understand the size gap between males and females across different species.

[Data Source](https://www.kaggle.com/datasets/amulyas/penguin-size-dataset)
# **Data Understanding**

- loading
- head and tail( glimpse of how the dat alooks like)
- shape
- info()
- data types
- descritptive stats (categorical)
- descritptive stats (numerical)
- missing values 
- duplicate
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
penguins_df=pd.read_csv("data/penguins_size.csv")
## head and tail
penguins_df.head()
penguins_df.tail()
## shape / dimension
rows,columns=penguins_df.shape 
output=f"RECORDS:{rows}|| FEATURES {columns}"
print(output)
## info
penguins_df.info()
## data types
penguins_df.dtypes
penguins_df.columns #features
## MISSING VALUES AND DUPLICATES
penguin_df.isna().sum()
penguin_df.duplicated().sum() # here no duplicates
isights:
data set
presence of missing values
## descriptive stats numerical
penguins_df.describe() #numerical
insights
-culmen= upper ridge of birds bill: 75% and below of the sample were at 48.55 mm
-50% was 44.45(50%)
-75% lay below 39.22 mm
-the longest length was at 59.6 mm(max)
-the smallest was at 32.1(min)
-most of the penguins culmen length fell about 43.92 mm
-the data spread was quite large as shown by the standart deviation(how far it is spread)

## categorical /qualitative data types
penguins_df.describe(include='object')
penguins_df['sex'].unique() # unique values in a column
penguins_df['island'].unique() # unique values in a column
penguins_df['species'].unique() # unique values in a column
