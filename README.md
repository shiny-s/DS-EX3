# Ex03-Univariate-Analysis

## AIM:
To read the given data and perform the univariate analysis with different types of plots.

## EXPLAINATION:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## ALGORITHM:

Step1:Read the given data set  using standard libraries.

Step2:Get the information about the data.

Step3:Remove the null values from the data.

Step4:Mention the datatypes from the data.

Step5:Count the values from the data.

Step6:Do plots like sepallength,species,sepalwidth.

## PROGRAM:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

df=pd.read_csv("/content/iris.csv")

df.head()

df.tail()

df.nunique()

df.iloc[:,4].value_counts()

for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")

sns.countplot(x='species',data=df)

dfv=df.loc[df['species']=='virginica']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.xlabel('sepal length')
plt.show()
##plt.plot(df_setosa['sepal_length'],np.zeros_like(df_setosa['sepal_length']),'o')

dfs=df.loc[df['species']=='setosa']
dfc=df.loc[df['species']=='versicolor']

plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'o')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'-')
plt.xlabel('SEPALLENGTH')
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_width","sepal_width").add_legend();
plt.show()

sns.FacetGrid(df,hue="species").map(plt.scatter,"petal_length","sepal_length").add_legend();
plt.show()

sns.pairplot(df,hue="species",size=3)

```

## OUPTUT:

![1](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/ff95db08-e2cb-43a9-b8a4-90d4d97c18ae)
![2](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/82106f0d-a070-43d4-80aa-90ff42751b84)
![3](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/f4971455-4718-41c4-81ef-e2893b9670e1)
![4](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/250121ae-219f-4d91-a95c-14cb8c1bca6f)
![5](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/91fe7a10-170a-4f7e-849f-7ceadaa3c198)
![6](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/081b76d2-6ea6-4f35-a91c-d78960f23a8c)
![7](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/348711a2-bb0e-4fbc-a1e7-340fee6e80a1)
![8](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/2671bd04-c93b-4b17-9bdf-5a58d4af9633)
![9](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/a416db08-fd15-4d25-bc12-beb8e8543485)
![10](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/e70e9fea-bdae-4594-893d-e32c6251fc2a)
![11](https://github.com/Krupa-Varsha-P/DS-EX-3/assets/100466625/f3e94963-ca77-4c26-8c71-904c3519c5dc)





## RESULT:
Thus we have read the given data and performed the univariate analysis with different types of plots are created and verified successfully.
