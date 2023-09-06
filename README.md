# Ex02-Outlier
# AIM:
To read a given dataset and remove outliers and save a new dataframe.

# ALGORITHM:
(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

# PROGRAM:
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

df = pd.read_csv("/content/heights.csv")

sns.boxplot(data=df)

sns.scatterplot(data=df)

max =df['height'].quantile(0.90)

min =df['height'].quantile(0.15)

max

min

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

low = min-1.5*iqr

high = max+1.5*iqr

dq = df[((df['height']>=min)&(df['height']<=max))]

 dq

## ZSCORE:

 import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}

df = pd.DataFrame(data)

df

sns.boxplot(data=df)

z = np.abs(stats.zscore(df))

print(df[z['weight']>3])

val = [12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]

out=[]

def d_o(val):

  ts=3
  
  m=np.mean(val)
  
  sd=np.std(val)
  
  for i in val:
  
    z=(i-m)/sd
    
    if np.abs(z)>ts:
    
      out.append(i)
      
  return out

  op = d_o(val)

  op 

  # OUTPUT:

![265260744-ce20a1d1-83d7-4ba9-ba68-d1b6a6a9fc74](https://github.com/Anuayshh/Expt2/assets/127651217/bb9c6930-d2aa-432d-8ee8-17f0e2baaa1e)

![265260769-d99857a5-ba5d-4205-b136-fe5db64f82e4](https://github.com/Anuayshh/Expt2/assets/127651217/64f358b8-5dd0-4a12-95af-ebcb5e4d28a8)

![265260794-3575c862-ddc9-4676-bc2a-eb0b028c0335](https://github.com/Anuayshh/Expt2/assets/127651217/105dccbb-9d5d-4594-a912-3d3fe22a259e)

![265260809-77c62ada-fc65-4dd1-bf90-6fb4fad91bd0](https://github.com/Anuayshh/Expt2/assets/127651217/089989d2-cf9d-4a2e-8dc8-d901da6ac068)

![265260824-1baf73cc-50a3-4b5c-9811-68c7a104cc09](https://github.com/Anuayshh/Expt2/assets/127651217/52c33fc9-2209-4183-86e4-0ee537828440)

![265260866-188ebebc-0dcf-443e-afbd-15986f2b10a4](https://github.com/Anuayshh/Expt2/assets/127651217/c178fdbf-14ea-4072-9112-672dff362bb6)

![265260898-5d623ceb-b7ea-4993-bd0f-626bc7e4bc72](https://github.com/Anuayshh/Expt2/assets/127651217/0738d411-2056-45e9-bd99-4b52252476f0)

![265260911-849cecb5-3c55-48bf-999f-8dbc43f85049](https://github.com/Anuayshh/Expt2/assets/127651217/486ad020-97d4-483a-91c7-0736be80838c)

![265260926-bb55307b-ca2e-447a-9cba-f1a18fcf8066](https://github.com/Anuayshh/Expt2/assets/127651217/883175ae-1a00-4d32-9311-bd42a297d684)






  # RESULT:
  Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.










